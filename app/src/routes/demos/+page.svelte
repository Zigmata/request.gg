<section class="hero">
	<h1 class="hero-title">Demos</h1>
	<p class=hero-subtitle>
		Watch videos demonstrating ReQuest's core features in action!
	</p>
</section>

<div class=demo-video>
	<iframe src="https://www.youtube.com/embed/e4-Sel7bA2U?si=OYv-aIARSex7h9F8" title="ReQuest v1.0.0 features" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</div>

<style>
	.demo-video {
		position: relative;
		padding-bottom: 56.25%; /* 16:9 */
		padding-top: 25px;
		height: 1;
		width: 1024px;
		margin: 0 auto 40px;
	}

	.demo-video iframe {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		border-radius: 8px;
		box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
	}

	@media (max-width: 768px) {
		.demo-video {
			width: 100%
		}
	}
</style>
