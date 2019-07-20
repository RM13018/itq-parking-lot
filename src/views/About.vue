<template>
  <div class="about">
    <div class = "container">
    <Parking/>
    </div>
    <div>
    <Parking2/>
  </div>
  </div>
</template>

<script>
import Parking from '@/components/Parking.vue'
export default {
  name: 'about',
  components:{
    Parking
  }
}
</script>
