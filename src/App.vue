<template>
  <v-app>
    <v-card class="mx-auto mt-5 pa-2">
      <v-card-title class="pb-0">
        <h1>Login</h1>
      </v-card-title>
      <v-card-text>
        <v-form>
          <v-text-field 
            label="Username"
            prepend-icon="account_circle" />
          <v-text-field
            :type="showPassword ? 'text' : 'password'"
            label="Password"
            prepend-icon="lock"
            :append-icon="showPassword ? 'visibility_on' : 'visibility_off'" 
            @click:append="showPassword = !showPassword"/>
        </v-form>
      </v-card-text>
      <v-card-actions>
        <v-btn color="success">Register</v-btn>
        <v-btn color="info">Login</v-btn>
      </v-card-actions>
    </v-card>
  </v-app>
</template>

<script>

export default {
  name: 'App',
  data () {
    return {
      showPassword: false
    }
  }
}
</script>

<style>

.v-card {
  width: 400px;
}
</style>
