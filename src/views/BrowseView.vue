<script setup lang="ts">
// If you are using PurgeCSS, make sure to whitelist the carousel CSS classes
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'
import TamarackCase1 from '@/assets/tamarack-case-1.png'
import TamarackCase2 from '@/assets/tamarack-case-2.png'
import TamarackCase3 from '@/assets/tamarack-case-3.png'
import TamarackCase4 from '@/assets/tamarack-case-4.png'
import TamarackCase5 from '@/assets/tamarack-case-5.png'
import TamarackCase6 from '@/assets/tamarack-case-6.png'
import TamarackCpuCooler from '@/assets/tamarack-cpu-cooler.png'
import TamarackCpu from '@/assets/tamarack-cpu.png'
import TamarackMotherboard from '@/assets/tamarack-motherboard.png'
import TamarackPsu from '@/assets/tamarack-psu.png'
import TamarackRam from '@/assets/tamarack-ram.png'
import TamarackSsd from '@/assets/tamarack-ssd.png'

const pcImages = [
  TamarackCase1,
  TamarackCase2,
  TamarackCase3,
  TamarackCase4,
  TamarackCase5,
  TamarackCase6,
  TamarackCpuCooler,
  TamarackCpu,
  TamarackMotherboard,
  TamarackPsu,
  TamarackRam,
  TamarackSsd
]

const config = {
  itemsToShow: 1
}
</script>

<template>
  <div class="carousel-wrapper">
    <h1>The Tamarack</h1>
    <h3>$1350</h3>
    <ul>
      <li>CPU: AMD Ryzen 5 7600X (6-core, 12-thread, AM5, unlocked for overclocking)</li>
      <li>GPU: GIGABYTE Radeon RX 7800 XT Gaming OC (16GB GDDR6, PCIe 4.0)</li>
      <li>Motherboard: GIGABYTE B650M GAMING PLUS WiFi (AM5, DDR5, PCIe 4.0, Wi-Fi 6E, USB-C)</li>
      <li>RAM: Patriot Viper Venom 32GB (2x16GB) DDR5 6000MHz, CL36</li>
      <li>Storage: Corsair MP600 Core XT 1TB NVMe SSD (PCIe 4.0, 5000MB/s read speeds)</li>
      <li>Case: Phanteks XT Pro Ultra Mid-Tower (high airflow, tempered glass, USB-C)</li>
      <li>PSU: MSI MAG A750GL (750W, 80+ Gold, fully modular, PCIe 5.0 ready)</li>
      <li>CPU Cooler: Cooler Master Hyper 212 Spectrum V3 (ARGB, efficient cooling)</li>
    </ul>

  <Carousel v-bind="config">
    <Slide v-for="(image, index) in pcImages" :key="index">
      <img :src="image" :alt="'PC Image ' + (index + 1)" class="carousel-image" />
    </Slide>

    <template #addons>
      <Navigation />
      <Pagination />
    </template>
  </Carousel>
  </div>
</template>

<style scoped>
.carousel-wrapper {
  max-width: 100%; /* Ensure it doesn't exceed screen width */
  width: 90%; /* Set a responsive width */
  margin: auto; /* Center the carousel */
  overflow: hidden; /* Prevent any accidental overflow */
}

.carousel-image {
  width: 100%; /* Ensure images scale to fit their container */
  height: auto;
  object-fit: cover;
  border-radius: 10px; /* Optional: Rounded corners */
}
</style>
