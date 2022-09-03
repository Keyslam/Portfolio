<script lang="ts">
    export let title: string;
    export let description: string;
</script>

<a href="#">
    <div class="card">
        <div class="img-container">
            <div class="placeholder">
                <img src="https://loremflickr.com/640/360" alt="TEMP" loading="lazy"/>
            </div>

            <div class="img-container-spacer" />

            <div class="content">
                <h1>{title}</h1>
                <p>{description}</p>
            </div>
        </div>
    </div>
</a>

<style>
	.card {
		border: 1px solid rgba(255, 255, 255, 0.2);
		border-radius: 0.5rem;
		background-color: transparent;
		width: 250px;
		height: 250px;

		margin: 5px 5px 5px 5px;

		transition: transform 0.2s;
	}

	.img-container {
		width: 100%;
		height: 140.63px;
		position: relative;
		top: 0;
	}

	.img-container-spacer {
		height: 140.63px;
	}

    .card {
        width: 150px;
        height: 200px;
    }

    .img-container {
        height: 84.38px;
    }

    .img-container-spacer {
        height: 84.38px;
    }

	.card img {
		width: 100%;
		height: 100%;
		position: absolute;
		border-radius: 0.5rem;
		font-size: 0;

		opacity: 1;
		animation-name: fadeInOpacity;
		animation-iteration-count: 1;
		animation-timing-function: ease-in;
		animation-duration: 0.5s;
	}

	@keyframes fadeInOpacity {
		0% {
			opacity: 0;
		}
		100% {
			opacity: 1;
		}
	}

	.card .placeholder {
		width: 100%;
		height: 100%;
		position: absolute;
		background-color: rgba(255, 255, 255, 0.1);
		border-top-left-radius: 0.5rem;
		border-top-right-radius: 0.5rem;
	}

	.card:hover {
		transform: scale(1.05);
	}

	.content {
		padding: 0px;
		text-align: center;
	}

	.content h1 {
		font-size: 20px;
		color: white;
	}

	.content :global(p) {
		font-size: 14px;
		color: white;
	}
</style>