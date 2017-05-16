<template>
 <div class="row">
        <div class="input-field col s3">
          <input placeholder="Placeholder" id="first_name" type="text" v-model="newTask.title" class="validate">
          <label for="first_name">Title</label>
        </div>
        <div class="input-field col s3">
          <input id="last_name" type="text" class="validate" v-model="newTask.importance">
          <label for="last_name">Importance</label>
        </div>
				<div class="input-field col s3">
          <input id="last_name" type="text" class="validate" v-model="newTask.hours">
          <label for="last_name">Hours</label>
        </div>

		
    <p>
      <input name="group1" type="radio" id="test1" v-bind:value="true" v-model="newTask.visibility"/>
      <label for="test1">Visible</label>
    </p>
    <p>
      <input name="group1" type="radio" id="test2" v-bind:value="false" v-model="newTask.visibility"/>
      <label for="test2">Unvisible</label>
    </p>
    
      <button class="btn" @click="addTask" type="button">Send</button>   
      </div>
</template>

<script>

import {Bus} from '@/Bus.js'
import {Store} from '@/Store.js'

export default {
  name: 'AddTask',
  data(){
    
    return {
      datas: Store.datas,
     newTask: {
        title: "",
        importance: 0,
        hours: 2,
        visibility: true
     }
    }
  },
  methods: {
    addTask: function(){
      console.log("new task added");
      this.datas.tasks.push(this.newTask);
    }// end addTask function
  }// end methods
}
</script>

<style scoped>

</style>