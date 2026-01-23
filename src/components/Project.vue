<script setup>
	const props = defineProps({
	title: {
		type: String,
		default: '',
	},
	description: {
		type: String,
		default: "Description Unavailable",
	},
	pdflink: {
		type: String,
		default: undefined,
	},
	pdfimage: {
		type: String,
		default: undefined,
	},
	githublink: {
		type: String,
		default: undefined,
	},

	});
</script>

<template>
	<div class="grid grid-cols-6 gap-4 m-[25px]">
		<div v-if="pdfimage" class="col-span-1">
			<a :href="pdflink" target="_blank" rel="noopener noreferrer"><img :src="`/img/${pdfimage}`" alt="Project Image" class="rounded-2xl" /></a>
		</div>
		<div class="col-span-3 justify-left">
			<h2 class="text-xl"><a :href="pdflink" target="_blank" rel="noopener noreferrer">{{ title }}</a></h2>
			<p><a :href="pdflink" target="_blank" rel="noopener noreferrer">{{ description }}</a></p>
			<p v-if="githublink">Open in Github: <a :href="githublink" target="_blank" rel="noopener noreferrer">{{ githublink }}</a></p>
		</div>
	</div>
</template>
