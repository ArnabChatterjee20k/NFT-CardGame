<script>
	import styles from '../../styles';
	export let title;
	export let handleClick;
	export let restStyles;
</script>

<button type="button" on:click={handleClick} class={`${styles.btn} ${restStyles}`}>
	{title}
</button>
