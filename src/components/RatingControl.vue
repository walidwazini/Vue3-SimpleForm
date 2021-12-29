<template>
  <ul>
    <li :class="{ active: modelValue === 'poor' }">
      <button type="button" @click="activate('poor')">Poor</button>
    </li>
    <li :class="{ active: modelValue === 'average' }">
      <button type="button" @click="activate('average')">Average</button>
    </li>
    <li :class="{ active: modelValue === 'rich' }">
      <button type="button" @click="activate('rich')">Rich</button>
    </li>
  </ul>
</template>

<script>
export default {
  props: ["modelValue"],
  emits: ["update:modelValue"],
  // data(){
  //   return {
  //     activeOption: this.modalValue,
  //   }
  // },
  // computed: {
  //   activeOption() {
  //     return this.modelValue;
  //   },
  // },
  methods: {
    activate(option) {
      // this.activeOption = option;
      this.$emit("update:modelValue", option);
    },
  },
};
</script>

<style>
</style>