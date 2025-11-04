<script lang="ts">
	// You can add logic here if needed, e.g., current year
	const currentYear = new Date().getFullYear();
</script>

<footer>
	<nav>
		<a href="/terms-of-service">Terms of Service</a>
		<a href="/privacy-policy">Privacy Policy</a>
	</nav>
	<p>
		&copy; {currentYear} ReQuest. All rights reserved.
	</p>
</footer>

<style>
	footer {
		width: 100%;
		padding: 2rem 1rem;
		margin-top: 4rem; /* Give it some space from the content above */
		border-top: 1px solid var(--border);
		text-align: center;
		color: var(--muted);
		font-size: 0.9rem;
	}

	nav {
		display: flex;
		justify-content: center;
		gap: 1.5rem;
		margin-bottom: 1rem;
	}

	nav a {
		color: var(--muted);
		text-decoration: none;
	}

	nav a:hover {
		color: var(--fg);
		text-decoration: underline;
	}

	p {
		margin: 0;
	}
</style>