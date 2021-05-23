<template>
    <div class="sidebar">
        <div class="sidebar-backdrop" @click="closeSidebarPanel" v-if="isPanelOpen"></div>
            <transition name="slide">
            <div v-if="isPanelOpen"
                 class="sidebar-panel">
                <slot></slot>
            </div>
            </transition>
    </div>
</template>
<script>
import { store, mutations } from '@/assets/store.js'

export default {
    methods: {
        closeSidebarPanel: mutations.toggleNav
    },
    computed: {
        isPanelOpen() {
            return store.isNavOpen
        }
    }
}
</script>
<style scoped>
.slide-enter-active,
.slide-leave-active
{
    transition: transform 0.5s ease;
}

.slide-enter,
.slide-leave-to {
    transform: translateX(-100%);
    transition: all 500ms ease-in 0s
}

.sidebar-backdrop {

    width: 100vw;
    height: 100vh;
    position: fixed;
    top: 0;
    left: 0;
    cursor: pointer;
}

.sidebar-panel {
    overflow-y: auto;
    background-color: #373737;
    position: fixed;
    left: 0;
    top: 0;
    height: 100vh;
    z-index: 999;
    padding: 3rem 20px 2rem 20px;
    width: 300px;
    border-right:1px solid#fff;
}
</style>