<script lang="ts">
	// runes are available if you want to add state later (e.g., mobile drawer)
	const { active } = $props<{ active?: 'features' | 'support' }>();

	let open = $state(false);
	const toggle = () => (open = !open);
	const close = () => (open = false);
</script>

<nav class="nav full-bleed">
	<div class="container nav-row">
    <!-- Desktop brand -->
    <img src="src/lib/assets/ReQuest_logo.png" alt="ReQuest Logo" class="brand logo hide-mobile" aria-hidden="true"/>

    <!-- Mobile brand -->
    <button
      class="brand brand-button hide-desktop"
      aria-label="Toggle navigation menu"
      aria-controls="navigation-menu"
      aria-expanded={open}
      onclick={toggle}
    >
      <img src="src/lib/assets/ReQuest_logo.png" alt="ReQuest Logo" class="logo hide-desktop" aria-hidden="true"/>
    </button>

    <!-- Desktop links -->
		<div class="navlinks hide-mobile">
      <a href="/" class:active={active === undefined}>Home</a>
			<a href="/features" class:active={active === 'features'}>Features</a>
			<a href="/support" class:active={active === 'support'}>Support</a>
		</div>

		<div class="spacer"></div>

		<a class="pill invite" href="/invite" rel="noopener">Invite</a>
	</div>

  <!-- Mobile drawer -->
  <div id="mobile-menu" class="mobile-drawer hide-desktop" data-open={open}>
    <a href="/" onclick={close}>Home</a>
    <a href="/features" onclick={close}>Features</a>
    <a href="/support" onclick={close}>Support</a>
    <a class="pill invite" href="/invite" rel="noopener" onclick={close}>Invite</a>
  </div>
</nav>

<style>
	/* uses global classes from app.css; keep local empty or add tweaks */
</style>
