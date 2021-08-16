<script>
	import { onMount, afterUpdate } from "svelte";

	let tabuleiro = [];
	let pecaAtual = {
		linha: 0,
		coluna: 0,
		peca: "",
	};

	let duploClick = true;

	function handleClick(event) {
		const linha = event.target.getAttribute("data-linha");
		const coluna = event.target.getAttribute("data-coluna");
		const tipoPeca = event.target.getAttribute("data-peca");
		console.log("peça", tipoPeca);

		if (duploClick) {
			const copiaTabuleiro = tabuleiro;
			copiaTabuleiro[linha][coluna] = "#";
			pecaAtual["peca"] = tipoPeca;

			console.log("linha", linha, "coluna", coluna);
			tabuleiro = [...copiaTabuleiro];

			pecaAtual[linha] = linha;
			pecaAtual[coluna] = coluna;
			duploClick = false;
		} else {
			const copiaTabuleiro = tabuleiro;
			copiaTabuleiro[linha][coluna] = pecaAtual.peca;

			console.log("linha", linha, "coluna", coluna);
			tabuleiro = [...copiaTabuleiro];
			duploClick = true;
		}
	}

	function renderizar() {
		for (let i = 0; i < 8; i++) {
			tabuleiro[i] = [];
			for (let j = 0; j < 8; j++) {
				tabuleiro[i][j] = "#";

				if ((i + j) % 2 == 0) {
					if (i < 3) {
						tabuleiro[i][j] = "O";
					}

					if (i > 7 - 3) {
						tabuleiro[i][j] = "X";
					}
				}
			}
		}
	}

	function init() {
		renderizar();
		console.log(tabuleiro);
	}

	init();
</script>

<main>
	<div class="container">
		<div class="navbar">
			<h2>
				<a href="#/"><i class="fa fa-home" aria-hidden="true" /></a>
			</h2>
		</div>
		<br />
		<br />
		<br />
		<br />
		<div class="container1">
			<div class="tabuleiro">
				{#each tabuleiro as linhas, i}
					{#each linhas as coluna, j}
						{#if (i + j) % 2 == 0}
							{#if coluna == "O"}
								<div
									class="tabuleiro__quadrado tabuleiro__quadrado-normal"
								>
									<div
										class="peca peca-white"
										on:click={handleClick}
										data-linha={i}
										data-coluna={j}
										data-peca="O"
									/>
								</div>
							{:else if coluna == "X"}
								<div
									class="tabuleiro__quadrado tabuleiro__quadrado-normal"
								>
									<div
										class="peca peca-black"
										on:click={handleClick}
										data-linha={i}
										data-coluna={j}
										data-peca="X"
									/>
								</div>
							{:else}
								<div
									class="tabuleiro__quadrado tabuleiro__quadrado-normal"
									on:click={handleClick}
									data-linha={i}
									data-coluna={j}
								/>
							{/if}
						{:else}
							<div
								class="tabuleiro__quadrado tabuleiro__quadrado-peca"
							/>
						{/if}
					{/each}
				{/each}
			</div>
		</div>
	</div>
</main>

<style>
	.container {
		width: 2000vh;
		height: 150vh;
	}
	.container1 {
		width: 75vw;
		height: 100vh;
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
	}
	.navbar {
		overflow: hidden;
		background-color: blueviolet;
		width: 50%;
		box-shadow: 4px 5px rgba(0, 0, 0, 0.535);
	}
	.navbar a {
		float: left;
		display: block;
		color: white;
		text-align: center;
		padding: 14px 16px;
		text-decoration: none;
	}
	.navbar a:hover {
		background: white;
		color: rgb(31, 54, 54);
	}
	main {
		width: 400px;
		display: flex;
		align-items: center;
	}

	.tabuleiro {
		display: grid;
		grid-template-rows: repeat(8, 1fr);
		grid-template-columns: repeat(8, 1fr);
		max-width: 300px !important;
	}

	.tabuleiro__quadrado {
		width: 80px;
		height: 80px;
		border: 1px solid;
	}

	.tabuleiro__quadrado-normal {
		background-color: #049d62;
	}

	.tabuleiro__quadrado-peca {
		background-color: #c5c5c5;
	}

	.peca {
		width: 100%;
		height: 100%;
		border-radius: 50%;
	}

	.peca-white {
		background-color: white;
	}

	.peca-black {
		background-color: black;
	}
</style>
