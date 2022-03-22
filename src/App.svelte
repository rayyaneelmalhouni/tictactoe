<script>
	import Score from "./components/Score.svelte"
	import Board from "./components/Board.svelte"
	let squares = Array(9).fill(null);
	let turn = true;
	let winner = "";
	const winningConditions = [
   [0, 1, 2],
   [3, 4, 5],
   [6, 7, 8],
   [0, 3, 6],
   [1, 4, 7],
   [2, 5, 8],
   [0, 4, 8],
   [2, 4, 6]
	];
	
	function getMessage(self) {
		if (!squares[self.detail.text - 1]) {
			squares[self.detail.text - 1] = turn ? "X": "O";
        	turn = turn ? false: true;
			winner = checkWinner();
			console.log(winner)
		}
    }
	function checkWinner() {
		let r = "";
		for (let i = 0; i < winningConditions.length; i++) {
			let condition = winningConditions[i]
				if (squares[condition[0]] === squares[condition[1]] && squares[condition[0]] === squares[condition[2]]){
					if (squares[condition[0]]) {
						r = squares[condition[0]]
					}
					
				}
		
		}
		
		return r;
		
	}
    function retry() {
		squares = Array(9).fill(null);
		winner = "";
		turn = true;
	}
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
<Score {turn} {winner} on:retry={retry}/>
<Board on:message={getMessage} {squares}/>