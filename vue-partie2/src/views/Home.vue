<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <!-- <ContactList :list="contactList"></ContactList> -->
      <div class="demo">
      <button
        v-for="tab in tabs"
        :key="tab"
        :class="['tab-button', { active: currentTab === tab }]"
        @click="currentTab = tab"
      >
        {{ tab }}
      </button>
      <component :is="currentTab" :list="contactList" @saveInfo="save" class="tab"></component>
      </div>
  </div>
</template>

<script>
// @ is an alias to /src
import ContactList from '@/components/contactList.vue'
import Addcontact from '@/components/Addcontact.vue'


export default {
  name: 'Home',
  components:{
    ContactList, 
    Addcontact,
  },
  
  data() {
    return {
      currentTab: 'ContactList',
      tabs: ['ContactList','Addcontact'],
       contactList:[
        {
          id:1,
          name:"jbeli basma",
          email:"jbelibasma22@gmail.com",
          phone:"58662695",
          address:{
            street:"lmsmjfg",
            city:"jfqhff",

        },
        },
           {
          id:2,
          name:"jbeli hannen",
          email:"jbelihannen22@gmail.com",
          phone:"58662695",
          address:{
            street:"lmsmjfg",
            city:"jfqhff",
        },
        },
           {
          id:3,
          name:"jbeli amal",
          email:"jbeliamal22@gmail.com",
          phone:"58662695",
          address:{
            street:"lmsmjfg",
            city:"jfqhff",

        }
        }
        ],
      methods:{
        save(obj){
            this.contactList=obj;

           
            
        }
    }
        
    }
    
  },
 
}
</script>
