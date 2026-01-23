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
	githublink: {
		type: String,
		default: undefined,
	},

	});
</script>

<template>
	<div>
		<div>
			
		</div>
		<div>
			<h2><a :href="pdflink">{{ title }}</a></h2>
			<p>{{ description }}</p>
			<p v-if="githublink">Open in Github: <a :href="githublink" target="_blank" rel="noopener noreferrer">{{ githublink }}</a></p>
		</div>
	</div>
</template>
