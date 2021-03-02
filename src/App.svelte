<script lang="ts">
  import Tailwind from "./Tailwind.svelte";
	let menu = [
		{label: "What I am"},
		{label: "What I do"},
		{label: "What I like"},
		{label: "What I want"}
	]
</script>

<Tailwind />
<main class="bg-white-500">
	<div class="bg-blue-400 h-screen w-screen flex flex-col items-center justify-between">
		<div class="">
			<ul class="flex items-center justify-center">
				{#each menu as view}
					<li class="p-4 text-xl">{view.label}</li>
				{/each}
			</ul>
		</div>
		<div class="bg-blue-500 w-11/12 flex items-center justify-center flex-grow rounded-xl">
			<img src="/portrait.jpg" alt="portrait" class="m-8 rounded-xl object-cover w-64 h-64 opacity-75 hover:opacity-100" />
			<div class="space-y-5">
				<h1 class="text-lg text-black font-semibold">Hello World !</h1>
				<p class="text-black-500 text-xl whitespace-pre-line">
					I live in a farm lost in the woods and I love to solve problems.
					Programming is my passion but I hate jargon though.
					I need to be understood by anyone because good ideas can come from anywhere.
				</p>
			</div>
		</div>
		<div>
			<ul class="flex items-center justify-center">
					<li class="p-4 text-xl">Made in 2021 using Svelte, Tailwind & Vercel</li>
			</ul>
		</div>
	</div>
</main>
