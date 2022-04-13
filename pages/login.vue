<template>
    <div>login

        <button @click="login">login</button>
    </div>
</template>

<script>
export default {
    data () {
        return {

        }
    },
    methods: {
        async login () {
            await this.$auth.loginWith('laravelSanctum', {
                data: {
                    email: 'rodnie.lecera@gmail.com',
                    password: 'password'
                }
            })
            this.$router.push('/dashboard')

        }
    }   
}
</script>