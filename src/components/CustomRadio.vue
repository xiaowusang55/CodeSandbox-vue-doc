<template>
  <label>
    <input
      type="radio"
      :checked="checked"
      @change="$emit('change', $event.target.checked)"
      v-bind="$attrs"
    >
    {{label}}-{{value}}
  </label>
</template>

<script>
export default {
  inhertiAttrs: false,
  name: "CustomRadio",
  props: {
    checked: {
      type: [Boolean, String, Array]
    },
    label: {
      type: String
    },
    value: {
      type: String
    }
  },
  model: {
    prop: "checked",
    event: "change"
  }
};
</script>

<style lang="less" scoped>
</style>
