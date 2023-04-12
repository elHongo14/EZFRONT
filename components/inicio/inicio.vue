<template>
    <body>
        <ul>
            <li><a @click="logoutBtn">Cerrar Sesión</a></li>
            <div class="title">
            <img class="icon" src="../../assets/css/images/icons/logo_cropped.png" alt="EZ-FORM">
                EZ-FORM
            </div>
        </ul>
        <div class="page">
            <iframe src="https://ezform.netlify.app/nuevoDoc" frameborder="0" height="720" width="100%"></iframe>
        </div>
    </body>
</template>

<script>

export default{
	methods: {
        async logoutBtn () {
            this.$router.push('/')
        },
    }
}
</script>


<style scoped>

@import url("../../assets/css/navbar.css");
</style>