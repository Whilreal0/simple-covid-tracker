<template>
  <div class="home">
    <main class="pt-10">
      <!-- <HeaderTitle :text="Title" /> -->
      <!-- <CountrySelect /> -->
      <DataCard :stats="stats"/>
      
    </main>

<!--  -->
 
<!--  -->
  </div>
</template>

<script>
import axios from "axios";
const apiUrl = "https://disease.sh/v3/covid-19/countries/ph";

import HeaderTitle from "@/components/HeaderTitle";
import CountrySelect from "@/components/CountrySelect";
import DataCard from "@/components/DataCard";
// @ is an alias to /src

export default {
  name: "HomeView",
  components: {
    HeaderTitle,
    CountrySelect,
    DataCard,
  },
  data: () => ({
    allData: null,
    isLoading: false,
    Title: "Philippines",
    date: {},
    countries: [],
    stats: [],

   selectedCountry: 'ph'
   
    
  }),

  methods: {
    async getData() {
      const self = this;
      axios.get(`${apiUrl} `).then(function (response) {
        self.stats = response.data;
        console.log(self.stats);
      });
    },

  },
  
  created() {
    this.getData();

 

  },
  
};
</script>
