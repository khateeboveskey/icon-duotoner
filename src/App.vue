<template>
	<div class="h-screen grid place-items-center">
		<div>
			<h1 class="scroll-m-20 text-4xl font-extrabold tracking-tight mb-10">🎨 Icon Duotoner</h1>
				<Button variant="outline" class="w-full h-fit p-0">
					<label
					class="hover:cursor-pointer w-full h-24 flex items-center justify-center"
					for="file-uploader">
					<Upload class="inline me-2 w-4" />
						Choose an SVG file
					</label>
					</Button>
				<input class="hidden" id="file-uploader" type="file" accept="image/svg+xml" />
		</div>
	</div>
</template>


<script setup>
import Button from './components/ui/button/Button.vue';
import { Upload } from 'lucide-vue-next';
</script>