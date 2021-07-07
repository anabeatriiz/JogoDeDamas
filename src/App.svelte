<script>
	// import Rotas from './Rotas.svelte';
	
	import Router from 'svelte-spa-router';
  import Ajuda from './Ajuda.svelte';
	import Inicio from './Inicio.svelte';
	import Sobre from './Sobre.svelte';
	import Tabuleiro from './Tabuleiro.svelte';
  

  const routes = {
    '/': Inicio,
    '/sobre/': Sobre,
    '/jogar/': Tabuleiro,
    '/ajuda/': Ajuda,
    // '/CompB/:bound': ComponentB,
  }
</script>

<!-- <img src="imagens/Tabuleiro.png" /> -->
<main>
	<Router {routes}/>
</main>



<style>
</style>
