<script setup>
import { ref, watch } from 'vue'
import { fa } from 'vuetify/locale';

const msg = ref('TODO LIST')
const list = ref([])
const todo = ref('')


function addTodo() {
  if (todo.value.trim() !== '') {
    list.value.push(todo.value)
    todo.value = ''
    alert('Insert successful')

  }
  else {
    alert('Empty')
  }
}


</script>


<template>
  <!--
    <v-text-field
    append-inner-icon="mdi-check-circle" label="Add Item"
    v-model="todo">
  </v-text-field>
    <v-btn
      append-icon="mdi-account-circle"
      prepend-icon="mdi-check-circle"
      height="50px"
      @click="addTodo"
    >
      <template v-slot:prepend>
        <v-icon color="success"></v-icon>
      </template>
      ADD
      <template v-slot:append>
        <v-icon color="warning"></v-icon>
      </template>
    </v-btn>
   
    <v-card
      class="mx-auto"
      max-width="100%"
      
    >
  
      <v-list :items="items"  v-for="(item, index) in list" :key="index">{{ item }}
        <v-btn class="ga-md-15" icon="mdi-information" variant="text" margin-left="500"></v-btn>
      </v-list>
    </v-card>
    <Test />
    <Flexbox />

  -->
</template>



<style>





</style>
