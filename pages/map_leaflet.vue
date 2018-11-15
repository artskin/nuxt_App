<template>
  <section class="container">
    <div>
      <logo/>
      <h1 class="title">
        nuxt_App
      </h1>
      <div 
        id="map-wrap" 
        style="height: 400px;width:600px;"
      >
        <no-ssr>
          <l-map
            :zoom="13"
            :center="[47.413220, -1.219482]"
          >
            <l-tile-layer url="http://{s}.tile.osm.org/{z}/{x}/{y}.png" />
            <l-marker :lat-lng="[47.413220, -1.219482]"/>
          </l-map>
        </no-ssr>
      </div>
    </div>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: { Logo }
}
</script>

<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
