<script>
	import Score from "./components/Score.svelte"
	import Board from "./components/Board.svelte"

</script>
<style>
    .title {
		text-align: center;
		color: blue;
		font-size: 2em;
		margin-top: 10px;
	}

</style>
<h1 class="title">Tic Tac Toe Game</h1>
<Score />
<Board />