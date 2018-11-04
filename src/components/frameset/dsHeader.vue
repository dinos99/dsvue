<template>
  <div class="topHeaderWrap">
    <div class="topHeader">
      <v-tabs v-model="acmenu" color="primary" slider-color="white">
        <v-tab
          v-for="item in items"
          :style="'padding:0 15px'"
          :key="item"
        >
          {{ item }}
        </v-tab>
      </v-tabs>
    </div>
  </div>
</template>

<script>
export default {
  name: 'dsHeader',
  data: () => ({
    acmenu: 0,
    items: [
      'Home', 'Blog', 'Study', 'Diary', 'Playground'
    ]
  })
}
</script>
<style>
  .topHeaderWrap { width: 100%;}
  .topHeader { width: 600px; max-width:700px; margin:0 auto;}
</style>

