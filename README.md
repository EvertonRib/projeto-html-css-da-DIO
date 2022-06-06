# projeto-html-css-da-DIO
Projeto utilizando técnicas do HTML e CSS.
------------------------------------------------------------
---HTML--
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="./style.css">
    <title>Document</title>
</head>
<body>
    <header class="header-wrapper">
        <div class="header">
            <div class="checkbox-container">
                <div class="checkbox-wrapper">
                    <input type="checkbox" id="toggle">
                    <label class="checkbox" for="toggle">
                        <div class="trace"></div>
                        <div class="trace"></div>
                        <div class="trace"></div>
                    </label>
                    <div class="menu"></div>
                    <nav class="menu-items">
                    <ul>
                        <li>
                            <a href="#">Home</a>
                        </li>
                        <li>
                            <a href="#">Sobre</a>
                        </li>
                        <li>
                            <a href="#">Projetos</a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
        <h1>Everton Ribeiro</h1>
        <h2>Front-end Developer</h2>
        <div class="social-media">
            <a href="#">LinkedIn</a>
            <a href="#">Github</a>
        </div>
    </header>
    <main class="container">
        <div class="card-container">
            <div class="card-text">
                O GitHub é uma das plataformas mais comentadas e valorizadas na área de desenvolvimento e engenharia de software. Seus recursos voltados para as demandas de atualização de código tornam a visualização dos processos mais simples e acessível. Além disso, ter uma conta no GitHub é uma ótima oportunidade de mostrar seu trabalho.
                Como um sistema de controle de versão, o GitHub sempre foi uma ferramenta comum no dia a dia de quem trabalha no segmento. Nos últimos anos, com o avanço do digital e a mudança das relações de trabalho, o GitHub passou a ter importância ainda maior, não só na rotina de atuação, mas também na hora de se posicionar no mercado.
            </div>
            <div class="card">
                <div class="card-wrapper">
                    <h2>Github</h2>
                    <p>Veja meus projetos!</p>
                </div>
            </div>
        </div>
        <div class="card-container">            
            <div class="card">
                <div class="card-wrapper">
                    <h2>LinkedIn</h2>
                    <p>Acompanhe minha carreira!</p>
                </div>
            </div>
            <div class="card-text">
                O LinkedIn é a mais famosa e maior rede social profissional, focada em gerar conexões e relacionamentos. Nela os profissionais podem criar seus currículos, buscar empregos e fazer contato com pessoas do mundo inteiro. Já as empresas conseguem buscar candidatos ideais para suas vagas e perfis de clientes em potencial.
            </div>
        </div>
        <div class="card-container">
            <div class="card-text">
                Instagram é uma rede social visual, criativa e interativa. Possibilita o compartilhamento de imagens e vídeos de curta duração diretamente do aplicativo de celular. Nele, também é possível seguir usuários, curtir, comentar e compartilhar as publicações.
            </div>
            <div class="card">
                <div class="card-wrapper">
                    <h2>Instagram</h2>
                    <p>Meu dia-a-dia!</p>
                </div>
            </div>
        </div>
    </main>
    <footer class="footer">
        Feito por Everton Ribeiro
    </footer>
</body>
</html>
  
  --------------------------------------------------------------------------------------
  --CSS--
  
  @import url('https://fonts.googleapis.com/css2?family=Amatic+SC&display=swap');

body {
	padding: 0;
	margin: 0;
	color: #ffffff;
	font-family: 'amatic sc', sans-serif;
}

/* HEADER */

.header-wrapper {
	height: 100vh;
	width: 100%;
	background: linear-gradient(-45deg, #050404, #2e1c2b, #4a1942, #893168);
	background-size: 400% 400%;
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
	position: relative;
	animation: backgroundTransition 8s ease-in-out infinite;
}

h1 {
	text-transform: uppercase;
	letter-spacing: 4px;
}

h2 {
	text-transform: uppercase;
	letter-spacing: 4px;
}

.social-media {
	margin-top: 1rem;
	display: flex;
}

.social-media a {
	text-decoration: none;
	color: #ffffff;
	font-size: 24px;
	padding: 1rem 4rem;
	border: 1px solid #ffffff;
	min-width: 4rem;
	display: flex;
	justify-content: center;
	align-items: center;
	transition: .5s cubic-bezier(0.55, 0.025, 0.675, 0.97);
}

a:hover {
	color: #2E1C2B;
	background-color: #ffffff;
}

@keyframes backgroundTransition {
	0% {
		background-position: 0% 80%;
	}
	50% {
		background-position: 80% 100%;
	}
	100% {
		background-position: 0% 90%;
	}
}

/* MENU HAMBURGUER */

.checkbox-container {
	display: flex;
	justify-content: center;
	align-items: center;
}

.checkbox {
	height: 100px;
	width: 100px;
	position: absolute;
	top: 0;
	right: 0;
	display: flex;
	justify-content: center;
	cursor: pointer;
	z-index: 9999;
	transition: 400ms ease-in-out 0;
}

.checkbox .trace {
	width: 50px;
	height: 2px;
	background-color: #ffffff;
	position: absolute;
	border-radius: 4px;
	transition: 0.5s ease-in-out;
}

.checkbox .trace:nth-child(1) {
	top: 26px;
	transform: rotate(0);
}

.checkbox .trace:nth-child(2) {
	top: 46px;
	transform: rotate(0);
}

.checkbox .trace:nth-child(3) {
	top: 66px;
	transform: rotate(0);
}

#toggle {
	display: none;
}

