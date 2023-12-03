<template>
    <form class="form">
        <InputText
            v-model="user.name"
            label="Имя*"
            name="name"
        />
        <InputText
            v-model="user.secondname"
            label="Фамилия*"
            name="secondname"
        />
        <InputText
            v-model="user.surname"
            label="Отчество"
            name="surname"
        />
        <InputDate label="Дата рождения" v-model="user.birthsDay"/>
    </form>
</template>

<script>
import InputDate from './UI/InputDate.vue';
import InputText from './UI/InputText.vue';

export default {
    name: 'CreateUserForm',
    components: { InputText, InputDate },
    data() {
        return {
            user: {
                name: '',
                secondname: '',
                surname: '',
                birthsDay: ''
            }
        }
    }
};
</script>

<style lang="scss" scoped>
    .form {
        display: flex;
        flex-direction: column;
        gap: 20px;
    }
</style>