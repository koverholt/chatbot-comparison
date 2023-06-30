<script lang="ts">
	import { Navbar, NavBrand } from 'flowbite-svelte';
	import { onMount } from 'svelte';
	import { Input, Label, Helper } from 'flowbite-svelte';
	import { Button, ButtonGroup } from 'flowbite-svelte';

	var utterance: string = 'Tell me about the Tensor G2 processor in the Pixel tablet';

	function fillAndSend(utterance: string, time: number) {
		document.querySelectorAll('iframe').forEach((item) =>
			setTimeout(function () {
				item.contentWindow.document.body
					.querySelector('df-messenger')
					.shadowRoot.querySelector('df-messenger-chat')
					.shadowRoot.querySelector('df-messenger-user-input')
					.shadowRoot.querySelector('.input-box-wrapper > input').value = utterance;
			}, time * 1000)
		);
		document.querySelectorAll('iframe').forEach((item) =>
			setTimeout(function () {
				item.contentWindow.document.body
					.querySelector('df-messenger')
					.shadowRoot.querySelector('df-messenger-chat')
					.shadowRoot.querySelector('df-messenger-user-input')
					.shadowRoot.querySelector('.input-box-wrapper > button')
					.click();
			}, (time + 1) * 1000)
		);
	}

	onMount(() => {
		fillAndSend('Hello', 1);
		// fillAndSend('Does the Pixel 7 Pro support fast charging?', 5);
		// fillAndSend('How does the Pixel Watch track sleep?', 15);
		// fillAndSend('How does the Nest Camera tell the difference between people, animals, vehicles, and packages?',	25);
	});
</script>

<Navbar let:hidden let:toggle class="bg-[#E8F0FE] p-6 mb-9">
	<NavBrand href="/">
		<span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">
			Bot Comparison - Google Store Virtual Agent
		</span>
	</NavBrand>
</Navbar>

<div class="flex text-center">
	<div class="w-0 grow">
		<form>
			<ButtonGroup class="w-1/2 mb-9">
				<Input class="w-full" type="text" id="utterance" bind:value={utterance} required />
				<Button color="blue" type="submit" on:click={fillAndSend(utterance, 0)}>Submit</Button>
			</ButtonGroup>
		</form>
	</div>
</div>

<div class="flex">
	<div class="w-1/4">
		<iframe src="/bot1.html" height="600" class="mx-auto" title="bot1" />
	</div>
	<div class="w-1/4">
		<iframe src="/bot2.html" height="600" class="mx-auto" title="bot2" />
	</div>
	<div class="w-1/4">
		<iframe src="/bot3.html" height="600" class="mx-auto" title="bot3" />
	</div>
	<div class="w-1/4">
		<iframe src="/bot4.html" height="600" class="mx-auto" title="bot4" />
	</div>
</div>
