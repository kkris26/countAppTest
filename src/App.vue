<script setup>
import { ref } from 'vue';

const count = ref(0)
const addToCount = () =>{
  count.value = count.value+1

}
const subToCount =() =>{
  count.value = count.value-1
}


</script>

<template>
  <main>

    <div>
      <h1 id = 'number'>{{count}}</h1>
      <button @click="addToCount()">+</button>
      <button @click="subToCount">-</button>
    </div>
  </main>
</template>



<style scoped>
main{
  height: 100vh;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}

#number {
  font-size: 70px;
  text-align: center;
}

button{
  padding: 10px 20px;
}

@media (max-width: 768px){
  button{

    padding: 8px 14px;
    border: 2px solid green;
    margin: 0 2px;
  }
  
}
</style>
