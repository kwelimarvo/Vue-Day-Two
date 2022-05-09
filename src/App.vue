<script>
export default {
  data() {
    return {
            brand:'Nissan', model:'Skyline', reg_year:2018
    }
  },

  // Computed properties
  computed:{
            car_age(){
                return new Date().getFullYear() - this.reg_year
            },
            full_name:{
                get(){
                    return this.brand+' '+this.model
                },
                set(newName){
                    this.brand = newName[0]
                    this.model = newName[1]
                }
            }
        }
}
</script>

<template>

  <h1><b>{{brand}}</b> <i>{{model}}</i> <span>{{reg_year}}</span></h1>
  <h2>Age: {{car_age}}</h2>

</template>

<style scoped>
b{color:#46ea0f}
i{color:#6fddff}
span{color:#C34A36}
h2{background-color:#e61739;color:#F9F871;padding:5px;text-align:center;font-size:42px}
</style>