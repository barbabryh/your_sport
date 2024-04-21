<script setup lang="ts">
import { userdataUserApi, touchMeApi } from '../api';
import { useProfileStore } from '../store';
import { onMounted, ref } from 'vue';

const profileStore = useProfileStore();

const showUserWarn = ref(false);
const showClickWarn = ref(false);
const clickResult = ref<number | null>(null);

onMounted(async () => {
	// Get username
	if (!profileStore.full_name && profileStore.id) {
		const resp = await userdataUserApi.getById(profileStore.id);
		if (resp.status != 200) {
			showUserWarn.value = true;
			return;
		}
		const data = resp.data;
		if (!data || !data.items) {
			showUserWarn.value = true;
			return;
		}
		const nameItem = data.items.find(item => {
			return item.category == 'Личная информация' && item.param == 'Полное имя';
		});
		if (!nameItem) {
			showUserWarn.value = true;
			return;
		}
		profileStore.full_name = nameItem?.value ?? null;
	}

	// Get touch data
	const resp = await touchMeApi.getTouch();
	if (resp.status != 200) {
		showClickWarn.value = true;
		return;
	}
	const data = resp.data;
	if (!data || !data.count) {
		showClickWarn.value = true;
		return;
	}
	clickResult.value = +data.count;
});




</script>

<template>
	<div>
		<p>Id: {{ profileStore.id }}</p>
		<p class="text-h1">
			Имя Фамилия<span v-if="profileStore.full_name">: {{ profileStore.full_name }}</span
			>
			</p>
		<p v-if="!profileStore.full_name">
			Не удалось 
			<a href="https://api.profcomff.com/?urls.primaryName=userdata"></a>
		</p>
		
		<p>Группа: {{profileStore.groups}}</p>
	</div>
</template>
