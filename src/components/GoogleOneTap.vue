<template>
  <div class="google-one-tap-container">
    <div id="google-one-tap-inner"></div>
    <div v-if="response">
      <h2>
        Google API response
      </h2>
      <textarea class="response" v-model="response"></textarea>
    </div>
  </div>
</template>

<script>

import googleOneTap from 'google-one-tap';

export default {
  name: "GoogleOneTap",
  data() {
    return {
      response: null
    };
  },
  mounted() {
    const options = {
      client_id: '',
      auto_select: false,
      cancel_on_tap_outside: false,
      context: 'signin',
      prompt_parent_id: 'google-one-tap-inner'
    };
    googleOneTap(options, (response) => {
      this.response = JSON.stringify(response);
    });
  }
}
</script>

<style scoped>
  .response {
    width: 1000px;
    height: 200px;
    margin: 0 auto;
  }
</style>