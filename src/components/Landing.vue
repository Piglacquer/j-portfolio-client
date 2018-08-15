<template>
    <div id='landing'>
        <router-link to='/main'>main</router-link>
    </div>
</template>

<script>
    export default {
        name: 'Landing',
        data() {
            return{
                alive: true
            }
        },
        props: {
            
        }
    }
</script>
<style scoped>
    #landing {
        width: 100vw;
    }
</style>