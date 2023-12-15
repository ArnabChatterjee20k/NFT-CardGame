<script>
	import { goto } from '$app/navigation';
	import { onMount } from 'svelte';
	import PageHoc from '../../lib/components/PageHOC.svelte';
	import Home from './Home.svelte';
</script>
<PageHoc Component={Home} title="Welcome to Avax Gods <br/> a Web3 NFT Card Game" description="Connect to wallet to start playing <br/> the ultimate Web3 Battle Card Game"/>

