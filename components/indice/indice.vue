<template>
    <body class="">
			<header id="header">
				<h1>EZ-FORM</h1>
				<nav>
					<ul>
						<li><a href="#intro" class="btn-inicio">inicio</a></li>
						<li><a href="#one" class="btn-one">sobre nosotros</a></li>
						<li><a href="#contact" class="btn-contact">contacto</a></li>
						<a @click="downloadBtn" class="btn-desc">
							descargar beta<i class=" fa fa-download"></i>
						</a>
						<a @click="loginBtn" class="btn">Iniciar Sesión</a>
					</ul>
				</nav>
			</header>
			<section id="intro" class="main style1 dark fullscreen">
				<div>
					<header>
						<h2>Bienvenidos a EZ-FORM</h2>
						<a @click="downloadBtn" class="btn-desc">
							Descargar Aplicación Beta<i class="fa fa-download"></i>
						</a>
					</header>
					<footer>
						<a href="#mobile" class="button style2 down">Ver más</a>
					</footer>
				</div>
			</section>
			<section id="mobile" class="main style2 left dark fullscreen">
				<div class="content box style2">
					<header>
						<h2>¡Descarga nuestra APP!</h2>
					</header>
					<p>
						¡EZ-FORM ahora está disponible en móviles!
						Sigue de cerca el desarrollo de nuestra aplicación móvil.
					</p>
					<a @click="downloadBtn" class="btn-desc">
						Descargar Aplicación Beta<i class="fa fa-download"></i>
					</a>
				</div>
				<a href="#one" class="button style2 down anchored">Next</a>
			</section>
			<section id="one" class="main style2 right dark fullscreen">
				<div class="content box style2">
					<header>
						<h2>¿Qué es EZ-FORM?</h2>
					</header>
					<p>EZ-FORM consiste en diseñar y desarrollar una plataforma que ayude a los profesores
						de la Universidad Tecnológica de Salamanca (UTS) en la gestión de documentos
						del sistema gestor de calidad; específicamente REDIC. El cual permitirá a los
						usuarios puedan tener una mejor manera para generar estos tipos de formatos para
						la (UTS) en los cuales dependiendo el rol que tenga el usuario podrá realizar sus
						funciones necesarias.</p>
				</div>
				<a href="#two" class="button style2 down anchored">Next</a>
			</section>
			<section id="two" class="main style2 left dark fullscreen">
				<div class="content box style2">
					<header>
						<h2>Llenado Fácil</h2>
					</header>
					<p>
						El usuario podrá tener a su disposición la información que este
						requiera para llenar de manera automática.
					</p>
				</div>
				<a href="#three" class="button style2 down anchored">Next</a>
			</section>
			<section id="three" class="main style2 right dark fullscreen">
				<div class="content box style2">
					<header>
						<h2>Guardado y edición directa desde la nube</h2>
					</header>
					<p>
						El usuario podrá guardar el archivo que
            			este esté editando desde la nube, para que de esta forma no lo esté guardando a
            			cada momento y este tenga la opción de editarlo desde la nube para no desperdiciar
            			espacio.
					</p>
				</div>
				<a href="#four" class="button style2 down anchored">Next</a>
			</section>
		<section id="four" class="main style2 left dark fullscreen">
			<div class="content box style2">
				<header>
					<h2>Guardado de Emergencia</h2>
				</header>
				<p>
					Se guardará el proceso del documento, sin la necesidad
					de estarlo guardando, esto por si surgen inconvenientes o problemas que pongan
					en riesgo el documento que se esté realizando, de esta forma el documento estará
					seguro hasta que el usuario lo de por finalizado.
				</p>
			</div>
			<a href="#contact" class="button style2 down anchored">Next</a>
		</section>
			<!--<section id="work" class="main style3 primary">
				<div class="gallery">
					<header>
						<h2>Trabajos Recientes</h2>
						<p>A continuación te dejamos los eventos más recientes que hemos cubierto en el bello
						municipio de Salamanca, Guanajuato.</p>
					</header>
						<div class="gallery poptrox-popup">
							<article class="from-left">
								<a href="images/fulls/01.jpg" class="image"><img src="images/thumbs/01.jpg" title="Vía Alta, Salamanca" alt="" /></a>
							</article>
							<article class="from-right">
								<a href="images/fulls/02.jpg" class="image"><img src="images/thumbs/02.jpg" title="New York, City" alt="" /></a>
							</article>
							<article class="from-left">
								<a href="images/fulls/03.jpg" class="image fit"><img src="images/thumbs/03.jpg" title="Air Lounge" alt="" /></a>
							</article>
							<article class="from-right">
								<a href="images/fulls/04.jpg" class="image fit"><img src="images/thumbs/04.jpg" title="Carry on" alt="" /></a>
							</article>
							<article class="from-left">
								<a href="images/fulls/05.jpg" class="image fit"><img src="images/thumbs/05.jpg" title="The sparkling shell" alt="" /></a>
							</article>
							<article class="from-right">
								<a href="images/fulls/06.jpg" class="image fit"><img src="images/thumbs/06.jpg" title="Bent IX" alt="" /></a>
							</article>
						</div>
				</div>
			</section> -->
			<section id="contact" class="main style3 secondary">
				<div class="content">
					<header>
						<h2>Contacto</h2>
						<p>¿Tienes alguna duda? ¿Algún comentario que desees hacernos? ¡Déjanos un mensaje!</p>
					</header>
						<div class="box">
						<form action="./assets/enviar.php" method="post" class="formulario">
							<div>
								<div class="field half"><input type="text" class="name" placeholder="Nombre"  id="name"/></div>
								<div class="field half"><input type="email" class="email" placeholder="Email" id="email"/></div>
								<div class="field half"><textarea type="message" placeholder="Mensaje" rows="6" id="message"></textarea></div>
								<button type="button" onclick="validarFormulario()">Enviar</button>
							</div>
						</form>
					</div>
				</div>
			</section>
			<footer id="footer">
				<ul class="menu">	
						<li><a href="#" class="brands fa-twitter icon"></a></li>
						<li><a href="#" class="brands fa-facebook-f icon"></a></li>
						<li><a href="#" class="brands fa-instagram icon"></a></li>
					</ul>
					<ul class="menu">
						<li>&copy; EZ-FORM</li><li>Todos los derechos reservados</li>
					</ul>
			</footer>
		</body>
</template>


<!-- <script src="../../assets/js/jquery.min.js"></script>
<script src="../../assets/js/jquery.poptrox.min.js"></script>
<script src="../../assets/js/jquery.scrolly.min.js"></script>
<script src="../../assets/js/jquery.scrollex.min.js"></script>
<script src="../../assets/js/browser.min.js"></script>
<script src="../../assets/js/breakpoints.min.js"></script>
<script src="../../assets/js/util.js"></script>
<script src="../../assets/js/main.js"></script>  -->

<script>

// import $ from '../../assets/js/util'
// import $ from '../../assets/js/main'
export default{
	methods: {
        async loginBtn () {
            this.$router.push('/user')
        },

		async downloadBtn () {
            // this.$router.push('https://ezform.netlify.app/zona-descarga')
			location.href = 'https://ezform.netlify.app/zona-descarga';
        },
    }
}
</script>

<style scoped>
@import url(../../assets/css/main.css);
</style>