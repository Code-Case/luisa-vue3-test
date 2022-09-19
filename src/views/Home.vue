<template>
  <Luisa :design="design" :config="config" v-model="viewModel"/>
</template>
<script>
/**
 * Here is the downloaded figma file. To download yours, type in the command line
 * node download.js.
 */
import app from './app.json'

/**
 * Import mdi fonts if you are using quant-ux designs
 */
//import '@mdi/font/css/materialdesignicons.css'


export default {
  name: 'Home',
  data: function() {
    return {
      design: app,
      viewModel: {
        name:'',
        result: ''
      },
      config: {
          responsive: [
            { value: "Desktop", label: "Desktop", types: ["desktop"] },
            { value: "Tablet", label: "Tablet", types: ["tablet"] },
            { value: "Mobile", label: "Mobile", types: ["mobile"] },
        ],
      }
    }
  },
  components: {
  },
  methods: {
    sayHello () {
      this.viewModel.result = "Hello " + this.viewModel.name
    }
  }
}
</script>