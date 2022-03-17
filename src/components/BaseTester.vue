<template>
  <v-container>
    <v-row class="text-center">
      <v-col class="mb-4">
        <v-select
            label="Person"
            :items="items"
            item-text="name"
            item-value="id"
            @change="submitForm"
        />
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup>
import { reactive, ref } from 'vue'

const items = ref([{ name: 'James', id: 10001 }, { name: 'Peter', id: 10002 }, { name: 'John', id: 10003 }])

const myForm = reactive({
  person: 0,
})

function submitForm () {
  console.log('called...')
  console.log(myForm)
}
</script>

<style scoped>

</style>
