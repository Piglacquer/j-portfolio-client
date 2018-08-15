<template>
    <div class='header'>
        <transition-group name="slide">
            <div :key='1' v-if='headerVisible || this.scrolled' >
                <ul class='nav-items'>
                    <router-link to='/about' class='nav-link'>About</router-link>
                    <router-link to='/film' class='nav-link'>Film</router-link>
                    <router-link to='/projects' class='nav-link'>Projects</router-link>
                    <router-link to='/contact' class='nav-link'>Contact</router-link>
                </ul>
            </div>
            <div :key='2' class='hamburger'>
                <img src='../../static/Hamburger.png' v-on:click="$emit('showHeader')">
            </div>
        </transition-group>
    </div>
</template>

<script>
    export default {
        name: 'Header',
        data() {
            return{
                
            }
        },
        methods: {
            showHeader() {
                $emit('showHeader')
             },
        },
        props: {
            scrolled: Boolean,
            yScroll: Number,
            headerVisible: Boolean
        }
    }
</script>

<style scoped>
    .header {
        width: 100vw;
        background-color: #CCB796;
        position: fixed;
    }

    .slide-enter-active {
        transition: all .7s ease;
    }

    .slide-enter .slide-leave-to {
        transition: translateY(-30px);
    }

    .hamburger {
        display: flex;
        justify-content: center;
    }

    .hamburger img {
        height: 50px;
        width: 50px;
    }

    .nav-items{
        display: flex;
        flex-flow: row nowrap;
        list-style: none;
        justify-content: flex-end;
    }

    .nav-link  {
        padding-right: 10px;
        padding-top: 20px;
        font-size: 2rem;
    }
</style>