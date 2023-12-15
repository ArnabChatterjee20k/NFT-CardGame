<script>
	import { goto } from '$app/navigation';
	import { onMount } from 'svelte';
	import PageHoc from '../../lib/components/PageHOC.svelte';
	import CreateBattle from './CreateBattle.svelte';
	
</script>
<PageHoc Component={CreateBattle} title="Create <br/> a new battle" description="Create your own battle and wait for other players to join"/>

