<template>
  <p>Reaction time: {{ score }}ms</p>
  <p>{{ rank }}</p>
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
    if (this.score < 200) this.rank = 'psycho';
    else if (this.score < 600) this.rank = 'loser';
    else this.rank = 'sucker';
  },
};
</script>

<style></style>
