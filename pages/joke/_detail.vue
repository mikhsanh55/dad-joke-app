<template>
    <b-card class="container">
        <h2>The Joke</h2>
        <p class="mb-4">{{joke.joke}}</p>
        
        <p class="text-center text-primary">
            <nuxt-link to="/">All Joke</nuxt-link>
        </p>
    </b-card>
</template>
<script>
    export default {
        data: () =>({
            joke: {
                joke: null
            }
        }),
        async fetch() {
            const response = await this.$axios.get(`https://icanhazdadjoke.com/j/${this.$route.params.detail}`, {
                headers: {
                    'Accept': 'application/json'
                }
            })

            this.joke = response.data
            console.log('joke', this.joke)
        }
    }
</script>