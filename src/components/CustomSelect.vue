<template>
  <select :value="value" @change="$emit('change', $event.target.value)">
    <option value="" selected disabled>please select</option>
    <option v-for="(item, index) in list" :key="index" :value="item.name">{{item.name}}</option>
  </select>
</template>

<script>
export default {
  name: "CustomSelect",
  model: {
    prop: "value",
    event: "change"
  },
  props: {
    value: {
      type: [String, Number]
    },
    list: {
      type: [Array],
      default() {
        return [
          { name: "jack", age: 18 },
          { name: "rose", age: 18 },
          { name: "bob", age: 17 }
        ];
      }
    }
  }
};
</script>

.<style lang="less" scoped>
</style>
