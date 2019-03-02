<script>
import VueDirection from '../src/vue-direction.vue'
import HoverBox from './hover-box.vue'

export default {
  name: 'Example',
  components: {
    VueDirection,
    HoverBox,
  },
}
</script>

<template>
  <div id="example">
    <VueDirection>
      <template slot-scope="{ mouseDirection }">
        <HoverBox :mouseDirection="mouseDirection" />
      </template>
    </VueDirection>
  </div>
</template>

<style scoped>
#example {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  display: -webkit-flex;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
