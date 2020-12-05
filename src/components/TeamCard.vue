<template>
    <div class="col-lg-3 col-sm-6">
        <div class="card text-left shadow mb-2">
            <img class="card-img-top" v-bind:src="member.image" v-bind:alt="member.nombre">
            <div class="card-body">
                <h4 class="card-title">{{member.nombre}}</h4>
                <p class="card-text">
                    {{member.descripcion}}
                </p>
                <p class="card-text">
                    {{member.rol}}
                </p>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "TeamCard",
        props: ['member']
    }
</script>

<style scoped>

</style>
