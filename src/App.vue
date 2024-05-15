<template>
	<div class="m-5 sm:m-0 w-screen flex flex-col md:flex-row h-screen">
		<!-- Options Pane -->
		<div class="w-1/3 grid place-items-center">
			<form class="flex flex-col gap-4">
				<h1 class="mb-5 text-center scroll-m-20 text-4xl font-extrabold tracking-tight">
					🎨 Icon Duotoner
				</h1>
				<label for="file-uploader">
					<Upload class="inline me-2 w-4" />
					Choose an SVG file
				</label>
				<input class="hidden" id="file-uploader" type="file" accept="image/svg+xml" />
				<label for="tone-color-input">Color</label>
				<input class="h-8 border-0 [&::-webkit-appearance]:hidden" type="color" id="tone-color-input" />
				<label for="tone-opacity-slider">Tone Opacity</label>
				<Slider id="tone-opacity-slider" :default-value="[5]" :max="10" />
				<Button>
					<Download class="inline me-2 w-4" />
					Download
				</Button>
			</form>
		</div>
		<!-- Preview Pane -->
		<div class="w-2/3 grid place-items-center">
			Preview Here
		</div>
	</div>
</template>

<script setup>
// Icons
import { Upload } from 'lucide-vue-next';
import { Download } from 'lucide-vue-next';

// Components
import Slider from './components/ui/slider/Slider.vue';
import Button from './components/ui/button/Button.vue';
</script>

<style scoped>
	/* * {
		border: 1px solid red; 
	} */

	label[for='file-uploader'] {
		@apply flex h-24 w-full items-center justify-center rounded-md border border-slate-200 bg-white px-4 py-2 shadow-sm hover:cursor-pointer hover:bg-slate-100 hover:text-slate-900 dark:border-slate-800 dark:bg-slate-950 dark:hover:bg-slate-800 dark:hover:text-slate-50;
	}

	input[type="color"]::-webkit-color-swatch-wrapper {
		padding: 0;
	}

	input[type="color"]::-webkit-color-swatch {
		border: none;
		@apply rounded-md;
	}
</style>
