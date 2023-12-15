<script>
	import styles from '../../styles';
	export let label;
	export let placeHolder;
	export let value;
	export let handleValueChange;
	const regex = /^[A-Za-z0-9]+$/;
</script>

<label for="name" class={styles.label}>{label}</label>
<input
	type="text"
	placeholder={placeHolder}
	{value}
	on:input={(e) => {
		if (e.target.value === '' || regex.test(e.target.value)) handleValueChange(e.target.value);
	}}
	class={styles.input}
/>
