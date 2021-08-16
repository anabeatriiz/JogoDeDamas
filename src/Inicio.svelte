<script>
	import Sobre from "./Sobre.svelte";
</script>

<img src="images/Tabuleiro.jpg" alt="Plano de fundo" />
<div class="div">
	<h1>Jogo de Damas</h1>
	<div class="texto">
		<i class="fas fa-play icone" />
		<a href="#/jogar/"><span class="text">JOGAR</span></a>
	</div>
	<div class="texto">
		<a href="#/sobre/"><span class="text">Sobre</span></a>
	</div>
	<div class="texto">
		<a href="#/ajuda/"><span class="text">Ajuda</span></a>
	</div>
</div>
<span class="ball" />
<span class="ball1" />
<span class="ball2" />
<span class="ball3" />

<style>
	img {
		width: 100%;
		height: auto;
	}

	h1 {
		margin-top: 6%;
	}

	.div {
		width: 38%;
		height: 62%;
		background-color: #9e3fa2;
		border-radius: 2%;
		position: absolute;
		top: 24%;
		left: 32%;
		box-shadow: 4px 5px rgba(0, 0, 0, 0.535);
		text-align: center;
	}

	.texto {
		width: 83%;
		height: 13%;
		box-shadow: 4px 5px rgba(0, 0, 0, 0.535);
		margin-left: 8%;
		margin-top: 6%;
		background-color: violet;
		border-radius: 8px;
	}

	.icone {
		color: black;
		font-size: 2vw;
		margin-right: 2%;
	}

	.text {
		color: black;
		font-size: 3vw;
	}

	a {
		text-decoration: none;
	}

	.text:hover {
		font-weight: bold;
	}

	.ball {
		width: 40px;
		height: 40px;
		background-color: #240e23;
		position: absolute;
		top: 19%;
		left: 31.5%;
		border-radius: 25%;
	}

	.ball1 {
		width: 40px;
		height: 40px;
		background-color: violet;
		position: absolute;
		top: 15%;
		left: 29%;
		border-radius: 25%;
	}

	.ball2 {
		width: 40px;
		height: 40px;
		background-color: #240e23;
		position: absolute;
		top: 85%;
		left: 68%;
		border-radius: 25%;
	}

	.ball3 {
		width: 40px;
		height: 40px;
		background-color: violet;
		position: absolute;
		top: 90%;
		left: 70%;
		border-radius: 25%;
	}

</style>
