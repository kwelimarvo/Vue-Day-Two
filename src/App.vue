<script>
export default {
  data() {
    return {
      activeColor: 'red',
      fontSize: 30,
      activeClass: 'active',
      errorClass: 'text-danger',
      paddingBottom: 'py-8',
      tcenter: 'text-center',
      mbottom: 'mb-3',

      cloudy: true,
      interns: ['Marvin', 'Savelline', 'Evans', 'Steve'],
    }
  }
}
</script>

<template>
  <div :class="[activeClass, paddingBottom, tcenter, mbottom, container]">Class Binding</div>
  <div :style="{ backgroundColor: activeColor, fontSize: fontSize + 'px' }" class="text-center">Style Binding</div>

  <div class="text-center">
    <h2 class="font-extrabold mt-4 bg-green-300 p-6">Conditional Rendering</h2>
    
    <p v-if="cloudy">It is cloudy today</p>
    <p v-else>There are no clouds today</p>
  </div>
  
  
  <div class="text-center">
    <h2 class="font-extrabold mt-4 bg-yellow-300 p-6">List Rendering</h2>
      <ul>
        <li v-for="intern in interns">{{intern}}</li>
      </ul>
  </div>

</template>

<style scoped>
  .active {
    background-color:aqua;
  }
</style>