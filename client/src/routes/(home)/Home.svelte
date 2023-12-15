<script>
	import CustomButton from '../../lib/components/CustomButton.svelte';
	import CustomInput from '../../lib/components/CustomInput.svelte';
	let playerName = '';

	function setPlayerName(name) {
		playerName = name;
	}
</script>

<div class="flex flex-col">
	<CustomInput
		label="Name"
		placeHolder="Enter player name"
		value={playerName}
		handleValueChange={setPlayerName}
	/>
	<CustomButton title="Register" restStyles="mt-26" />
</div>
