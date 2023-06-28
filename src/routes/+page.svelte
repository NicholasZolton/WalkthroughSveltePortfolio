<script>
	import { base } from "$app/paths";
</script>

<main>
	<div id="homepage">
		<h1>Welcome to my Portfolio</h1>
		<div id="contacts">

			<div id="contact-row">
				<i class="fa-brands fa-github"></i>
				<a href="https://www.google.com/">Github</a>
			</div>

			<div style="width: 20px; height: 20px;" />

			<div id="contact-row">
				<i class="fa-brands fa-linkedin"></i>
				<a href="https://www.google.com/">LinkedIn</a>
			</div>

		</div>

		<div id="project-link">
			<a href="{base}/sorting_project"><p>Wanna see a sorting project I made?</p></a>
		</div>
	</div>
</main>

<style>

	#homepage {
		width: 100vw;
		height: 100vh;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		background-color: aliceblue;
	}

	#contacts {
		display:flex;
		flex-direction: row;
	}

</style>
