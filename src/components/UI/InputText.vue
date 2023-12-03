<template>
    <div class="input-wrapper">
        <label :for="name">{{ label }}</label>
        <span v-if="isError" class="input-error"></span>
        <input
            type="text"
            class="input"
            name="name"
            v-model="inputValue"
        />
    </div>
</template>

<script>
export default {
    name: 'InputText',
    props: {
        label: {
            type: String
        },
        value: {
            type: String
        },
        name: {
            type: String
        },
        isError: {
            type: Boolean,
            default: false
        },
        errorMessage: {
            type: String
        }
    },
    data() {
        return {
            inputValue: ''
        }
    },
    watch: {
        inputValue(newValue) {
            this.$emit('input', newValue);
        },
        value(newValue) {
            this.inputValue = newValue;
        },
    }
};
</script>

<style lang="scss" scoped>
.input-wrapper {
    display: flex;
    flex-direction: column;
    gap: 10px;
}

.input {
    height: 52px;
    padding: 0px 32px 0px 12px;
    max-width: 460px;
    background-color: #F5F7FA;
    border: 2px solid #F5F7FA;
    border-radius: 8px;
    color: #0b1f33;
    font-size: 16px;
    outline: none;
    
    &:focus {
        border: 2px solid #99B1E6;
    }
}

</style>