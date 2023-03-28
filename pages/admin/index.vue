<template>
    <div style="padding: 20px;">
      <principal/>
    </div>
  </template>
  
  <script>
  import principal from '../../components/admin/principal.vue';
  export default {
    auth: true,
    layout: 'admin',
    components: {
      principal
    }
  }
  </script>