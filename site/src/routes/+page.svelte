<script lang="ts">
	import { Navbar, NavBrand } from 'flowbite-svelte';
	import { onMount } from 'svelte';

	onMount(() => {
		document.querySelectorAll('iframe').forEach((item) =>
			setTimeout(function () {
				item.contentWindow.document.body
					.querySelector('df-messenger')
					.shadowRoot.querySelector('df-messenger-chat')
					.shadowRoot.querySelector('df-messenger-user-input')
					.shadowRoot.querySelector('.input-box-wrapper > input').value = 'Hello';
			}, 1000)
		);
		document.querySelectorAll('iframe').forEach((item) =>
			setTimeout(function () {
				item.contentWindow.document.body
					.querySelector('df-messenger')
					.shadowRoot.querySelector('df-messenger-chat')
					.shadowRoot.querySelector('df-messenger-user-input')
					.shadowRoot.querySelector('.input-box-wrapper > button')
					.click();
			}, 2000)
		);

		document.querySelectorAll('iframe').forEach((item) =>
			setTimeout(function () {
				item.contentWindow.document.body
					.querySelector('df-messenger')
					.shadowRoot.querySelector('df-messenger-chat')
					.shadowRoot.querySelector('df-messenger-user-input')
					.shadowRoot.querySelector('.input-box-wrapper > input').value =
					'Does the Pixel 7 Pro support fast charging?';
			}, 5000)
		);
		document.querySelectorAll('iframe').forEach((item) =>
			setTimeout(function () {
				item.contentWindow.document.body
					.querySelector('df-messenger')
					.shadowRoot.querySelector('df-messenger-chat')
					.shadowRoot.querySelector('df-messenger-user-input')
					.shadowRoot.querySelector('.input-box-wrapper > button')
					.click();
			}, 6000)
		);

		document.querySelectorAll('iframe').forEach((item) =>
			setTimeout(function () {
				item.contentWindow.document.body
					.querySelector('df-messenger')
					.shadowRoot.querySelector('df-messenger-chat')
					.shadowRoot.querySelector('df-messenger-user-input')
					.shadowRoot.querySelector('.input-box-wrapper > input').value =
					'How does the Pixel Watch track my time sleeping?';
			}, 15000)
		);
		document.querySelectorAll('iframe').forEach((item) =>
			setTimeout(function () {
				item.contentWindow.document.body
					.querySelector('df-messenger')
					.shadowRoot.querySelector('df-messenger-chat')
					.shadowRoot.querySelector('df-messenger-user-input')
					.shadowRoot.querySelector('.input-box-wrapper > button')
					.click();
			}, 16000)
		);

		document.querySelectorAll('iframe').forEach((item) =>
			setTimeout(function () {
				item.contentWindow.document.body
					.querySelector('df-messenger')
					.shadowRoot.querySelector('df-messenger-chat')
					.shadowRoot.querySelector('df-messenger-user-input')
					.shadowRoot.querySelector('.input-box-wrapper > input').value =
					'How does the Nest Camera tell the difference between people, animals, vehicles, and packages?';
			}, 25000)
		);
		document.querySelectorAll('iframe').forEach((item) =>
			setTimeout(function () {
				item.contentWindow.document.body
					.querySelector('df-messenger')
					.shadowRoot.querySelector('df-messenger-chat')
					.shadowRoot.querySelector('df-messenger-user-input')
					.shadowRoot.querySelector('.input-box-wrapper > button')
					.click();
			}, 26000)
		);
	});
</script>

<Navbar let:hidden let:toggle>
	<NavBrand href="/">
		<span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">
			Google Store Virtual Agent
		</span>
	</NavBrand>
</Navbar>

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
