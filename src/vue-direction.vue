<script>
export default {
  name: "VueDirection",
  data() {
    return {
      xDirection: "",
      yDirection: "",
      prevPageX: 0,
      prevPageY: 0
    };
  },
  computed: {
    mouseDirection() {
      return { x: this.xDirection, y: this.yDirection };
    }
  },
  methods: {
    getMouseDirection(e) {
      if (this.prevPageX < e.pageX) {
        this.xDirection = "right";
      } else {
        this.xDirection = "left";
      }

      if (this.prevPageY < e.pageY) {
        this.yDirection = "down";
      } else {
        this.yDirection = "up";
      }

      this.prevPageX = e.pageX;
      this.prevPageY = e.pageY;
    }
  }
};
</script>

<template>
  <div @mousemove="getMouseDirection">
    <slot :mouseDirection="mouseDirection"/>
  </div>
</template>
