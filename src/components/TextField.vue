<template>
  <div>
    <input type="text" id="text" :checked="value" @input="$emit('input', $event.target.checked)">
    <label for="text">{{ value }}</label>
  </div>
</template>

<script>
export default {
  name: 'TextField',
  props: ['value'],
}
</script>
