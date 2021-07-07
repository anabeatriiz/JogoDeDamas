<div class="container">
    <div class="navbar">
        <h2><a href="#/"><i class="fa fa-home" aria-hidden="true" /></a></h2>
        <h2><a href="#/"><i class="fa fa-play" aria-hidden="true" /></a></h2>
    </div>

    <div class="Ajuda">
        <div>
            <h1> Damas - Como Jogar</h1>
            <p>
              O jogo de damas é um jogo de tabuleiro praticado por duas pessoas/adversários, 
              no qual cada um tem 12 pedras que são diferenciadas pelas cores, claras e escuras.
              o primeiro a jogar é sempre o adversário que está com as pedras claras. o objetivo 
              do jogo é capturar, ou apenas imobilizar, todas as pedras do seu adversário.
              cada jogada é feita somente na diagonal pra frente e uma casa por vez - a não ser 
              que você precise capturar uma pedra. é obrigatório a captura das pedras e caso você 
              precise escolher qual capturar, priorize a captura que tenha mais pedras a serem pegas 
              ou a que lhe transforme em dama. quando uma pedra alcança a última linha do tabuleiro 
              ela se transforma em dama. Diferente de uma pedra normal, a dama pode andar todas as 
              casas, tanto na diagonal para frente como para trás, porém não pode passar por cima 
              de uma pedra da mesma cor que a sua e para diferenciar uma dama das outras pedras é 
              colocada uma pedra em cima da que virou dama.
            </p>
        </div>
    </div>
</div>

<style>
.container {
    display: flex;
    flex-direction: column;
    background: rgb(220, 192, 231);
    widows: 100vw;
    height: 100vh;
}

h1 {
    text-align: center;
}

p {
    width: 800px;
    margin-top: 20px;
    text-align: justify;
    font-size: 20px;
}
.navbar {
  overflow: hidden;
  background-color: blueviolet;
  width: 50%;
  box-shadow: 4px 5px black;;
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
  color: rgb(31, 54, 54);;
}
.Ajuda {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 50px;
}
</style>