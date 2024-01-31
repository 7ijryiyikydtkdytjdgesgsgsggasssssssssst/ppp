<!DOCTYPE html>
<html>

<head>
	<title>Моя игра</title>
	<style>
		/* Стили для игрового поля */
		#game-board {
			width: 400px;
			height: 400px;
			border: 1px solid black;
			position: relative;
		}

		/* Стили для игровых элементов */
		.game-item {
			width: 50px;
			height: 50px;
			position: absolute;
		}

		/* Стили для игрового персонажа */
		#player {
			background-color: blue;
		}
	</style>
</head>

<body>
	<div id="game-board">
		<div id="player" class="game-item"></div>
	</div>

	<script>
		// Код JavaScript для управления игрой
        document.addEventListener("keydown", function(event) {
            var player = document.getElementById("player");
            var x = player.offsetLeft;
            var y = player.offsetTop;
            
            if (event.key === "ArrowUp") {
                // Движение вверх
                player.style.top = (y - 50) + "px";
            } else if (event.key === "ArrowDown") {
                // Движение вниз
                player.style.top = (y + 50) + "px";
            } else if (event.key === "ArrowLeft") {
                // Движение влево
                player.style.left = (x - 50) + "px";
            } else if (event.key === "ArrowRight") {
                // Движение вправо
                player.style.left = (x + 50) + "px";
            }
        });
	</script>
</body>

</html>
