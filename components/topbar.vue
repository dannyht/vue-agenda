<template>
    <div class="topbar d-flex">
        <a href="#news" class="d-flex justify-content-start">
            <font-awesome-icon :icon="['fas', 'bars']"/>
        </a>
        <a href="#about" class="d-flex justify-content-end">
            <font-awesome-icon :icon="['fas', 'user']"/>
        </a>
    </div>  
</template>

<script>
import { defineComponent } from '@vue/composition-api'

export default defineComponent({
    setup() {
        
    },
})
</script>

<style scoped>
    .topbar {
        overflow: hidden;
        background-color: #333;
    }

    .topbar a {
        float: left;
        color: #f2f2f2;
        text-align: center;
        padding: 14px 16px;
        text-decoration: none;
        font-size: 17px;
    }

    .topbar a:hover {
        background-color: #ddd;
        color: black;
    }

    .topbar a.active {
        background-color: #04AA6D;
        color: white;
    }
</style>
