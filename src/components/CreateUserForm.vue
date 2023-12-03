<template>
    <form>
        <InputText
            v-model="user.name"
            label="Имя*"
            name="name"
        />
        <p style="color: blue;">{{ testValue }}</p>
    </form>
</template>

<script>
import InputText from './UI/InputText.vue';

export default {
    name: 'CreateUserForm',
    components: { InputText },
    data() {
        return {
            user: {
                name: ''
            }
        }
    }
};
</script>

<style lang="scss" scoped>

</style>