<template>
  <div id="app">
  111
  </div>
</template>

<script>

export default {
  methods:{
    test(){ 
 
//※※※※※※※※※※※测试4※※※※※※※※※※※※※※ 
var arrayLike = { 
0 : '司徒正美', 
1 : '司徒正美', 
2 : '司徒正美', 
length : 3 
}; 
alert(arrayLike) 
arrayLike = Array.prototype.slice.call(arrayLike); 
alert(arrayLike instanceof Array); 
alert(arrayLike); 
  }
  }
,mounted(){
  this.test()
}
}
</script>

<style>
 
</style>









