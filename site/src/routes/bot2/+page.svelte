<script lang="ts">
	import { onMount } from 'svelte';

	onMount(() => {
		const script = document.createElement('script');
		script.src = 'https://www.gstatic.com/dialogflow-console/fast/messenger-cx/bootstrap.js?v=1';
		script.async = true;
		document.head.appendChild(script);
	});
</script>

<div>
	<df-messenger
		df-cx="true"
		chat-title="Gen Responses"
		agent-id="5e367795-33eb-4272-9398-60ee7e2cdf67"
		language-code="en"
		expand="true"
	/>
</div>
