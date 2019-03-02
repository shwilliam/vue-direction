<script>
export default {
    name: 'VueDirection',
    data() {
        return {
            xDirection: '',
            yDirection: '',
            oldX: 0,
            oldY: 0,
        }
    },
    computed: {
        mouseDirection() {
            return { x: this.xDirection, y: this.yDirection }
        },
    },
    methods: {
        getMouseDirection(e) {
            if (this.oldX < e.pageX) {
                this.xDirection = 'right'
            } else {
                this.xDirection = 'left'
            }
        
            if (this.oldY < e.pageY) {
                this.yDirection = 'down'
            } else {
                this.yDirection = 'up'
            }
        
            this.oldX = e.pageX
            this.oldY = e.pageY
        },
    },
}
</script>

<template>
    <div @mousemove="getMouseDirection">
        <slot
            :mouseDirection="mouseDirection"
        />
    </div>
</template>
