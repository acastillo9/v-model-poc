<template>
  <div>
    <p>{{ inputValue }}</p>
    <CheckboxField
      v-model="inputValue"
      v-on="customListeners" />
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
  computed: {
    customListeners() {
      return Object.keys(this.$listeners).reduce((acc, key) => {
        const newKey = key.replace('modelCompat:', '');
        acc[newKey] = this.$listeners[key];
        return acc;
      }, {})
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
    console.log(this.customListeners);
  }
}
</script>
