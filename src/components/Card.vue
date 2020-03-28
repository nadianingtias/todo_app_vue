<template>
  <div>
    <div class="card todo" style="width: 100%;">
      <img class="card-img-top" src="../assets/sample.png" alt="Card image cap">
      <div class="card-body">
        <h5 class="card-title">{{ card.title }}</h5>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Card',
    props: [
      "card"
    ]
  }
</script>
<style scoped>
  .card.todo{
    margin-top: 10px;
  }
</style>