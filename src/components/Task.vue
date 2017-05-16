<template>
  <div>
    <div class="row">
      <div class="col s3" v-for='item in listTasks.tasks'>
			<div class="row">
        <div class="col s12">
          <div class="card blue-grey darken-1">
            <div class="card-content white-text">
              <span class="card-title">{{item.title}}</span>
              <p>  bbssssssssssb:{{item.title}} </p>
              <p> Importance: {{item.importance}} </p>
              <p> Hours: {{item.hours}} </p>
              <p> Visibility: {{item.visibility}} </p>
            </div>
            <div class="card-action">
              <button class="btn" @click="deleteTask(item)" type="button">Delete</button>
              <a href="#"> </a>
            </div>
          </div>
        </div>
      </div>
			</div>
      
    </div>
          
  </div>
</template>

<script>
import {Store} from '@/Store.js'

export default {
  name: 'Task',
  data(){
    return {
      listTasks: Store.datas,
    }
  },
  methods: {
	  deleteTask: function (item) {
      let position = this.listTasks.tasks.indexOf(item);
      this.listTasks.tasks.splice(position, 1);
    }// end delete Task

}// end methods
}// end export
</script>

<style scoped>

</style>