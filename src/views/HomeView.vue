<template>
  <div class="home">
    Home
    <p>{{name}} sdsdisd sdsds {{age}}</p>
    <button @click="handleClick">Clicked</button>
  </div>
</template>

<script>

export default {
  name: 'HomeView',
  setup(){
    

    let name = 'mario'
    let age = 28

    const handleClick = () => {
      console.log('Clicked');
    }
    return {name, age, handleClick}
  }
}
</script>
