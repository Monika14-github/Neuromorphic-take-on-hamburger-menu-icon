# Neuromorphic-take-on-hamburger-menu-icon
.....html.....
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>repl.it</title>
    <link href="style.css" rel="stylesheet" type="text/css" />
  </head>
  <body>
    <script src="script.js"></script>
    <div id="neuburger">
	<div class="line"></div>
	<div class="line"></div>
	<div class="line"></div>
</div>
  </body>
</html>
......css......
*,
*::before,
*::after {
	box-sizing: border-box;
}
body {
	display: flex;
	justify-content: center;
	align-items: center;
	background-color: #E3E3E3;
	height: 100vh;
	margin: 0;
}
#neuburger {
	height: 160px;
	width: 200px;
	display: flex;
	flex-direction: column;
	justify-content: space-around;
	align-items: center;
	cursor: pointer;
}
.line.closed {
	transition: box-shadow .5s ease-out;
	box-shadow: none!important;
}
.line.disappear {
	transition: box-shadow .5s ease-out;
}
.line {
	transition: box-shadow .1s ease-out;
	height: 15%;
	width: 80%;
	border-radius: 100px;
	box-shadow:
		-.3em -.2em 1em #fff,
		inset .4em .5em .9em #E3E3E375,
		.3em .2em .5em #88888890,
		inset -.4em -.5em .9em #E3E3E390;
}
#neuburger:hover .line:not(.closed) {
	box-shadow:
		-.3em -.2em 1em #fff,
		inset .4em .5em .9em #ddd,
		.3em .2em .5em #88888890,
		inset -.4em -.5em .9em #ddd;
}
#neuburger:active .line:not(.closed) {
	box-shadow:
		-.3em -.2em 1em #fff,
		inset .4em .5em .9em #aaaaaa35,
		.3em .2em .5em #88888850,
		inset -.4em -.5em .9em #f2f2f2;
}
