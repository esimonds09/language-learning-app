<template>
  <v-btn :class="btnClass" @click="handleClick">
    <slot></slot>
  </v-btn>
</template>

<script>
export default {
  props: {
    primary: Boolean,
    secondary: Boolean,
    disabled: Boolean,
  },
  computed: {
    btnClass() {
      return {
        "v-btn--contained": this.primary,
        "v-btn--outlined": this.secondary,
        "v-btn--disabled": this.disabled,
      };
    },
  },
  methods: {
    handleClick() {
      this.$emit("click");
    },
  },
};
</script>
