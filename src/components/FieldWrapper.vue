<template>
  <div>
    <p>{{ inputValue }}</p>
    <CheckboxField
      v-model="inputValue"
      v-on="$listeners" />
  </div>
</template>

<script>
import CheckboxField from './CheckboxField.vue';

export default {
  name: 'FieldWrapper',
  components: {
    CheckboxField,
  },
  props: ['value'],
  data() {
    return {
      inputValue: ''
    }
  },
  watch: {
    value(newVal) {
      this.inputValue = newVal;
    },
  },
  mounted() {
    this.inputValue = this.value;
    console.log(this.$attrs);
    console.log(this.$listeners);
  }
}
</script>
