<template>
    <div class="col-md-4">
        <div>
            <div class="bd-example">
                <div class="title-board">
                    <h2>Board</h2>
                </div>
                <div class="body-board">
                    <li v-bind:key="item.id" v-for="item in board" style="list-style:none">
                        <Card v-bind:card="item" />
                    </li>
                </div>
                <div class="footer-board">
                    <AddCard v-on:add-card="addCard" />
                </div>
                <div class="footer-board">
                            
                </div>
            </div>

        </div>
    </div>
</template>

<script>
    
    import Card from './Card';
    import AddCard from './AddCard';

    export default {
        name: 'Board',
        components: {
            Card,
            AddCard
        },
        props: [
            "board"
        ],
        methods: {
            addCard(newTodoObj) {
                this.board = [...this.board, newTodoObj]
            }
        }
    }
</script>

<style scoped>

    .title-board h2 {
        font-size: 24px;
        padding-bottom: 10px;
        text-align: left;
    }

    .footer-board {
        padding-top: 20px;

    }
</style>