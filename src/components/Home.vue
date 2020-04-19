<template>
<div>
    <div>
<h2>Addresses </h2>
<ul id="menu-standard">
    <li id="menu-standard" v-for="item in myJson.addresses" v-bind:key="item" >
      <div  v-for="(value, key) in item" v-bind:key="key">
        <tr><td> <strong>{{key}} : </strong></td><td> {{value}} </td></tr>
      </div>
    </li>
  </ul>

<!--
<h2>Transaction Details </h2>
<ul id="menu-standard">
    <li id="menu-standard" v-for="item in myJson.paymentMethods" v-bind:key="item" >
      <div  v-for="(value, key) in item" v-bind:key="key">
        <tr><td> <strong>{{key}} : </strong></td><td> {{value}} </td></tr>
      </div>
    </li>
  </ul> -->

  {{ keys }}
    </div>
</div>
  
</template>

<script>
import json from './test.json'
import djson from './test_expectedAddressJson.json'
//import axios from "axios";


export default {
  name: 'Home',
  props: {
   // msg: String,
    //myJson: json
  },
  data(){
      return{
          myJson: json,
          metric: null,
          addresses: null,
          myAdd: djson,
          //hson
      }
  }
  
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#menu-standard { 
    float: left;
}


</style>
