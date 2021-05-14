<template>
  <form>
    <FormSection>
      <input type="text" v-model="inputs.foo">
    </FormSection>
    <input type="text" v-model="inputs.bar">
  </form>
</template>

<script lang="ts">
import {defineComponent, ref} from 'vue'
import FormSection from "./components/FormSection.vue";

export default defineComponent({
  name: 'App',
  components: {
    FormSection
  },
  setup() {
    const inputs = ref({
      foo: '',
      bar: '',
    });

    return { inputs }
  }
})
</script>
