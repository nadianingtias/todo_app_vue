<template>
    <div class="col-md-4">
                    <div class="bd-example">

                        <div class="footer-board">
                            <div class="collapse" id="newBoard">
                                <div class="card card-body">
                                    <div class="form-group">
                                        <input type="text" class="form-control" id="exampleInputEmail1"
                                            placeholder="Enter title for this board">
                                    </div>
                                </div>
                            </div>
                            <a class="btn btn-light btn-block" data-toggle="collapse" href="#newBoard" role="button"
                                aria-expanded="false" aria-controls="newBoard">
                                Add New Board
                            </a>

                        </div>
                    </div>
    </div>
</template>

<script>
export default {
    name : 'AddBoard'
}
</script>

<style scoped>

</style>