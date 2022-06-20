<template>
  <div></div>
</template>

<script>

const anotherProps = {
  e: {
    type: Function,
    default () {}
  },
  'g': {
    type: String,
    default: 'HELLO'
  }
}

const otherProps = {
    b: [Number, String],
    c: {
      type: Object,
      default: function () {
        return {
          val: 1
        }
      },
      required: true,
      validator: function () {
        return true
      }
    },
    d: 'null',
    ...anotherProps,
}

export default {
  props: {
    a: String,
    ...otherProps,
  }
}
</script>
