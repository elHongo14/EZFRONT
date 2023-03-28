<template>
    <body>
        <section>
        <div class="loginForm">
            <div class="logo">
                <img src="../../assets/images/logo.png" alt="">
            </div>
            <div class="form">
                <form action="">
                    <h2>Iniciar Sesión</h2>
                    <v-form ref="formLogin">
                        <div>
                            <v-text-field class="loginField"
                              label="Correo Institucional" 
                              placeholder="Correo Institucional"
                              v-model="correoElectronico"
                              :rules="validarCorreo"/>
                        </div>
                    <div>
                        <v-text-field class="loginField"
                              label="Contraseña" 
                              placeholder="Contraseña"
                              v-model="password"
                              :rules="validarPassword"/>
                    </div>
                    <div class="casillaRecord">
                        <label for=""><input type="checkbox">Recuérdame</label>
                    </div>
                    <a href="#">¿Problemas con tu cuenta?</a>
                    </v-form>
                </form>
            <div class="btn">
                        <button @click="loginBackend">ACCEDER</button>
                    </div>
            </div>
        </div>
        </section>
    </body>
</template>

<script type="module" src="https://unpkg.com/ionicons@5.5.2/dist/ionicons/ionicons.esm.js"></script>
<script nomodule src="https://unpkg.com/ionicons@5.5.2/dist/ionicons/ionicons.js"></script>

<script>
export default {
    data() {
        return {
            correoElectronico: '',
            validarCorreo: [
            v => !v || /^\w+([.-]?\w+)*@\w+([.-]?\w+)*(\.\w{2,3})+$/.test(v) || 'Introduce un correo válido.'
            ],
            password:'',
            validarPassword: [
                value => value.length >= 6 || 'Introduce mínimo 6 caractéres'
            ]
        }
    },
    methods: {
        async loginBackend () {
            const valid = this.$refs.formLogin.validate()
            if (valid) {
                const sendData = {
                    email: this.correoElectronico,
                    password: this.password
                }
                await this.$auth.loginWith('local', {
                    data: sendData
                }).then(async (res) => {
                    console.log('respuesta del back:', res)
                    if (res.data.alert !== 'Correo no registrado en la base de datos'){
                        if (res.data.alert !== 'Contraseña incorrecta') {
                            this.$router.push('/inicio')
                        } else {
                            alert('Contraseña incorrecta!!')
                        }
                    } else {
                        alert('Correo no registrado en la base de datos')
                    }
                }).catch((error) => {
                    console.log('error: ', error)
                })
            }else {
                alert('Introduce los datos correctamente.')
            }
        }
    }
}
</script>

<style scoped>
@import url('../../assets/css/login2.css');
</style>