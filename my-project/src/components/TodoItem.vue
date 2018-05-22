<template>
  <div>
    <li @click='deletee'>{{content}}</li>
  </div>
</template>

<script>
export default {
  props: ['content', 'index'],
  methods: {
    deletee() {
      this.$emit('delete', this.index);
    }
  }
}
</script>

<style scoped>
</style>
