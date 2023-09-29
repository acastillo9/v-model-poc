<template>
  <div>
    <input type="checkbox" id="checkbox" :checked="value" @change="$emit('input', $event.target.checked)">
    <label for="checkbox">{{ value }}</label>
  </div>
</template>

<script>
export default {
  name: 'CheckboxField',
  props: ['value'],
}
</script>
