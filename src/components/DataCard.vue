<template>
  <div
    class="
      px-5
      md:px-16
      lg:px-[10rem]
      xl:px-[18rem]
      bg-custom
      flex flex-col
      items-center
      justify-center
    "
  >
    <div
      class="
        grid grid-cols-2
        gap-2
        md:gap-3.5
        justify-center
        items-center
        w-full
        max-w-[672px]
      "
    >
      <!-- Cases -->
      <div
        class="
          custom-shadow
          text-[#bfd4e9]
          h-32
          rounded-md
          max-h-[250px] max-w-[329px]
          p-5
          pt-3
        "
      >
        <h3 class="font-semibold text-red-300 pb-2">Cases</h3>
        <div class="flex flex-col">
          <span class="text-[10px] uppercase" v-if="stats">
            Latest:&nbsp;
            <span class="text-red-300  font-bold text-base">
              {{ parseInt(stats.todayCases).toLocaleString() }}
              
            </span>
          </span>
            
          <span class="text-[10px] uppercase">
            Total:&nbsp;
            <span class="text-red-300 font-bold text-base">
              {{parseInt(stats.cases).toLocaleString()}}
            </span>
          </span>
          
        </div>
      </div>
      <!-- Recoveries -->
      <div
        class="custom-shadow text-[#bfd4e9] h-32 rounded-md max-h-[250px] max-w-[329px] p-5 pt-3"
      >
        <h3 class="text-green-300 font-semibold pb-2">Recovered</h3>
        <div class="flex flex-col">
          <span class="text-[10px] uppercase">
            Latest:&nbsp;
            <span class=" text-green-300 text-base uppercase">
              {{parseInt(stats.todayRecovered).toLocaleString()}}
            </span>
          </span>
          <span class="text-[10px] uppercase">
            Total:&nbsp;
            <span class=" text-green-300 text-base uppercase">
              {{parseInt(stats.recovered).toLocaleString()}}
            </span>
          </span>
        </div>
      </div>
      <!-- Deaths -->
      <div
        class="
          custom-shadow
          text-[#bfd4e9]
          h-32
          rounded-md
          max-h-[250px] max-w-[329px]
          p-5
          pt-3
        "
      >
        <h3 class="font-semibold text-gray-300 pb-2">Deaths</h3>
        <div class="flex flex-col">
          <span class="text-[10px] uppercase">
            Latest:&nbsp;
            <span class="text-gray-300  font-bold text-base">
              
              {{parseInt(stats.todayDeaths).toLocaleString()}}
            </span>
          </span>
            
          <span class="text-[10px] uppercase">
            Total:&nbsp;
            <span class="text-gray-300 font-bold text-base">
              {{parseInt(stats.deaths).toLocaleString()}}
            </span>
          </span>
          
        </div>
      </div>
      <!-- active cases -->
      <div
        class="custom-shadow text-[#bfd4e9] h-32 rounded-md max-h-[250px] max-w-[329px] p-5 pt-3"
      >
        <h3 class="font-semibold text-red-500 pb-2">Active </h3>
        <div class="flex flex-col">
          <span class="text-[10px] uppercase">
            Active:
              <span class="font-bold text-base text-red-500">
                {{ parseInt(stats.active).toLocaleString() }}
              </span>
            </span>
          <span class="text-[10px] uppercase">
            Critical:
              <span class="font-bold text-base text-red-500">
                {{ parseInt(stats.critical).toLocaleString() }}
              </span>
          </span>
          
        </div>
      </div>
    </div>
    
  </div>
</template>

<script>
export default {
  name: 'DataCard',
  props: ["stats"],
  data: () => ({
    eto: '9999999'
  }),

 
};
</script>

<style >
.custom-shadow {
  box-shadow: inset 3.3px 3.3px 1px #161c2e, inset -3.3px -3.3px 1px #2c3a5c;
  background: linear-gradient(145deg, #263250, #1c243a);
}
</style>