/*MENU */

.menu {
	position: absolute;
	top: 28px;
	right: 30px;
	background-color: rgb(255, 255, 255);
	height: 40px;
	width: 40px;
	border-radius: 50%;
	box-shadow: 0px 0 px 0px 0px #ffffff;
	z-index: -1;
	transition: 400ms ease-in-out 0s;
}

.menu-items {
	position: fixed;
	top: 0;
	left: 0;
	width: 100%;
	height: 100vh;
	display: flex;
	justify-content: center;
	align-items: center;
	z-index: 2;
	opacity: 0;
	visibility: hidden;
	transition: 400ms ease-in-out 0s;
}

.menu-items ul {
	list-style-type: none;
}

.menu-items ul li a {
	margin: 10px 0;
	color: #2E1C2B;
	text-decoration: none;
	text-transform: uppercase;
	letter-spacing: 4px;
	font-size: 40px;
}

/* ANIMAÇÃO DO MENU */

#toggle:checked + .checkbox .trace:nth-child(1) {
	transform: rotate(45deg);
	background-color: #2E1C2B;
	top: 47px;
}

#toggle:checked + .checkbox .trace:nth-child(2) {
	transform: translateX(-100px);
	width: 30px;
	visibility: hidden;
	opacity: 0;
}

#toggle:checked + .checkbox .trace:nth-child(3) {
	transform: rotate(-45deg);
	background-color: #2E1C2B;
	top: 48px;
}

#toggle:checked + .checkbox {
	background-color: #ffffff;
}

#toggle:checked ~.menu {
	box-shadow: 0px 0px 0px 100vmax #ffffff;
	z-index: 1;
}

#toggle:checked ~.menu-items {
	visibility: visible;
	opacity: 1;
}

/*CARDS*/

.container {
	width: 100%;
	height: auto;
	display: flex;
	flex-direction: column;
	justify-content: space-between;
	align-items: center;
	margin: 3rem 0;
}

.card-container {
	display: flex;
	align-items: center;
	justify-content: space-evenly;
	width: 90%;
}

.card {
	height: 300px;
	width: 400px;
	margin: 3rem 0 0 0;
	background-image: url('./Des1.jpg');
	background-position: center;
	background-repeat: no-repeat;
	background-size: cover;
	display: flex;
	justify-content: center;
	align-items: center;
	filter: grayscale(0.5);
	color: #ffffff;
	cursor: pointer;
	transition: 0.3s;
}

.card-text {
	width: 40%;
	font-family: sans-serif;
	letter-spacing: 1px;
	color: rgb(109, 109, 109);
}

.card-wrapper {
	text-align: center;
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
	position: relative;
}

.card-wrapper::before {
	content: '';
	position: absolute;
	height: 100px;
	width: 100px;
	display: block;
	border: 1px solid #ffffff;
	opacity: 0;
	transition: 0.3s;
}

.card-wrapper h2 {
	font-size: 40px;
	text-transform: uppercase;
	letter-spacing: 4px;
	margin: 0;
	transition: 0.3s;
}

.card-wrapper p {
	font-size: 0;
	visibility: hidden;
	opacity: 0;
	font-weight: bold;
	text-transform: uppercase;
	transition: 0.3s;
}

.card:hover > .card-wrapper::before {
	height: 250px;
	opacity: 1;
	width: 350px;
}

.card:hover > .card-wrapper p {
	font-size: 14px;
	opacity: 1;
	visibility: visible;
}

/* FOTTER */

.footer {
	height: 100px;
	width: 100%;
	display: flex;
	justify-content: center;
	align-items: center;
	background-color: #2E1C2B;
}

/* RESPONSIVO */

@media (max-width: 800px) {
	.social-media {
		display: flex;
		flex-direction: column;
	}

	.container {
		margin-top: 0;
	}

	.card-container {
		flex-direction: column;
	}

	.container .card-container:nth-child(1),
	.container .card-container:nth-child(3) {
		flex-direction: column-reverse;
	}

	.card {
		height: 250px;
		width: 250px;
	}

	.card-text {
		width: 90%;
		margin-top: 2rem;
		text-align: center;
	}

	.card:hover > .card-wrapper::before {
		height: 190px;
		width: 190px;
	}
}
