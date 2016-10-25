<template>
  <div class="slider js_slider">
    <div class="frame js_frame">
      <ul class="slides js_slides">
        <slot></slot>
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

<style lang="scss">
/**
 * (optional) define here the style definitions which should be applied on the slider container
 * e.g. width including further controls like arrows etc.
 */
.slider {

  .frame {
    /**
     * (optional) wrapper width, specifies width of the slider frame.
     */
    width: 100%;

    position: relative;
    font-size: 0;
    line-height: 0;
    overflow: hidden;
    white-space: nowrap;
  }

  .slides {
    width: 100%;
    display: inline-block;
  }

  li {
    position: relative;
    display: inline-block;

    /**
     * (optional) if the content inside the slide element has a defined size.
     */
    width: 100%;

    position: relative;
    display: inline-block;
    text-align: center;
    font-size: 15px;
    line-height: 30px;
  }

  .prev, .next {
    position: absolute;
    top: 50%;
    margin-top: -25px;
    display: block;
    cursor: pointer;
  }

  .next {
    right: 0;
  }

  .prev {
    left: 0;
  }

  .next svg, .prev svg {
    width: 25px;
  }

  &.js_rewind {
    .frame li {
      margin-right: 10px;
    }
  }
}
</style>
