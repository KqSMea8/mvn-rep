<template>
  <li @click="handleDelete">a {{content}} b {{this.abc}} c {{this.index}}</li>
</template>

<script>
export default {
  props: ['content', 'abc', 'index'],
  methods: {
    handleDelete () {
      // 子组件与父组件通信,向外触发delete事件,把下标作为参数
      this.$emit('delete', this.index)
    }
  }
}
</script>

<style scoped>

</style>
