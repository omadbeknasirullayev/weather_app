
<script setup lang="ts">
  const items = 24

  const regions = [
    {
      name: "Tashkent",
      lat: 0,
      lon: 0
    },
    {
      name: "Andijon",
      lat: 0,
      lon: 0
    },
    {
      name: "Namangan",
      lat: 0,
      lon: 0
    },
    {
      name: "Farg'ona",
      lat: 0,
      lon: 0
    },
    {
      name: "Jizzax",
      lat: 0,
      lon: 0
    },
    {
      name: "Samarqand",
      lat: 0,
      lon: 0
    },
    {
      name: "Buxoro",
      lat: 0,
      lon: 0
    },
    {
      name: "Sirdaryo",
      lat: 0,
      lon: 0
    },
    {
      name: "Surxondaryo",
      lat: 0,
      lon: 0
    },
    {
      name: "Qashqadaryo",
      lat: 0,
      lon: 0
    },
    {
      name: "Xorazm",
      lat: 0,
      lon: 0
    },
    {
      name: "Qoraqalpag'iston",
      lat: 0,
      lon: 0
    },
    {
      name: "Navoiy",
      lat: 0,
      lon: 0
    },
  ]

  function get_infos () {
    alert("salom")
  }
</script>

<template>
  <div class="container">

    <!-- Infos weather of the city  -->
    <div id="infos">
      <div class="region_deg">

        <div class="region_deg_name">
          <h1>Toshkent shahri</h1>
          <p>Seshanba 20-Fevral</p>
          <p>-1C</p>
        </div>

        <div class="infos_image">
          <img src="./images/1.png" alt="" width="200px">
        </div>


      </div>


      <div class="hours_deg">
        <div v-for="(item, index) in items" :key="index" class="hours_deg_item">
          <p>Hozir</p>
          <p>-1C</p>
          <div>
            <img src="./images/icons/water.svg" alt="">
          </div>
        </div>
      </div>


      <div class="days_deg">

      </div>
    </div>

    <!-- regions -->
    <div id="regions">
      <h2 class="regions_title">Xududlar</h2>
      
      <label @click="get_infos" v-for="(item, index) in regions" :key="index" :for="item.name">
        <span>{{item.name}}</span>
        <input type="radio" :name="region" :id="item.name">
      </label>

    </div>
  </div>
</template>

<style scoped>

  .container {
      display: flex;
      justify-content: space-between;
      margin-top: 2rem;
  }

  #infos {
    width: 70%;
  }

  #regions {
    width: 25%;
  }

  .region_deg {
      display: flex;
      justify-content: space-between;
  }

  .region_deg_name h1 {
    color: rgb(55,69,135);
    font-size: 3rem
  }

  .region_deg_name p:nth-child(2) {
    color: rgb(55,69,135);
    font-size: 1.3rem;
  }

  .region_deg_name p:nth-child(3) {
    color: rgb(1,146,255);
    font-size: 10rem;
  }

  /* dagree of hours */

  .hours_deg {
    background-color: rgb(249,249,249);
    display: flex;
    flex-wrap: wrap;
  }

  .hours_deg_item {
    margin: .5rem 1rem;
  }

  #regions {
    display: flex;
    justify-content: space-between;
    flex-direction: column;
    background-color: rgb(249,249,249);
    padding: 1rem;
    height: 70vh;
  }

  #regions label {
    display: flex;
    justify-content: space-between;
    font-size: 25px;
  }

  #regions label input {
    width: 1.6rem;
  }

  .regions_title {
    /* text-align: center; */
  }

</style>