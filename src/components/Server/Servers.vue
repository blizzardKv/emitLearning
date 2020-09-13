<template>
    <div class="col-xs-12 col-sm-6">
        <ul class="list-group">
            <Server v-for="server in serversData" :server="server" />
        </ul>
    </div>
</template>

<script>
    import Server from "./Server.vue";
    export default {
        components: {
            Server
        },
        data() {
            return {
                serversData: [
                    { id: 1, status: 'Normal'},
                    { id: 2, status: 'Crispy'},
                    { id: 3, status: 'Danger'},
                    { id: 4, status: 'Normal'},
                ]
            }
        },
    }
</script>

<style>

</style>
