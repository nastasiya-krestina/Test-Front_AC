<script>
//import { RouterLink } from 'vue-router';

export default {
    props: {
        title: {
            type: String,
            default: "Отправить письмо",
        },

        width: {
            type: [Number, String],
            default: 30
        },

        height: {
            type: [Number, String],
            default: 30
        },

        disabled: {
            type: Boolean,
            default: false,
        },

        primary: {
            type: Boolean,
            default: false,
        },

        secondary: {
            type: Boolean,
            default: false,
        },

        warning: {
            type: Boolean,
            default: false,
        },

        info: {
            type: Boolean,
            default: false,
        },

        danger: {
            type: Boolean,
            default: false,
        },

        action: {
            type: Boolean,
            default: false,
        },

        question: {
            type: Boolean,
            default: false,
        },
    },

    data() {
        return {}
    },

    computed: {
        className() {
            return {
                'button__disabled': this.disabled,
                'button__color-primary': this.primary,
                'button__color-secondary': this.secondary,
                'button__color-warning': this.warning,
                'button__color-info': this.info,
                'button__color-danger': this.danger,
                'button__color-action': this.action,
                'button__color-question': this.question,
            }
        },
    },

    methods: {
        click() {
            this.$emit( 'click')
        }
    }
}
</script>

<template>
    <button 
    @click="click"
    class="button"
    :class="className"
    :width="width"
    :height="height"
    >
        {{ title }}
    </button>
</template>

<style>
.button {
    padding: 19px;
    cursor: pointer;
    border-radius: 20px;
    font-family: "PhosphateRRSolid", sans-serif;
}

.button__disabled {
    background: var(--disabled);
    color: var(--disabled-text);
}

.button__color-primary {
    background: var(--primary);
}

.button__color-secondary {
    background: var(--secondary);
}

.button__color-warning {
    background: var(--warning);
}

.button__color-info {
    background: var(--info);
}

.button__color-danger {
    background: var(--danger);
}

.button__color-action {
    background: var(--action);
}

.button__color-question {
    background: var(--question);
}

</style>
