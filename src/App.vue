<template>
  <main>
    <custom-header/>
    <sites-panel/>
    <hr/>
    <router-view class="container"/>
    <hr/>
    <custom-footer/>
  </main>
</template>

<script>
import CustomHeader from '@/components/CustomHeader'
import SitesPanel from '@/components/SitesPanel'
import CustomFooter from '@/components/CustomFooter'

export default {
  name: 'App',
  components: {
    CustomHeader,
    SitesPanel,
    CustomFooter
  }
}
</script>

<style>
  body {
      background-color: var(--back-color);
      margin: unset;
      font-family: 'FontAwesome';
      overflow-x: hidden;
      overflow-y: auto;
  }
</style>
