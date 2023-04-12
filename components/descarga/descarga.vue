<template>
    <body>
        <header>
            <div class="container-header">
                <div class="logo-title">
                    <h4>EZ-FORM</h4>
                </div>
                <nav class="navigation">
                    <div class=boton-inicio>
                        <ul>
                            <li><a href="" @click="regresoInicio">Inicio</a></li>
                        </ul>
                    </div>
                </nav>
            </div>
        </header>
        <div class="container-portada">
            <div class="capa-gradient"></div>
            <div class="container-details">
                <div class="details">
                    <h1>Zona descarga</h1>
                    <p>OBTEN EZ-FORM YA!</p>
                    <a href="../../download/ezform_v4beta.apk" download="ezform_v4beta.apk"><button>Descargar</button></a>
                </div>
            </div>
        </div>
    </body>
</template>

<script>
export default{
	methods: {
        async regresoInicio () {
            this.$router.push('/')
        },
    }
}
</script>

<style scoped>
@import url(../../assets/css/descarga.css);
</style>