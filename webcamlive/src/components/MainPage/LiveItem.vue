<template>
<li class="list-group-item">
  <div class="live-item">
    <p>{{ live.username }}</p>
    <p>{{ live.title }}</p>
  </div>
</li>
</template>

<script>
export default {
  name: "LiveItem",
  props: {
    live: Object
  }
}
</script>

<style>
.list-group-item {
  height: 40px;
  outline: solid 2px black;
}

.live-item {
  display: flex;
}

.live-item p {
  margin-right: 1rem;
}
</style>