<template>
  <label>
    {{label}}
    <input
      type="checkbox"
      :checked="checked"
      @change="$emit('change', $event.target.checked)"
    >
    {{checked}}
  </label>
</template>

<script>
export default {
  name: "CustomCheckbox",
  model: {
    prop: "checked",
    event: "change"
  },
  props: {
    checked: [Boolean, Array, String],
    label: {
      type: String
    }
  }
};
</script>

<style lang="less" scoped>
</style>
