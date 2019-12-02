<template>
  <div>
    <span>
      <slot v-bind:obj="obj" name="firstname">{{obj.firstName}}</slot>
    </span>
    <span>
      <slot v-bind:obj="obj" name="lastname">{{obj.lastName}}</slot>
    </span>
    <span>
      <slot v-bind:obj="obj"></slot>
    </span>
  </div>
</template>

<script>
export default {
  data() {
    return {
      obj: {
        firstName: "jack",
        lastName: "smith",
        age: "234"
      }
    };
  }
};
</script>

<style>
</style>
