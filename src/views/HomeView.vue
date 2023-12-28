<script setup lang="ts">
// import { Authenticator } from "@aws-amplify/ui-vue";
import { signInWithRedirect, signOut } from "aws-amplify/auth";

const onClick = () => {
  signInWithRedirect();
};
</script>

<template>
  <main>
    <h1>Hello World From Auth</h1>
    <!-- <Authenticator :social-providers="['google']">
      <template #="{ signOut }">
        <button @click="signOut">Sign out</button>
      </template>
    </Authenticator> -->
    <button @click="onClick">Click me for cognito</button>
    <button @click="signOut()">Sign Out</button>
  </main>
</template>
