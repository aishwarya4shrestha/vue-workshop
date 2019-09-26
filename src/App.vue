<template>
  <div id="app">
    <registration-form>
      <template slot="form-header">
        <div class="heading">
          <h4 class="title">Register to create a new account</h4>
        </div>
      </template>
      <template slot="form-field" slot-scope="slotProps">
        <div class="form-group">
          <label class="label" for="name">Name</label>
          <input
            v-model="name"
            type="text"
            class="form-control"
            id="name"
            placeholder="name"
            required
          />
        </div>
        <div class="form-group">
          <label class="label" for="email">Email address</label>
          <input type="email" class="form-control" id="email" placeholder="email" required />
        </div>
        <div class="form-group">
          <label class="label" for="password">Password</label>
          <input type="password" class="form-control" id="password" placeholder="password" required />
        </div>
        <div class="error">{{slotProps}}</div>
        <!-- Take child's props likt thos -->
      </template>
    </registration-form>
  </div>
</template>

<script>
import RegistrationForm from "./components/RegistrationForm.vue";

export default {
  name: "app",
  components: {
    RegistrationForm
  },
  data() {
    return {
      endpoints: "something",
      fields: {
        name: "Aish"
      }
    };
  }
};
</script>

<style lang="scss">
@import "./styles/main.scss";

#app {
  margin-top: 60px;
}
</style>