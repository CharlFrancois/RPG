<template>
  <div class="select-gender ">
      <img src="@/assets/skill1.png"/>
    <div>
      <div class="right">
        <button type="button" id="male" value="Homme" @click="selectBtn('Homme')">
          Homme
        </button>
        <br>
        <button type="button" id="male" value="Femme" @click="selectBtn('Femme')"> 
          Femme
        </button>
      </div>
      <br>
      <div class="input">
        <input type="text" placeholder="Pseudo"/>
    </div>
    
    </div>
    
  </div>
</template>

<script>
  export default {
    name: 'SelectGender',
    methods:{
      selectBtn(gender){
        console.log(gender)
      }
    }
  }
</script>

<style lang="scss" scoped>
  .select-gender {
    display: flex;
    background: rgba(black, 0.7);
    border-radius: 10px;
    padding: 3rem 2rem 3rem 2rem;
    button{
      padding: 1rem 2rem 1rem 2rem;
      background-color: #BCAE3F;
      color: #fff;
      border: none;
      border-radius: 15px;
      box-shadow: 7px 6px 23px 1px rgba(0,0,0,0.75);
      margin-right: 5%;
    }

    .input{
       padding: 1rem 2rem 1rem 2rem;
        border: none;
        border-radius: 15px;
        box-shadow: 7px 6px 23px 1px rgba(0,0,0,0.75);
        margin-right: 5%;
        margin-top: 25%;
    }
    .card{
     
        border: none;
        border-radius: 15px;
        box-shadow: 7px 6px 23px 1px rgba(0,0,0,0.75);

    }
    .right{
      display: flex;

    }
  }
</style>
