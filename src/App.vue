<template>
	<div class="h-screen m-5 grid place-items-center">
		<div>
			<h1 class="scroll-m-20 text-4xl font-extrabold tracking-tight mb-10">🎨 Icon Duotoner</h1>
			<label for="file-uploader">
				<Upload class="inline w-4 me-2" />
				Choose an SVG file
			</label>
			<input class="hidden" id="file-uploader" type="file" accept="image/svg+xml" />
		</div>
	</div>
</template>

<script setup>
import { Upload } from 'lucide-vue-next';
</script>

<style scoped>
label[for="file-uploader"] {
	@apply hover:cursor-pointer w-full h-24 flex items-center justify-center border border-slate-200 bg-white shadow-sm hover:bg-slate-100 hover:text-slate-900 dark:border-slate-800 dark:bg-slate-950 dark:hover:bg-slate-800 dark:hover:text-slate-50 px-4 py-2 rounded-md
}
</style>