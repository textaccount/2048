# 2048
game2048
<!DOCTYPE html>
<html lang="zh">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width,initial-scale=1,user-scalable=no">
    <title>2048</title>
    <link href="css/main.css" rel="stylesheet">
    <script src="js/controllerLayer.js"></script>
    <script src="js/modelLayer.js"></script>
    <script src="js/jquery-2.1.4.min.js"></script>
</head>
<body>
<header>
    <h1>2048</h1>
    <div id="newgamebutton" onclick="startGame(context)" >开始游戏</div>
    <p>score: <span id="score">0</span></p>
</header>
<div id="canvas-warp">
    <canvas id="canvas">
        你的浏览器居然不支持Canvas？！赶快换一个吧！！
    </canvas>
</div>

<script>
    var canvas = document.getElementById("canvas");
    canvas.width = game_width;
    canvas.height = game_width;
    var context = canvas.getContext("2d");

    window.addEventListener('keydown', moveKeyDown, true);


    window.onload = function(){
        startGame(context);
        $("body").bind("touchmove",function(event){
            event.preventDefault();
        });
    }

</script>
</body>
</html>
