<template>
<section class="users">
  <p v-if="!users">Loading users...</p>
  <ul v-else class="list">
    <User
      v-for="(user, index) in users"
      :key="index"
      :user="user"
    />
  </ul>


</section>
</template>

<script>
import User from './User';
import { getUsersandGoals } from '../services/api';
export default {
  data() {
    return { 
      users: null
    };
  },
  created() {
    getUsersandGoals()
      .then(users => {
        this.users = users;
      });
  },
  components: { 
    User,
  },
};
</script>

<style scoped>
section {
  padding-bottom: 100px;
}
</style>