<template>
  <div class="results">
    Reaction time: {{ score }} ms
    <p class="rank">{{ rank }}</p>
  </div>
</template>

<script>
export default {
    props: ['score'],
    data() {
        return {
            rank: null
        }
    },
    mounted() {
        if (this.score < 250) {
            this.rank = 'Ninja Fingers'
        } else if (this.score < 400) {
            this.rank = 'Rapid Fingers'
        } else {
            this.rank = 'Snail Pace...'
        }
    }
}
</script>

<style>
 .rank  {
    font-size: 1.4em;
    color: teal;
    font-weight: bold;
}

.results {
    margin: 40px auto;
}
</style>