<template>
  <form>
    <div class="mb-3">
    <label for="exampleInputPassword1" class="form-label">name</label>
    <input type="text" class="form-control" v-model="obj.name" id="name">
  </div>
  <div class="mb-3">
    <label for="exampleInputEmail1" class="form-label">Email</label>
    <input type="email" class="form-control" v-model="obj.email" id="exampleInputEmail1" aria-describedby="emailHelp">
    <div id="emailHelp" class="form-text">We'll never share your email with anyone else.</div>
  </div>
  <div class="mb-3">
    <label for="exampleInputPassword1" class="form-label">phone</label>
    <input type="text" class="form-control" v-model="obj.phone" id="phone">
  </div>
  <div class="mb-3">
    <label for="exampleInputPassword1" class="form-label">address</label>
    <input type="text" class="form-control" v-model="obj.address" id="address">
  </div>
  
  <button type="submit" class="btn btn-primary" @click.prevent="save()">Submit</button>
</form>
</template>

<script>
export default {
   name:'obj',
    props: {
    list: object,
  },
data(){
    return {
            obj:{
              name:"",
              email : "",
              phone : "",
              address:"",
            }
        }
    },
    methods:{
        save(){

            this.$emit("saveInfo",this.obj)
        }
    }

}


</script>

<style>

</style>