<template>
  <div class="editor">
    <h1>エディター画面</h1>
    <span>{{ user.displayName }}</span><br>
    <button @click="logout">ログアウト</button>
  </div>
</template>

<script>
  export default {
    name: 'editor',
    props: ["user"],
    data() {
      return {};
    },
    methods: {
      logout: function () {
        firebase.auth().signOut();
      }
    }
  };
</script>
