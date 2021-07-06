<script>
  import Sobre from "./Sobre.svelte";

</script>

<img src="images/Tabuleiro.png" alt="Plano de fundo">
<div class="div">
  <h1>Jogo de Dama</h1>
  <div class="jogar">
    <i class="fas fa-play icone" />
    <a href="#/jogar/"><span class="text">JOGAR</span></a>
    <!-- <Link class="text" to="sobre">JOGAR</Link> -->
    <!-- <a ">jogar</a> -->
  </div>
  <div class="sobre">
    <a href="#/sobre/"><span class="text">Sobre</span></a>
  </div>
</div>
<span class="ball" />
<span class="ball1" />
<span class="ball2" />
<span class="ball3" />


<style>


img{
	width: 100%;
	height: auto;
}

h1{
	margin-top: 6%;
	/* font-size: 5vw; */
}
  h3{
color: purple;
}

.div{
	width: 38%;
	height: 62%;
	background-color: darkviolet;
	border-radius: 0%;
	position: absolute;
	top: 24%;
	left: 32%;
	box-shadow: 4px 5px black;
	text-align: center;
}

.jogar{
	width: 83%;
	height: 13%;
	box-shadow: 4px 5px black;
	margin-left: 8%;
	margin-top: 8%;
	background-color: violet;
	border-radius: 10px;
}

.sobre{
	width: 83%;
	height: 13%;
	box-shadow: 4px 5px black;
	margin-left: 8%;
	margin-top: 6%;
	background-color: violet;
	border-radius: 10px;

}

.icone{
	color: black;
	font-size: 2vw;
	margin-right: 2%;
}

.text{
	color: black;
	font-size: 3vw;
}

.texto{
	color: black;
	font-size: 3vw;
}

.texto1{
	color: black;
	font-size: 3vw;
}

a{
	text-decoration: none;
}

.text:hover{
	font-weight: bold;
}

.texto:hover{
	font-weight: bold; 
}

.texto1:hover{
	font-weight: bold;
}

.ball{
	width: 40px;
	height: 40px;
	background-color: rgb(19, 34, 34);
	position: absolute;
	top: 19%;
	left: 31.5%; 
	border-radius: 25%;
}

.ball1{
	width: 40px;
	height: 40px;
	background-color: violet;
	position: absolute;
	top: 15%;
	left: 29%; 
	border-radius: 25%;
}

.ball2{
	width: 40px;
	height: 40px;
	background-color: rgb(19, 34, 34);
	position: absolute;
	top: 85%;
	left: 68%; 
	border-radius: 25%;
}

.ball3{
	width: 40px;
	height: 40px;
	background-color: violet;
	position: absolute;
	top: 90%;
	left: 70%; 
	border-radius: 25%;
}
</style>