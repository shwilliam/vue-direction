<script>
export default {
  name: 'HoverBox',
  props: ['mouse-direction']
}
</script>

<template>
  <div class="hover-box">
    {{
      mouseDirection.x === ''
      ? 'hover me'
      : `${mouseDirection.x} ${mouseDirection.y}`
    }}
  </div>
</template>

<style scoped>
.hover-box {
  width: 100px;
  height: 100px;
  background-color: lightpink;
  display: -webkit-flex;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
