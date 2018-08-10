<template>
    <div class='header'>
        <transition name="slide">
            <div v-if='headerVisible || this.scrolled' >
                <ul class='nav-items'>
                    <li>First Item</li>
                    <li>Second Item</li>
                    <li>Third Item</li>
                    <li>Fourth Item</li>
                </ul>
            </div>
        </transition>
        <div class='hamburger'>
            <img src='../../static/Hamburger.png' v-on:click='showHeader'>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Header',
        data() {
            return{
                headerVisible: false
            }
        },
        methods: {
            showHeader() {
                this.headerVisible = !this.headerVisible
             },
        },
        props: {
            scrolled: Boolean,
            yScroll: Number
        }
    }
</script>

<style scoped>
    .header {
        width: 100vw;
        background-color: blue;
        position: fixed;
    }

    .slide-enter-active {
    transition: all .3s ease;
    }

    .slide-leave-active {
    transition: all .3s cubic-bezier(1.0, 0.5, 0.8, 1.0);
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

    .nav-items li {
        padding-right: 10px;
    }
</style>