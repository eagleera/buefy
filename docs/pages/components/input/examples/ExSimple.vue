<template>
    <section>
        <button @click="() => loading = !loading">Toggle skeleton</button>
        <b-field label="Name" :loading="loading">
            <b-input v-model="name"></b-input>
        </b-field>

        <b-field label="Email"
            type="is-danger"
            message="This email is invalid"
            :loading="loading">
            <b-input type="email"
                value="john@"
                maxlength="30">
            </b-input>
        </b-field>

        <b-field label="Skeleton" :loading="loading">
            <b-input v-model="name"></b-input>
        </b-field>

        <b-field label="Username"
            type="is-success"
            message="This username is available"
            :loading="loading">
            <b-input value="johnsilver" maxlength="30"></b-input>
        </b-field>

        <b-field label="Password" :loading="loading">
            <b-input type="password"
                value="iwantmytreasure"
                password-reveal>
            </b-input>
        </b-field>

        <b-field label="Message">
            <b-input maxlength="200" type="textarea"></b-input>
        </b-field>
    </section>
</template>

<script>
    export default {
        data() {
            return {
                name: 'John Silver',
                loading: false
            }
        }
    }
</script>
