<template id="shared">
    <div class="container">
        <Shared v-for="(task,index) in tasks" :key="index">
            <div class="card" style="width: 18rem;" id="shared_tasks">
                <div class="card-body">
                    <h5 class="card-title">Card title</h5>
                    <h6 class="card-subtitle mb-2 text-muted">Card subtitle</h6>
                    <p class="task card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
                    <a href="#" class="card-link">Card link</a>
                    <a href="#" class="card-link">Another link</a>
                </div>
            </div>
        </Shared>
        
    </div>
</template>

<script>
// import ToDo from './ToDo.vue';
import Shared from './shared.vue';

export default {
    name: 'Shared',
    components: {
        HelloWorld
    }
}
</script>

<style>

</style>