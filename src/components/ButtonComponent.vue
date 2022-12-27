<script>
import { RouterLink } from 'vue-router';

export default {
    props: {
        title: {
            type: String,
            default: "Отправить письмо",
        } 
    },

    data() {
        return {}
    },

    methods: {}
}
</script>

<template>    
    <div class="button">
        <span>
            {{ title }}
        </span>
    </div>
</template>

<style>
.button {
    padding: 15px;
    background-color: blueviolet;
    border-radius: 20px;
}
</style>
