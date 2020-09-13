<template>
    <div class="col-xs-12 col-sm-6">
        <p v-if="!server">select a server</p>
        <p v-else>Server {{ server.id }} selected, Status {{ server.status }}</p>
        <button @click="resetStat">reset stat</button>
    </div>

</template>

<script>
    import { eventBus } from '../../main';
    export default {
        data() {
            return {
                server: null,
            }
        },
        methods: {
          resetStat() {
              this.server.status = 'Normal';
          }
        },
        created() {
            eventBus.$on('serverSelected', (server) => {
                this.server = server;
            });
        }
    }
</script>

<style>

</style>
