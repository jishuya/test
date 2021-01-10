<template>
  <v-container>
    {{ todoList }}
  <v-container>
    <v-layout row wrap>
      <v-flex xs6>
        <List/>
      </v-flex>
      <v-flex>
        <ListAdd @listAdd="listAdd" />
      </v-flex>
    </v-layout>
</template>
<script>
import List from "./List"
import ListAdd from "./ListAdd"

export default {
  components: {
    List,
    ListAdd
  },
  data() {
    return{
      todoList: []
    }
  },
  methods: {
    listAdd(memo) {
      console.log("받았어!!")
      this.todoList.push({  })
    }
  }  
}
</script>