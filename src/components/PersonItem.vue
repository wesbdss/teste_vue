<template>
  <div class="card">
    <div class="name">
      <h3>{{ user.name }}</h3>
    </div>
    <div class="description">
      <h5><strong>Id: </strong>{{ user.id }}</h5>
      <h5><strong>Nome: </strong>{{ user.username }}</h5>
    </div>
    <div>
      <p><strong>Website: </strong> {{ user.website }}</p>
    </div>

    <button :key="user.id" v-on:click="callback(user.id)">Excluir</button>
  </div>
</template>

<script>
export default {
  name: "PersonItem",
  props: {
    user: Object,
      callback: {type: Function},
  },
};
</script>


<style scoped>
.card {
  display: flex;
  width: 100%;
  flex-direction: column;
  background-color: aqua;
  border-radius: 20px;
  margin: 10px;
  padding: 20px;
}
.description {
}
</style>
