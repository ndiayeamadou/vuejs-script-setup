<template>
  <h2>Testing...</h2>
  <h3 @click="handleHeadingClick">Abbreviation name : {{name}} | age : {{age}}</h3>
  <MyButton
    @buttonClicked="showAlert"
    text="Text button w/ props :-)"
  />
</template>


<script setup>
import { ref } from 'vue'
import MyButton from "@/components/Mybutton.vue"

const name = ref('AMADU')
const age = ref(32)

const handleHeadingClick = () => {
  name.value = 'ELAN'
}
const showAlert = () => {
  alert("Child button was clicked!")
}
</script>

<!--
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

    const showAlert = () => {
      alert("This is an alert, shown when clicked button!")
    }

    return {
      age, name, handleHeadingClick, showAlert
    }
    
  },

  components: {
    MyButton
  }

}
</script>
-->