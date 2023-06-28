<script lang="ts">
	import { Input, Label, Helper } from 'flowbite-svelte';
	import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte';
	import { onMount } from 'svelte';

	onMount(() => {

		document.querySelectorAll('iframe').forEach( item =>
		  setTimeout(function(){ item.contentWindow.document.body.querySelector("df-messenger").shadowRoot.querySelector("df-messenger-chat").shadowRoot.querySelector("df-messenger-user-input").shadowRoot.querySelector(".input-box-wrapper > input").value="Hello" }, 1000)
		)

		document.querySelectorAll('iframe').forEach( item =>
		  setTimeout(function(){ item.contentWindow.document.body.querySelector("df-messenger").shadowRoot.querySelector("df-messenger-chat").shadowRoot.querySelector("df-messenger-user-input").shadowRoot.querySelector(".input-box-wrapper > button").click() }, 2000)
		)

    document.querySelectorAll('iframe').forEach( item =>
		  setTimeout(function(){ item.contentWindow.document.body.querySelector("df-messenger").shadowRoot.querySelector("df-messenger-chat").shadowRoot.querySelector("df-messenger-user-input").shadowRoot.querySelector(".input-box-wrapper > input").value="Does the Pixel 7 Pro support fast charging?" }, 5000)
		)

    document.querySelectorAll('iframe').forEach( item =>
		  setTimeout(function(){ item.contentWindow.document.body.querySelector("df-messenger").shadowRoot.querySelector("df-messenger-chat").shadowRoot.querySelector("df-messenger-user-input").shadowRoot.querySelector(".input-box-wrapper > button").click() }, 6000)
		)

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
