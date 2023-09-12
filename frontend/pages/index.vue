<template>
  <v-container class="text-center align center">
    <v-row>
      <v-col>
        <h1 class="mb-4">Learning Through Conversation</h1>
        <Button primary @click="redirectToConvo">Start Conversing</Button>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import Button from "@/components/Button.vue";

export default {
  components: {
    Button,
  },
  methods: {
    redirectToConvo() {
      this.$router.push({ name: "conversation" });
    },
  },
};
</script>

<style></style>
