<template>
    <div class="input-wrapper">
        <label for="date">{{ label }}</label>
        <input type="date" class="input-date" v-model="inputValue">
    </div>
</template>

<script>
export default {
    name: 'InputDate',
    props: {
        label: {
            type: String
        },
        value: {
            type: String
        }
    },
    data() {
        return {
            inputValue: ''
        };
    },
    watch: {
        inputValue(newValue) {
            this.$emit('input', newValue);
        },
        value(newValue) {
            this.inputValue = newValue;
        }
    }
};
</script>

<style lang="scss" scoped>
    .input-date {
        width: 256px;
        height: 52px;
        padding: 0px 16px 0px 16px;
        text-transform: uppercase;
    }
</style>