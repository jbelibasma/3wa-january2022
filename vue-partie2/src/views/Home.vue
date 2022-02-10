<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <ContactList :list="contactList"></ContactList>
  </div>
</template>

<script>
// @ is an alias to /src
import ContactList from '@/components/contactList.vue'

export default {
  name: 'Home',
  components:{
    ContactList, 
  },
  
  data(){
    return{
      contactList:[
        {
          id:1,
          name:"jbeli basma",
          email:"jbelibasma22@gmail.com",
          phone:"58662695",
          adress:{
            street:"lmsmjfg",
            city:"jfqhff",

        },
        },
           {
          id:2,
          name:"jbeli basma",
          email:"jbelibasma22@gmail.com",
          phone:"58662695",
          adress:{
            street:"lmsmjfg",
            city:"jfqhff",
        },
        },
           {
          id:3,
          name:"jbeli basma",
          email:"jbelibasma22@gmail.com",
          phone:"58662695",
          adress:{
            street:"lmsmjfg",
            city:"jfqhff",

        }
        }
        ]
    }
  }
}
</script>
