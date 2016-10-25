<template>
  <div class="slider js_slider">
    <div class="frame js_frame">
      <ul class="slides js_slides">
        <slot name="slide"></slot>
      </ul>
    </div>
    <slot name="actions"></slot>
  </div>
</template>

<script>
import { lory } from 'lory.js'

export default {

  props: {
    options: {
      type: Object,
      default: () => ({})
    }
  },

  data () {
    return {
      slider: null
    }
  },

  mounted () {
    this.slider = lory(this.$el, this.options)
  },

  beforeDestroy () {
    this.slider.destroy()
  }

}
</script>

<style>
</style>
