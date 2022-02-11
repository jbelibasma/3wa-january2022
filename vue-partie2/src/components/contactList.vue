
<template>
<div class="row ">
  <ul class="list-group col-4 offset-2">
    <router-link class="nav-link text-darck" to="#"><li class="list-group-item" v-for="contact in list" v-bind:key="contact.id"  @click="currentContact = contact">
      {{ contact.name }}
    </li></router-link>
  </ul>
  <div class="col-4 offset-2">
    
      
        <contactdetail v-if="currentContact" :contact="currentContact"></contactdetail>
      
   
  </div>

</div>

</template>

<script>
import contactdetail from './Contactdetail.vue';


export default {
    name:'contactList',
    props: {
    list: Array,
  },
  components:{
    contactdetail,
  },
  data(){
    return{
    currentContact:null,


    }
  }
}

</script>

<style>


</style>