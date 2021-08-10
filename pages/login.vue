<template>
    <div class="container">
        <topbar></topbar>
        <p class="title">
            {{ 'Login' }}
        </p>
        <div>
            <input type="text" placeholder="Username"
             v-model="input.username" id="username" name="username">

            <input type="password" placeholder="Password"
             v-model="input.password" id="password" name="password">

            <input type="submit" value="Login" @click="login()">
        </div>
        <div>
            {{ loginMessage }}
        </div>
    </div>
</template>

<script>
import {defineComponent} from '@vue/composition-api';
import topbar from '~/components/topbar.vue';

export default defineComponent({
  name: 'Login',
  data() {
    return {
      input: {
        username: '',
        password: '',
      },
      loginMessage: '',
    };
  },
  methods: {
    login() {
      if (
        this.username?.input !== '' && this.input?.password !== '' &&
        this.username?.input !== null && this.input?.password !== null &&
        this.username?.input !== undefined && this.input?.password !== undefined
      ) {
        this.loginMessage = 'Login was successful!';
      } else {
        this.loginMessage = 'Login failed! Incorrect username or password!';
      }
    },
  },
  components: {topbar},
  setup() {

  },
});
</script>

<style scoped>

</style>
