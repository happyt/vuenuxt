<template>
  <h1>Hello world with {{title}}</h1>
</template>
<script>
import axios from 'axios'

export default {
  async asyncData ({ params }) {
    let { data } = await axios.get(`https://dinosaur-facts-1df58.firebaseio.com/matches.json`)
    return { title: data.LiveMatches }
  }
}
</script>
