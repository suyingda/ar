<template>
  <div id="app">


   {{arrarr}}<br/>a
   <div v-for="(ll,index,indexd) in arrarr"  >
     i  am  index{{indexd}}<br/>
     i am is  title: {{ll[0].name}}
     <div v-for="l in ll"  >
       <li v-for="iii in l">{{iii}}</li>
     </div>
   </div>
   <br/>
   <span v-for='data2 in groupOrderData2'> {{data2}}</span>
 </div>
 
</template>

<script>


  export default {
    name: 'app',
    data(){
      return {
        arrarr:{},
        groupOrderData2:{},
        arr:[
        {"name":"suyingda","age":23,'b':1},
        {"name":"maomao","age":33,'b':1},
        {"name":"suyingda","age":13,'b':22},
        {"name":"tankang","age":63,'b':22},
        {"name":"maomao","age":43,'b':56},
        {"name":"xiaoli","age":3,'b':77},
        ]
      }
    }
    ,
    methods:{
      abc(){
        var  groupOrderData={};  //进行大分类
var groupOrderData2={}; //再分类
this.arr.forEach((v) =>
{
  !groupOrderData[v.name] && (groupOrderData[v.name] = []);
  groupOrderData[v.name].push(v);

  !groupOrderData2[v.b] && (groupOrderData2[v.b] = []);
//  groupOrderData2[v.b].push(v);

});
this.arrarr=groupOrderData;
console.log(groupOrderData2)
for(var i in groupOrderData2)
  this.groupOrderData2[i]=i
}
}
,mounted(){
  this.abc();
}

}
</script>

<style>

</style>
