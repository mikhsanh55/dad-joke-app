<template>
  <section class="container">
    <b-card class="mb-2">
      <h3>Welcome Dad! 😜</h3>
      <p>Looking for something funny? you found the great place!</p>
    </b-card>

    <b-row>
      <joke v-for="(joke, i) in jokes.results" :joke="joke" :key="i" />
    </b-row>
  </section>
</template>

<script>
  import Joke from '@/components/Joke.vue'
export default {
  components: {
    Joke
  },
  async asyncData({ $axios }) {
    const params = {
      page: 1,
      term: ''
    }
    const jokes = await $axios.get('https://icanhazdadjoke.com/search', {
      headers: {
        'Accept': 'application/json'
      },
      params
    })

    const result = jokes.data

    return {jokes: result}
  }
}
</script>
<style>
  header ul {
    list-style-type: none;
    display: flex;
    justify-content: center;
    margin-bottom: 1rem;
  }

  .text-center {
    text-align: center;
  }
</style>
