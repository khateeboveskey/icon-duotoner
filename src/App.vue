<template>
	<div class="m-5 grid h-screen place-items-center">
		<div>
			<h1 class="mb-10 scroll-m-20 text-4xl font-extrabold tracking-tight">
				🎨 Icon Duotoner
			</h1>
			<form class="flex flex-col gap-4">
				<label for="file-uploader">
					<Upload class="inline me-2 w-4" />
					Choose an SVG file
				</label>
				<input class="hidden" id="file-uploader" type="file" accept="image/svg+xml" />
				<label for="tone-opacity-slider">Secondary Tone Opacity</label>
				<Slider id="tone-opacity-slider" :default-value="[5]" :max="10" />
			</form>
		</div>
	</div>
</template>

<script setup>
// Icons
import { Upload } from 'lucide-vue-next';

// Components
import Slider from './components/ui/slider/Slider.vue';
</script>

<style scoped>
label[for='file-uploader'] {
	@apply flex h-24 w-full items-center justify-center rounded-md border border-slate-200 bg-white px-4 py-2 shadow-sm hover:cursor-pointer hover:bg-slate-100 hover:text-slate-900 dark:border-slate-800 dark:bg-slate-950 dark:hover:bg-slate-800 dark:hover:text-slate-50;
}
</style>
