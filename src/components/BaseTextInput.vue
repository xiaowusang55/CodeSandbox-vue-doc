<template>
  <label>
    BaseTextInput:
    <input
      :value="value"
      @input="$emit('input', $event.target.value)"
      v-bind="$attrs"
    >
    {{value}}
  </label>
</template>

<script>
export default {
  name: "BaseTextInput",
  inheritAttrs: false,
  props: ["value"]
};
</script>

<style>
</style>