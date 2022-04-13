<template>
    <div class="w-full flex justify-between "><h1>Dashboard</h1> <a href="" @click.prevent="logout">logout</a></div>
</template>

<script>
// import env from '../environment'
export default {
    data () {
        return {

        }
    },
    methods: {
        async logout() {
            await this.$auth.logout()
            this.$router.push('/login')
            
        }
    }
}
</script>
<style scoped>
   .flex {
       display: flex;
   }
   .justify-between {
       justify-content: space-between;
   }
   .w-full {
       width: 100%;
   }
</style>
