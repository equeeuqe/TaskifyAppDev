<template id="ToDo">
    <div id="todo" class="container">
        <form>
            <input type="text" placeholder="Enter your task" v-model="newTask">
            <button @click="addTask">Add Task</button>
            <button class="delete-all">Delete All</button>
        </form>
        <ToDo v-for="(task,index) in tasks" :key="index">
            <div class="task">
                 {{task.description}}
            <span><button class="delete" @click="deleteTask(index)">Delete</button></span>
            </div>
        </ToDo>
    </div>
</template>

<script>
import ToDo from './ToDo.vue';

export default {
    name: 'ToDoComponent',
    components: {
        ToDo,
    },
    props: {
        tasks: {
            type: Array,
            default: () => []
        }
    },
    data(){
        return{
            newTask: ""
        }
    },
    methods:{
        addTask(){
            if (this.newTask) {
                this.tasks.push({
                  description: this.newTask,
                  completed: false
                });
            this.newTask = '';
            }
        },
        deleteTask(index){
            this.tasks.splice(index,1);
        },
        deleteAll(){
            this.tasks = [];
        }
    }
}
</script>