@import url('https://fonts.googleapis.com/css?family=Montserrat:100,100i,200,200i,300,300i,400,400i,500,500i,600,600i,700,700i,800,800i,900,900i');

body{
	font-family: 'Montserrat', sans-serif;
	font-weight: 300;
	font-size: 15px;
	line-height: 1.7;
	color: #c4c3ca;
	background-color: #1f2029;
	overflow-x: hidden;
	-webkit-transition: all 300ms linear;
	transition: all 300ms linear;
}

/* #Primary style
================================================== */

.section {
    position: relative;
	width: 100%;
	display: block;
}
.over-hide{
	overflow: hidden;
}
.full-height {
	height: 0.1vh;
}

/* #Navigation
================================================== */
 
.cd-header{
    position: fixed;
	width:100%;
	top:0;
	left:0;
	z-index:100;
} 
.header-wrapper{
    position: relative;
	width: calc(100% - 100px);
	margin-left: 90px	;
} 
.nav-but-wrap{ 
	position: relative;
	display: inline-block;
	float: right;
	padding-left: 15px;
	padding-top: 15px;
	margin-top: 26px;
	transition : all 0.3s ease-out;
}
.menu-icon {
	height: 30px;
	width: 30px;
	position: relative;
	z-index: 2;
	cursor: pointer;
	display: block;
}
.menu-icon__line {
	height: 2px;
	width: 30px;
	display: block;
	background-color: #fff;
	margin-bottom: 7px;
	cursor: pointer;
	-webkit-transition: background-color .5s ease, -webkit-transform .2s ease;
	transition: background-color .5s ease, -webkit-transform .2s ease;
	transition: transform .2s ease, background-color .5s ease;
	transition: transform .2s ease, background-color .5s ease, -webkit-transform .2s ease;
}
.menu-icon__line-left {
	width: 16.5px;
	-webkit-transition: all 200ms linear;
	transition: all 200ms linear;
}
.menu-icon__line-right {
	width: 16.5px;
	float: right;
	-webkit-transition: all 200ms linear;
	-moz-transition: all 200ms linear;
	-o-transition: all 200ms linear;
	-ms-transition: all 200ms linear;
	transition: all 200ms linear;
}
.menu-icon:hover .menu-icon__line-left,
.menu-icon:hover .menu-icon__line-right {
	width: 30px;
}
.nav {
	position: fixed;
	z-index: 98;
}
.nav:before, .nav:after {
	content: "";
	position: fixed;
	width: 100vw;
	height: 100vh;
	background: #265df2;
	border-bottom-left-radius: 200%;
	z-index: -1;
	-webkit-transition: -webkit-transform cubic-bezier(0.77, 0, 0.175, 1) 0.6s, border-radius linear 0.8s;
	transition: -webkit-transform cubic-bezier(0.77, 0, 0.175, 1) 0.6s, border-radius linear 0.8s;
	transition: transform cubic-bezier(0.77, 0, 0.175, 1) 0.6s, border-radius linear 0.8s;
	transition: transform cubic-bezier(0.77, 0, 0.175, 1) 0.6s, -webkit-transform cubic-bezier(0.77, 0, 0.175, 1) 0.6s, border-radius linear 0.8s;
	-webkit-transform: translateX(100%) translateY(-100%);
          transform: translateX(100%) translateY(-100%);
}
.nav:after {
	background: rgba(9,9,12,1);
	-webkit-transition-delay: 0s;
          transition-delay: 0s;
}
.nav:before {
	-webkit-transition-delay: .2s;
          transition-delay: .2s;
}
.nav__content {
	position: fixed;
	visibility: hidden;
	top: 50%;
	margin-top: 20px;
	-webkit-transform: translate(0%, -50%);
          transform: translate(0%, -50%);
	width: 100%;
	text-align: center;
}
.nav__list {
	position: relative;
	padding: 0;
	margin: 0;
	z-index: 2;
}
.nav__list-item {
	position: relative;
	display: block;
	-webkit-transition-delay: 0.8s;
          transition-delay: 0.8s;
	opacity: 0;
	text-align: center;
	color: #fff;
	overflow: hidden; 
	font-family: 'Montserrat', sans-serif;
	font-size: 40px;
	font-weight: 900;
	line-height: 1.15;
	letter-spacing: 3px;
	-webkit-transform: translate(100px, 0%);
          transform: translate(100px, 0%);
	-webkit-transition: opacity .2s ease, -webkit-transform .3s ease;
	transition: opacity .2s ease, -webkit-transform .3s ease;
	transition: opacity .2s ease, transform .3s ease;
	transition: opacity .2s ease, transform .3s ease, -webkit-transform .3s ease;
	margin-top: 0;
	margin-bottom: 0;
}
.nav__list-item a{ 
	position: relative;
	text-decoration: none;
	color: rgba(255,255,255,0.6);
	overflow: hidden; 
	cursor: pointer;
	padding-left: 5px;
	padding-right: 5px;
	font-weight: 900;
	z-index: 2;
	display: inline-block;
	text-transform: uppercase;
    -webkit-transition: all 200ms linear;
    transition: all 200ms linear; 
}
.nav__list-item a:after{ 
	position: absolute;
	content: '';
	top: 50%;
	margin-top: -2px;
	left: 50%;
	width: 0;
	height: 0;
	opacity: 0;
	background-color: #265df2;
	z-index: 1;
    -webkit-transition: all 200ms linear;
    transition: all 200ms linear; 
}
.nav__list-item a:hover:after{ 
	height: 4px;
	opacity: 1;
	left: 0;
	width: 100%;
}
.nav__list-item a:hover{
	color: rgba(255,255,255,1);
}
.nav__list-item.active-nav a{
	color: rgba(255,255,255,1);
}
.nav__list-item.active-nav a:after{ 
	height: 4px;
	opacity: 1;
	left: 0;
	width: 100%;
}
body.nav-active .nav__content {
	visibility: visible;
}
body.nav-active .menu-icon__line {
	background-color: #fff;
	-webkit-transform: translate(0px, 0px) rotate(-45deg);
          transform: translate(0px, 0px) rotate(-45deg);
}
body.nav-active .menu-icon__line-left {
	width: 15px;
	-webkit-transform: translate(2px, 4px) rotate(45deg);
          transform: translate(2px, 4px) rotate(45deg);
}
body.nav-active .menu-icon__line-right {
	width: 15px;
	float: right;
	-webkit-transform: translate(-3px, -3.5px) rotate(45deg);
          transform: translate(-3px, -3.5px) rotate(45deg);
}
body.nav-active .menu-icon:hover .menu-icon__line-left,
body.nav-active .menu-icon:hover .menu-icon__line-right {
	width: 15px;
}
body.nav-active .nav {
	visibility: visible;
}
body.nav-active .nav:before, body.nav-active .nav:after {
	-webkit-transform: translateX(0%) translateY(0%);
          transform: translateX(0%) translateY(0%);
	border-radius: 0;
}
body.nav-active .nav:after {
	-webkit-transition-delay: .1s;
          transition-delay: .1s;
}
body.nav-active .nav:before {
	-webkit-transition-delay: 0s;
          transition-delay: 0s;
}
body.nav-active .nav__list-item {
	opacity: 1;
	-webkit-transform: translateX(0%);
          transform: translateX(0%);
	-webkit-transition: opacity .3s ease, color .3s ease, -webkit-transform .3s ease;
	transition: opacity .3s ease, color .3s ease, -webkit-transform .3s ease;
	transition: opacity .3s ease, transform .3s ease, color .3s ease;
	transition: opacity .3s ease, transform .3s ease, color .3s ease, -webkit-transform .3s ease;
}
body.nav-active .nav__list-item:nth-child(0) {
	-webkit-transition-delay: 0.7s;
          transition-delay: 0.7s;
}
body.nav-active .nav__list-item:nth-child(1) {
	-webkit-transition-delay: 0.8s;
          transition-delay: 0.8s;
}
body.nav-active .nav__list-item:nth-child(2) {
	-webkit-transition-delay: 0.9s;
          transition-delay: 0.9s;
}
body.nav-active .nav__list-item:nth-child(3) {
	-webkit-transition-delay: 1s;
          transition-delay: 1s;
}
body.nav-active .nav__list-item:nth-child(4) {
	-webkit-transition-delay: 1.1s;
          transition-delay: 1.1s;
}
body.nav-active .nav__list-item:nth-child(5) {
	-webkit-transition-delay: 1.2s;
          transition-delay: 1.2s;
}
body.nav-active .nav__list-item:nth-child(6) {
	-webkit-transition-delay: 1.3s;
          transition-delay: 1.3s;
}
body.nav-active .nav__list-item:nth-child(7) {
	-webkit-transition-delay: 1.4s;
          transition-delay: 1.4s;
}
body.nav-active .nav__list-item:nth-child(8) {
	-webkit-transition-delay: 1.5s;
          transition-delay: 1.5s;
}
body.nav-active .nav__list-item:nth-child(9) {
	-webkit-transition-delay: 1.6s;
          transition-delay: 1.6s;
}
body.nav-active .nav__list-item:nth-child(10) {
	-webkit-transition-delay: 1.7s;
          transition-delay: 1.7s;
}

 :root {
	--bg: hsl(242, 19%, 13%);
	--color: #15fda0;
	--buttonBg: hsl(242, 19%, 15%);
	--buttonText: hsl(217, 89%, 58%);
	--buttonBg_hover: hsl(217, 89%, 51%);
	--buttonText_hover: hsl(242, 19%, 10%);
}

