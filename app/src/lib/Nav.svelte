<script lang="ts">
	const { active } = $props<{ active?: 'demos' | 'support' }>();

	let open = $state(false);
	const toggle = () => (open = !open);
	const close = () => (open = false);
</script>

<nav class="nav full-bleed">
	<div class="container nav-row">
		<a href="/" class="brand logo hide-mobile" aria-label="Homepage">
			<img
				src="/src/lib/assets/ReQuest_logo.png"
				alt="ReQuest Logo"
				class="brand logo"
				aria-hidden="true"
			/>
		</a>

		<button
			class="brand brand-button hide-desktop"
			aria-label="Toggle navigation menu"
			aria-controls="navigation-menu"
			aria-expanded={open}
			onclick={toggle}
		>
			<img
				src="/src/lib/assets/ReQuest_logo.png"
				alt="ReQuest Logo"
				class="logo hide-desktop"
				aria-hidden="true"
			/>
		</button>

		<div class="navlinks hide-mobile">
			<a href="/" class:active={active === undefined}>Home</a>
			<a href="/demos" class:active={active === 'demos'}>Demos</a>
			<a href="/support" class:active={active === 'support'}>Support</a>
		</div>

		<div class="spacer"></div>

		<a class="pill invite" href="https://discord.com/api/oauth2/authorize?client_id=601492201704521765&permissions=1497132133440&scope=applications.commands%20bot" rel="noopener">Invite ReQuest</a>
	</div>

	<div id="navigation-menu" class="mobile-drawer hide-desktop" data-open={open}>
		<a href="/" onclick={close}>Home</a>
		<a href="/demos" onclick={close}>Demos</a>
		<a href="/support" onclick={close}>Support</a>
	</div>
</nav>

<div class="scrim" data-open={open} onclick={close} aria-hidden="true" ></div>

<style>
	/* uses global classes from app.css; keep local empty or add tweaks */
</style>