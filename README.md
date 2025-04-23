<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <link rel="preconnect" href="https://fonts.googleapis.com">
        <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
        <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400..900&family=DM+Serif+Display:ital@0;1&family=Dancing+Script:wght@400..700&family=Playfair+Display:ital,wght@0,400..900;1,400..900&family=Quicksand:wght@300..700&display=swap" rel="stylesheet">
        <link rel="stylesheet" href="love.css">
        <title>LOVE</title>
    </head>
    <body>
        <p class="instruction">Chạm vô cái trái tym ở dưới này đi Pé !</p>
        <div class="container">
            <label>
            <div class="heart">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/68/Red-Heart-vector-2731436.svg/640px-Red-Heart-vector-2731436.svg.png"></img>
            </div>
            <input id="messageState" type="checkbox" style="display:none"/>
            </label>
            <div class="message">
                <h1 style="font-family: Cinzel, serif; font-size: 40px; letter-spacing: 1.2px;">Gửi _huyenvy_!</h1>
                <p> 
                    <span>
                        &emsp; Những lời sau đây em muốn nói với chị, à không là anh muốn nói với em. Em trong mắt anh là một cô gái vô cùng toả sáng, toả sáng đến mức anh không nghĩ lời tỏ tình của anh được em đồng ý. Khoảng thời gian được làm việc tiếp xúc với em làm anh cảm thấy rất thoải mái như thể chẳng thể nào khó chịu khi hôm ấy được gặp em.
                    </span>
                    <br> <br>
                    <span>
                        &emsp; Cụ thể là hôm nào anh bắt đầu thích em thì anh không biết được, nhưng từ hôm mà anh cảm thấy sợ khi nghĩ đến nếu chàng trai khác có thể dành được sự chú ý của em thì anh biết mình đã yêu em mất rồi. Mặc dù ở bên ngoài những lời như vậy với anh rất khó để nói cho em nghe, nhưng những sự chú ý hay cả ánh mắt của anh đều hướng về em. Cảm ơn em vì đã đồng ý làm bạn gái anh, tuy hôm tỏ tình của anh em chẳng còn bất ngờ nhưng mà khoảng thời gian sắp tới anh sẽ cố gắng tạo bất ngờ cho em nhiều hơn. Sắp tới mong cả hai giúp đỡ nhau nhiều hơn.
                    </span>      
                </p>
                <br>
                <div class="sincere">
                    <p style="font-weight: bold;"> Người gửi.!</p>
                    <p>_ntienn_</p>
                 </div>
            </div>
        </div>
        
        <script src="jquery.js"></script>
        <script src="jquery2.1.js"></script>
        <script defer src="love.js"></script>
    </body>
</html>

*{
	box-sizing: border-box;
}

h1,
p 
{
	font-family: "Quicksand";
  font-optical-sizing: auto;
}

h1 
{
	font-weight: 200;
}

body 
{
    margin: 0px;
    background-image: url('images/huyenvy.jpeg'); /* Đường dẫn đến ảnh nền */
    background-size: cover; /* Đảm bảo ảnh phủ toàn bộ màn hình */
    background-position: center; /* Căn giữa ảnh nền */
    background-repeat: no-repeat; /* Không lặp lại ảnh */
    background-attachment: fixed; /* Ảnh nền cố định khi cuộn */
}

.instruction
{
	position: absolute;
	font-size: 2.4rem;
	color: rgba(255, 0, 0, 0.554);
	top: 36%;
	left: 50%;
	transform: translate(-50%, -50%);
	font-weight: bold;
}

.container 
{
	position: relative;
	width: 100%;
	height: 100vh;
	overflow: hidden;
}

.heart 
{
	position: absolute;
	left: 50%;
	top: 50%;
	text-align: center;
	transform: translate(-50%, -50%);
	transition: transform 2s;
	z-index: 1;
	cursor: pointer;
}

.heart > img 
{
	width: 200px;
	height: auto;

	animation-name: beat;
	animation-duration: 2s;
	animation-timing-function: ease-in-out;
	animation-iteration-count: infinite;
	animation-play-state: running;
}

