<template>

    <div>
        <a class="btn btn-light btn-block" data-toggle="collapse" href="#collapseExample"
                                role="button" aria-expanded="false" aria-controls="collapseExample">
                                Add New Card
                            </a>
                            <div class="collapse card" id="collapseExample">
                                <div class="card-body">
                                    <form  @submit="addCard">
                                        <div class="form-group">
                                            <input v-model="title" type="text" class="form-control" id="exampleInputEmail1"
                                            placeholder="Enter title for this card">
                                        </div>
                                        <button type="submit" class="card-link btn btn-primary btn-sm" style="width:30%">add</button>
                                        <button  class="card-link btn btn-light btn-sm" style="width:30%">cancel</button>
                                    </form>
                                    
                                    
                                </div>
                            </div>
        <!-- <form @submit="addCard">
            <input type="text"  name="title" >
            <button type="submit">Add</button>
        
        </form> -->
    </div>
</template>

<script>
import uuid from 'uuid';
export default {
    
    name : 'AddCard',
    methods : {
        addCard(e){
            e.preventDefault();
            const newTodoObj = {
                id : uuid.v4(),
                title : this.title,
                completed : false
            }

            this.$emit('add-todo', newTodoObj);
            this.title = ''
        }
    }
    ,
    data() {

            return{
                title:''
            }
        }
}
</script>

<style scoped>

</style>