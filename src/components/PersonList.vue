<template>
  <h1>Lista</h1>
  <div class="list">
    <div v-for="user in users" :key="user.id">
      <PersonItem :user="user" :callback="removeElement" />
    </div>
  </div>
</template>

<script>
import PersonItem from "./PersonItem.vue";
export default {
  name: "PersonList",
  data() {
    return { users: [] };
  },
  created() {
    fetch("https://jsonplaceholder.typicode.com/users")
      .then((response) => response.json())
      .then((data) => (this.users = data));
  },
  components: {
    PersonItem,
  },
  methods: {
    removeElement: function (index) {
        let del = this.users.findIndex(elem => elem.id == index)
        if(del>=0){
            this.users.splice(del, 1);
        }
      
    },
  },
};
</script>

<style scoped>
.list {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
