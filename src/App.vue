<template>
  <h2>Testing...</h2>
  <h3 @click="handleHeadingClick">Abbreviation name : {{name}} | age : {{age}}</h3>
  <MyButton />
</template>

<!--
<script setup>
import { ref } from 'vue'

const name = ref('AMADU')
const age = ref(32)

const handleHeadingClick = () => {
  name.value = 'ELAN'
}
</script>
-->

<script>
import { ref } from 'vue'
import MyButton from "@/components/MyButton.vue"
/* import MyButton from "./components/MyButton.vue" */

export default {
  setup() {
    const name = ref('AMADU')
    const age = ref(32)

    const handleHeadingClick = () => {
      name.value = "ELAN"
      age.value = 45
    }

    return {
      age, name, handleHeadingClick
    }
    
  },

  components: {
    MyButton
  }

}
</script>
