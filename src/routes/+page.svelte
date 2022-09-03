<script>
	import Card from "$lib/Card.svelte";

	import AccountCircle from "svelte-material-icons/AccountCircle.svelte";
	import Lightbulb from "svelte-material-icons/Lightbulb.svelte";
	import Code from "svelte-material-icons/CodeTags.svelte";
	import CardAccountMail from "svelte-material-icons/CardAccountMail.svelte";

	import { reveal } from "svelte-reveal";
	import { scrollTo, scrollRef, scrollTop } from "svelte-scrolling";
</script>

<main>
	<div class="sidebar">
		<ul>
			<img src="logo-1600x1600-nobg.png" alt="logo"/>
			<hr/>
			<a href="#" use:scrollTo={"profile"}><AccountCircle color="white" width="40%" height="auto"/></a>
			<a href="#" use:scrollTo={"skills"}><Lightbulb color="white" width="40%" height="auto"/></a>
			<a href="#" use:scrollTo={"projects"}><Code color="white" width="40%" height="auto"/></a>
			<a href="#" use:scrollTo={"contact"}><CardAccountMail color="white" width="40%" height="auto"/></a>
		</ul>
	</div>

	<div class="sidebar-spacer"/>

	<div class="content">
		<div class="section profile" use:scrollRef={"profile"}>	
			<h1 use:reveal={{ transition: "fade", easing: "easeInOutCubic"}}>Hi there!</h1>
			<h2 use:reveal={{ transition: "slide", delay: 1000, easing: "easeInOutCubic"}}>My name is Berber,</h2>
			<h3 use:reveal={{ transition: "slide", delay: 1500, easing: "easeInOutCubic"}}>and I am a Software Engineer.</h3>
		</div>

		<div class="section skills" use:scrollRef={"skills"}>
			<h2 use:reveal={{ transition: "fade", easing: "easeInOutCubic"}}>Skills</h2>
			<h3 use:reveal={{ transition: "fade", easing: "easeInOutCubic"}}>Heb ik niet</h3>
		</div>

		<div class="section projects" use:scrollRef={"projects"}>
			<h2 use:reveal={{ transition: "fade", easing: "easeInOutCubic"}}>Projects</h2>
			<h3 use:reveal={{ transition: "fade", easing: "easeInOutCubic"}}>Is poep</h3>

			<div class="card-container">	
				<Card title="Tieten" description="Very nice"/>
				<Card title="Tieten" description="Very nice"/>
				<Card title="Tieten" description="Very nice"/>
				<Card title="Tieten" description="Very nice"/>
				<Card title="Tieten" description="Very nice"/>
				<Card title="Tieten" description="Very nice"/>
				<Card title="Tieten" description="Very nice"/>
				<Card title="Tieten" description="Very nice"/>
				<Card title="Tieten" description="Very nice"/>
				<Card title="Tieten" description="Very nice"/>
				<Card title="Tieten" description="Very nice"/>
			</div>
		</div>

		<div class="section contact" use:scrollRef={"contact"}>
			<h2 use:reveal={{ transition: "fade", easing: "easeInOutCubic"}}>Contact</h2>
			<h3 use:reveal={{ transition: "fade", easing: "easeInOutCubic"}}>Beter van niet</h3>
		</div>
	</div>
</main>



<style>
	:global(body) {
		font-family: 'Fira Code', monospace;

		padding: 0px;
		margin: 0px;
		background-color: #25293A;
		color: white;
		height: 100vh;
	}

	main {
		display: flex;
	}

	.card-container {
		display: flex;
		align-items: center;
		justify-content: center;
		flex-wrap: wrap;
	}

	.content {
		width: 60%;
		margin-left: auto;
		margin-right: auto;
	}

	.content .section {
		padding-bottom: 200px;
	}

	.content h1 {
		font-size: 100px;
		margin: 0px;
	}

	.content h2 {
		margin-top: -10px;
		margin-bottom: 0px;
		margin-left: 40px;
	}
	.content h3 {
		margin-top:  0px;
		margin-left: 40px;
	}

	.content .profile {
		padding-top: 100px;
		height: calc(100vh - 100px) !important;
	}

	.content .skills {
		padding-top: 100px;
		height: calc(100vh - 100px) !important;
	}

	.content .projects {
		padding-top: 100px;
		height: calc(100vh - 100px) !important;
	}

	.content .contact {
		padding-top: 100px;
		height: calc(100vh - 100px) !important;
	}

	.sidebar-spacer {
		width: 100px;
		height: 100%;
	}

	.sidebar {
		position: fixed;
		top: 0;
		background-color: rgba(0, 0, 0, 0.1);
		box-shadow: 5px 0 5px -2px rgba(0, 0, 0, 0.1);
		width: 100px;
		height: 100%;
	}

	.sidebar ul {
		list-style: none;
		padding: 0;
		display: flex;
		align-items: center;
		justify-content: flex-start;
		flex-direction: column;
		height: 100%;
	}

	.sidebar ul img {
		width: 90%;
		border-radius: 50%;
		height: auto;
		margin-top: 10px;
		margin-bottom: 10px;
	}

	.sidebar ul hr {
		width: 80%;
		color:rgba(0, 0, 0, 0.2)
	}

	.sidebar ul a {
		display: flex;
		justify-content: center;
		margin-top: 30px;
		margin-bottom: 30px;
	}

	.sidebar ul a {
		transition: transform .2s;
	}

	.sidebar ul a:hover {
		transform: scale(1.2); 
	}
</style>