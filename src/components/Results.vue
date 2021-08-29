<template>
  <p class="score">Reaction time - {{ score }} ms</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ['score'],
  data() {
    return {
      rank: null,
    };
  },
  mounted() {
    if (this.score < 250) {
      this.rank = 'Great Reflexes';
    } else if (this.score < 400) {
      this.rank = 'Good Reflexes';
    } else {
      this.rank = 'You can do better, try again!';
    }
  },
};
</script>

<style>
.rank {
  margin-top: 50px;
  font-size: 2.5em;
  color: #f12155;
  font-weight: bold;
}

.score {
  font-size: 1.2rem;
}
</style>
