<template>
    <b-col sm="12" md="6">
        <b-card>
            <nuxt-link :to="`/joke/${joke.id}`">
                {{joke.joke}}
            </nuxt-link>
        </b-card>
    </b-col>
</template>
<script>
    export default {
        props: ['joke'],
        mounted() {
            console.log('jokes', this.joke)
        }
    }
</script>