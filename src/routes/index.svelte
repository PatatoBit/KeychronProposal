<script>
	import { onMount } from 'svelte';
	import { fly } from 'svelte/transition';
	import Typewriter from 'svelte-typewriter';
	import Rain from '$lib/components/rain.svelte';

	let loaded = false;
	let end = false;

	// onMount set loaded to true
	onMount(() => {
		loaded = true;
	});
	// set delay 12 seconds to change end to true
	setTimeout(() => {
		end = true;
	}, 8 * 1000);
</script>

<svelte:head>
	<title>อยากได้ Keychron Q2</title>
</svelte:head>

<div class="flex flex-col bg-slate-800 w-full h-screen items-center justify-center">
	{#if loaded}
		<div
			in:fly={{ x: 500, y: 100, duration: 1000, delay: 0 }}
			class="flex text-orange-500 text-6xl"
		>
			ผมอยากได้คีย์บอร์ด Keychron <span class="text-blue-400"> Q2 </span> เพราะ
		</div>
	{/if}

	<Typewriter interval={10} cascade>
		<div class="flex flex-row">
			<ul class="mt-5 text-xs sm:text-lg flex-1">
				<li class="text-green-500">✅มีการ lube มาให้แล้ว ทำให้เสียงดีโดยไม่ต้องทำอะไรเลย</li>
				<li class="text-green-500">✅ตัวเครื่องอะลูมิเนียมดูสวยหรู</li>
				<li class="text-green-500">✅มีสีสีนให้เลือกมากมาย</li>
				<li class="text-green-500">
					✅Keycap hot swappable สามารถเปลี่ยนไปคีย์อะไรก็ได้เองตามใจชอบ
				</li>
				<li class="text-green-500">✅ใช้ได้ทั้ง MacOS และ Windows</li>
				<li class="text-green-500">✅สามารถ remap ปุ่มได้ง่ายผ่านซอฟ์แวร์</li>
				<li class="text-green-500">✅ดูหรูหรา กิ๊บเก๋ยูเรก้า</li>
				<li class="text-green-500">✅เสียงดี สบายหู อย่างกับฟังเพลง</li>
				<li class="text-green-500">✅9arm ใช้</li>
				<li class="text-green-500">✅9arm บอกว่าดีมากๆ</li>
			</ul>
			<ul class="mt-5 text-xs sm:text-lg flex-1">
				<li class="text-green-500">✅ตัวเครื่องมีผิวสัมผัสดีมาก ดูพรีเมียม</li>
				<li class="text-green-500">✅มันดีมาก ผมอยากได้</li>
				<li class="text-green-500">✅พิมพ์ก็ดี เสียงก็ดี</li>
				<li class="text-green-500">✅สี Carbon Black สวย</li>
				<li class="text-green-500">✅สี Silver Grey สวย</li>
				<li class="text-green-500">✅สี Navy Blue สวย</li>
				<li class="text-green-500">✅ทุกสีสวยหมดเลย</li>
				<li class="text-green-500">✅แต่ผมชอบ Navy Blue มากที่สุด</li>
				<li class="text-green-500">✅อยากได้</li>
				<li class="text-green-500">✅อยากได้</li>
				<li class="text-green-500">✅อยากได้</li>
				<li class="text-green-500">✅ของเค้าดีจริงงงงงงงง</li>
			</ul>
		</div>
	</Typewriter>
	{#if end}
		<Rain />
	{/if}
</div>
