<script>
	import { onMount } from 'svelte';
	import { writable } from 'svelte/store';
	import { BrowserProvider } from 'ethers';
	export const walletAddress = writable('');
	export const provider = writable(null);
	export const contract = writable('');
	export const address = writable('');

	async function updateCurrentWalletAddress() {
		const accounts = await window?.ethereum?.request({ method: 'eth_requestAccounts' });
		if (accounts) walletAddress.set(accounts[0]);
	}
	onMount(() => {
		updateCurrentWalletAddress();
	});

	onMount(() => {
		(async () => {
			if (!window.ethereum) {
				alert('Please install metamask');
				return;
			}
			const walletProvider = new BrowserProvider(window.ethereum);
			const walletSigner = await walletProvider?.getSigner();
			// grab the signer and set the contract
			provider.update(()=>walletProvider);
		})()
	});
</script>

<slot />
