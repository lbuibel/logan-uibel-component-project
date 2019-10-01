<template>

<div>

    <v-card
    class="mx-auto"
    dark
  >
    <v-card-title margin-bottom="50"> Server Status</v-card-title>
    
    <v-card-actions
    margin-bottom="20px">
    <div @click="changeStatus">
        <v-btn color="primary" small>Change Status</v-btn>
    </div>
    </v-card-actions>

    <v-alert
      dense
      :type= "type"
      :color=  "color"
      dark
    >
      Server Status {{ status }}
    </v-alert>

  </v-card>


 </div>
</template>

<script>
import colors from 'vuetify/lib/util/colors'

export default {
    data: function () {
        return {
            status: 'Critical',
            color: "red",
            type: "error"
        }  
    },
    methods: {
        changeStatus () {
            if (this.status === 'Critical'){
                this.status = 'Normal'
                this.color = "green"
                this.type = "success"
            } else {
            this.status = 'Critical'
            this.color = "red"
            this.type = "error"
            }
        }
    }
}

</script>

<style scoped>

</style>