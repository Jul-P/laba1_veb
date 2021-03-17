<template>

 <v-stepper v-model="e1">
    <v-stepper-header>
      <v-stepper-step
        :complete="e1 > 1"
        step="1"
      >
        Name of step 1
      </v-stepper-step>

      <v-divider></v-divider>

      <v-stepper-step
        :complete="e1 > 2"
        step="2"
      >
        Name of step 2
      </v-stepper-step>

      <v-divider></v-divider>

      <v-stepper-step step="3">
        Name of step 3
      </v-stepper-step>
    </v-stepper-header>

    <v-stepper-items>
      <v-stepper-content step="1">
        <v-card
         
        ><Step1/></v-card>

       <Center>
          <v-btn
          color="primary"
          @click="e1 = 2"
        >
        
          Continue
          
        </v-btn>
        </Center>

       
      </v-stepper-content>

      <v-stepper-content step="2">
        <v-card
          
        ><Step2/></v-card>

       <Center>
        <v-btn
          color="primary"
          @click="e1 = 3"
        >
          Continue
        </v-btn>
       </Center>

        
      </v-stepper-content>

      <v-stepper-content step="3">
        <v-card
          
        ><Step3/></v-card>

        <Center>
        <v-btn
          color="primary"
          @click="e1 = 1"
        >
          Continue
        </v-btn>
        </Center>

        
      </v-stepper-content>
    </v-stepper-items>
  </v-stepper>
</template>
<script>
import Step1 from './Step1.vue';
import Step2 from './Step2.vue';
import Step3 from './Step3.vue';
export default {
    name: 'Stepper',
     components: {
    Step1, Step2, Step3
  },
    data () {
      return {
        e1: 1,
      }
    },
  
    
    
}
</script>
<style scoped>
#regForm {
  background-color: #ffffff;
  margin: 100px auto;
  padding: 40px;
  width: 70%;
  min-width: 300px;
}

/* Style the input fields */
input {
  padding: 10px;
  width: 100%;
  font-size: 17px;
  font-family: Raleway;
  border: 1px solid #aaaaaa;
}

/* Mark input boxes that gets an error on validation: */
input.invalid {
  background-color: #ffdddd;
}

/* Hide all steps by default: */
.tab {
  display: none;
}

/* Make circles that indicate the steps of the form: */
.step {
  height: 15px;
  width: 15px;
  margin: 0 2px;
  background-color: #bbbbbb;
  border: none;
  border-radius: 50%;
  display: inline-block;
  opacity: 0.5;
}

/* Mark the active step: */
.step.active {
  opacity: 1;
}

/* Mark the steps that are finished and valid: */
.step.finish {
  background-color: #4CAF50;
}

</style>