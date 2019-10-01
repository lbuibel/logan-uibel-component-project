<template>
    <v-container>
        <v-row>
            <v-col 
                v-for="server in 6"
                :key="server"
                cols="12" 
                sm="4">
                <app-server-status></app-server-status>
            </v-col>
        </v-row>
    </v-container>

</template>

<script>

import ServerDetails from '../components/ServerDetails'

export default {
    components: {
        'app-server-status': ServerDetails
    }
}


</script>

<style scoped>

</style>