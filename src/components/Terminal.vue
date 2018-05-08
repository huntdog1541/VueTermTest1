<template>
    <div class="terminal" ref="terminal">
        <prompt :active="true" :prmtUsername="username" :prmtLocation="location" :prmptDirectory="directory"></prompt>
    </div>
</template>

<script>
    import Prompt from './prompt.vue';
    import { store } from '../store.js'

    export default {
        name: "Terminal",
        components: {
            Prompt
        },
        store,
        computed: {
            username() {
                return this.$store.state.username;
            },
            location() {
                return this.$store.state.location;
            },
            directory() {
                return this.$store.state.directory;
            }
        }
    }
</script>

<style scoped>

</style>