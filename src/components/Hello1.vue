<template>
  <div id="app">
 {{arrarr}}<br/>a
               <div v-for="ll in arrarr"  >
      我是标题分组: {{ll[0].name}}
                <div v-for="l in ll"  >
               <li v-for="iii in l">{{iii}}</li>
               </div>
               </div>
  </div>
</template>

<script>


export default {
  name: 'app',
  data(){
      return {
        arrarr:{},
        arr:[
          {"name":"suyingda","age":23},
          {"name":"maomao","age":33},
          {"name":"suyingda","age":13},
          {"name":"tankang","age":63},
          {"name":"maomao","age":43},
          {"name":"xiaoli","age":3},
      ]
      }
    }
    ,
      methods:{
        abc(){
          var  groupOrderData={};
            this.arr.forEach((v) =>
                {
                    !groupOrderData[v.name] && (groupOrderData[v.name] = []);
                    groupOrderData[v.name].push(v);
                });
            console.log(groupOrderData)
           this.arrarr=groupOrderData;
        }
      }
    ,mounted(){
      this.abc();
    }
 
}
</script>

<style>
 
</style>
