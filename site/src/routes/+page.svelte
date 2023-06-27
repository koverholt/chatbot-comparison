<script lang="ts">
	import { Input, Label, Helper } from 'flowbite-svelte';
	import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte';
	import { onMount } from 'svelte';

	onMount(() => {
		// code
	});
</script>

<Navbar let:hidden let:toggle>
	<NavBrand href="/">
		<span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">
			Google Store Virtual Agent
		</span>
	</NavBrand>
</Navbar>

<!-- <form>
	<Label for="first_name" class="mb-2">Input</Label>
	<Input type="text" id="first_name" placeholder="Test" required />
</form> -->

<div class="flex">
	<div class="w-1/4">
		<iframe src="/bot1" height="600" class="mx-auto" />
	</div>
	<div class="w-1/4">
		<iframe src="/bot2" height="600" class="mx-auto" />
	</div>
	<div class="w-1/4">
		<iframe src="/bot3" height="600" class="mx-auto" />
	</div>
	<div class="w-1/4">
		<iframe src="/bot4" height="600" class="mx-auto" />
	</div>
</div>