* {
	box-sizing: border-box;
}

body {
	background-color: var(--bg);
	margin: 0;
	

}
.main {
	margin: 7% 15% 0 15%;
	display: grid;
	grid-auto-rows: minmax(100px, auto);
}
.ssaa {
width: 90%;

	
	margin: 4% 4% 4% 5%;
	display: grid;
	grid-auto-rows: minmax(100px, auto);
}
.left {
	color: var(--color);
	font-size: 1.1rem;
}
.ssaa{
	color: var(--color);
	background-color: hsl(242, 19%, 16%);
	box-shadow: 0 4px 6px 0 rgba(0, 0, 0, 0.15), 0 6px 12px 0 rgba(0, 0, 0, 0.15);
	outline: none;
	border:1px solid #265df2;
	height: auto;
	padding: 20px 0 20px 40px;
	line-height: 1.6;
	font-size: 1.25rem;
}

.left,
.ssaa {
	display: block;
	border-radius: 5px;
	grid-gap: 40px;
}

button {
width: 100%;
	
}
a{
				 text-decoration: none;
				 color: var(--buttonText);
}
button{
  --success-opacity: 0;
  position: relative;  
	padding: 5px;
	font-size: 1.1rem;
	color: var(--buttonText);
	background: var(--buttonBg);
	box-shadow: 0 4px 6px 0 rgba(0, 0, 0, 0.15), 0 6px 12px 0 rgba(0, 0, 0, 0.15);
	font-weight: 500;
	border: none;
	border-radius: 5px;
}

button span {
  opacity: var(--text-opacity);
}
button span.success {

  position: absolute;
  left: 0;
  right: 0;
  top: 8px;
 
  opacity: var(--success-opacity);
  color: red;
}


.pulse {
	animation: pulse 200ms ease-in-out 2 alternate;
	color: hsla(217, 89%, 73%, 1);
}
@keyframes pulse {
	from {
		transform: scale(1);
	}
	
	to {
		transform: scale(1.1);
	}
}
@media screen and (min-width: 3000px) {
	.main,
	button {
		grid-template-columns: repeat(2, 1fr);
	}
}
.qqwwq{
	text-align: center;		
									font-size: 20px;
	margin: 0;
	padding: 20px 40px;
	color: red;
	background-color: hsl(242, 19%, 10%);
	box-shadow: 0 4px 6px 0 rgba(0, 0, 0, 0.15), 0 6px 12px 0 rgba(0, 0, 0, 0.15);
	font-weight: 900;
}