.message 
{
	padding: 25px;
	background-color: #eee;
	font-family: "Quicksand", serif;
  font-optical-sizing: auto;
	font-size: clamp(16px, 10vw, 17px);
	text-align: justify;
	line-height: 1.5em;
	width: 80%;
	max-width: 550px;
	height: 78%;
	position: absolute;
	left: 50%;
	top: 50%;
	transform: translate(-50%, -50%);
	z-index: 0;

	animation-name: openmsg;
	animation-duration: 2s;
	animation-timing-function: linear;
	animation-play-state: paused;
	animation-fill-mode: forwards;
	box-shadow: 0 10px 20px rgba(0, 0, 0, 0.19), 0 6px 6px rgba(0, 0, 0, 0.23);
	border-radius: 5px;
	overflow: scroll;
	scrollbar-width: none;
}
 
.message .sincere
{
	text-align: left;
	font-family: "Cinzel, serif";
	font-size: 14px;
	line-height: 1.2em;
}

.message .sincere p
{
	margin: 0;
}

@keyframes beat 
{
	0% {
		width: 50px;
	}
	25% {
		width: 58px;
	}
	30% {
		width: 50px;
	}
	50% {
		width: 45px;
	}
	60% {
		width: 50px;
	}
	75% {
		width: 58px;
	}
	100% {
		width: 50px;
	}
}

@keyframes openmsg {
	0% {
		height: 0px;
		padding: 0px 20px;
	}
	100% {
		height: 75%;
		padding: 20px 20px;
	}
}

@keyframes heartMove {
	0% {
		top: 50%
	}
	100% {
		top: 85%;
		transform: translate(-50%, 0);
	}
}

.openNor {
	animation-direction: normal;
	animation-play-state: running;
}

.closeNor {
	animation-direction: reverse;
	animation-play-state: running;
}

.no-anim {
	animation: none;
}

.closed {
	height: 0px;
	padding: 0px 20px;
}

.bottom {
	bottom: 5px;
}

.openHer {
	animation-name: heartMove;
	animation-duration: 2s;
	animation-timing-function: linear;
	animation-play-state: running;
	animation-fill-mode: forwards;
}

.closeHer {
	animation-name: heartMove;
	animation-duration: 2s;
	animation-timing-function: linear; 
	animation-play-state: running;
	animation-direction: reverse;
	animation-fill-mode: forwards;
}

.beating > img {
	animation-name: beat;
	animation-duration: 2s;
	animation-timing-function: ease-in-out;
	animation-iteration-count: infinite;
	animation-play-state: running;
}

.openedHer {
	top: 85%;
	transform: translate(-50%, 0);
}
$("#messageState").on("change", (x) => 
	{
	$(".message").removeClass("openNor").removeClass("closeNor");
	if ($("#messageState").is(":checked")) 
	{
		$(".message").removeClass("closed").removeClass("no-anim").addClass("openNor");
		$(".heart").removeClass("closeHer").removeClass("openedHer").addClass("openHer");
		$(".container").stop().animate({"backgroundColor": "#f48fb1"}, 2000);
		console.log("Abrindo");
	} 
	else 
	{
		$(".message").removeClass("no-anim").addClass("closeNor");
		$(".heart").removeClass("openHer").removeClass("openedHer").addClass("closeHer");
		$(".container").stop().animate({"backgroundColor": "#fce4ec"}, 2000);
		console.log("fechando");
	}
});

$(".message").on('webkitAnimationEnd oanimationend msAnimationEnd animationend', function(e) 
{
	console.log("Animation End");
	if ($(".message").hasClass("closeNor"))
		$(".message").addClass("closed");
	$(".message").removeClass("openNor").removeClass("closeNor").addClass("no-anim");
});

$(".heart").on('webkitAnimationEnd oanimationend msAnimationEnd animationend', function(e) 
{
	console.log("Animation End");
	if (!$(".heart").hasClass("closeHer"))
		$(".heart").addClass("openedHer").addClass("beating");
	else
		$(".heart").addClass("no-anim").removeClass("beating");
	$(".heart").removeClass("openHer").removeClass("closeHer");
});
