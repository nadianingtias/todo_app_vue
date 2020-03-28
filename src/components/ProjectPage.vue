<template>
    <div>
        <nav class="navbar navbar-light bg-light">
            <div class="container">
                <a class="navbar-brand" href="#">
                    <img class="d-inline-block align-top" height="40" alt="Brand logo" src="../assets/todo.png">
                    <a class="navbar-brand" href="#">TO-DO Apps</a>

                </a>
            </div>
        </nav>
        <div class="container" style="margin-top:30px">
            <div class="row">
                <Board v-bind:board="board" />
                <div class="col-md-4">
                    <div class="bd-example">
                        <div class="title-board">
                            <h2>Backlog</h2>
                        </div>
                        <div class="body-board">

                            <div class="card todo" style="width: 100%;">
                                <img class="card-img-top" src="../assets/sample.png" alt="Card image cap">
                                <div class="card-body">
                                    <h5 class="card-title">Fitur Login dan Signup Aplikasi E-accounting</h5>
                                    <!-- <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p> -->
                                </div>

                                <!-- <div class="card-body" style="padding-top:0px">
                                <a href="#" class="card-link">Card link</a>
                                <a href="#" class="card-link">Another link</a>
                                <img class="ava rounded-circle" height="30" alt="Member Avatar"
                                    src="../assets/image/ava1.jpg">
                                <img class="ava rounded-circle" height="30" alt="Member Avatar"
                                    src="../assets/image/ava1.jpg">

                            </div> -->
                            </div>
                        </div>
                        <div class="footer-board">
                            <a class="btn btn-light btn-block" data-toggle="collapse" href="#collapseExample"
                                role="button" aria-expanded="false" aria-controls="collapseExample">
                                Add New Card
                            </a>
                            <div class="collapse card" id="collapseExample">
                                <div class="card-body">
                                    <form>
                                        <div class="form-group">
                                            <input type="text" class="form-control" id="exampleInputEmail1"
                                            placeholder="Enter title for this card">
                                        </div>
                                        <button type="submit" class="card-link btn btn-primary btn-sm" style="width:30%">add</button>
                                        <button  class="card-link btn btn-light btn-sm" style="width:30%">cancel</button>
                                    </form>
                                    
                                    
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <AddBoard />
            </div>

        </div>

    </div>
</template>

<script>
    import Board from '../components/Board';
    import AddBoard from '../components/AddBoard';

    export default {
        name: "ProjectPage",
        components: {
            Board,
            AddBoard
        },
        
        data() {
            return {
                board: [{
                        id: 1,
                        title: 'Design Workflow',
                        completed: false
                    },
                    {
                        id: 2,
                        title: 'Wireframing',
                        completed: false
                    },
                    {
                        id: 3,
                        title: 'Low fidelity',
                        completed: false
                    },
                    {
                        id: 4,
                        title: 'High Fidelity',
                        completed: false
                    }
                ],
            }
        }

    }
</script>

<style scoped>
    .ava {
        padding-left: 5px
    }

    .title-board h2 {
        font-size: 24px;
        padding-bottom: 10px;
        text-align: left;
    }

    .footer-board {
        padding-top: 20px;

    }
</style>