<script>
	import { logo, heroImg } from '../../assets/';
	import styles from '../../styles/index';

	export let Component;
	export let title;
	export let description;
</script>

<div class={styles.hocContainer}>
	<div class={styles.hocContentBox}>
		<img src={logo} alt="logo" class={styles.hocLogo} />

		<div class={styles.hocBodyWrapper}>
			<div class="flex flex-row w-full">
				<h1
					class={`flex ${styles.headText} head-text`}
				>
					{@html title}
				</h1>
			</div>

			<p class={`${styles.normalText} my-10`}>{@html description}</p>

			<svelte:component this={Component} />
		</div>

		<p class={styles.footerText}>Made with 💜 by Arnab Chatterjee</p>
	</div>

	<div class="flex flex-1">
		<img src={heroImg} alt="hero-img" class="w-full xl:h-full object-cover" />
	</div>
</div>
