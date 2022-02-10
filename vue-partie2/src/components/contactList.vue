
<template>
  <ul class="list-group">
  <li class="list-group-item" v-for="contact in list" v-bind:key="contact.id">
    {{ contact.name }}
  </li>
</ul>
</template>

<script>
// import Home from '@/views/Home.vue'


export default {
    name:'contactList',
    props: {
    list: Array
  },
}
</script>

<style>

</style>