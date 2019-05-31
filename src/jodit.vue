<template>
  <textarea :value="value" />
</template>

<script>
import Jodit from 'jodit'
export default {
  props: ['value', 'options'],
  data() {
    return {
      editor: null,
      newVal: null,
    }
  },
  mounted() {
    var app = this
    this.editor = new Jodit(this.$el, this.options)
    this.editor.events.on('change', this.handleInput)
  },
  methods: {
    handleInput (value) {
      this.newVal = value
      this.$emit('input', value)
    }
  },
  watch: {
    value(newVal, oldVal) {
      if(this.newVal != newVal) {
        this.editor.value = newVal
      }
    }
  }
}
</script>