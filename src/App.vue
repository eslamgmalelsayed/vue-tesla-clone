<template>
<div>
  <navBar />
  <sectionComp
  v-for=" ({id, title, desc, link, image}) in sectionData"
  :key="id"
  :title="title" 
  :desc='desc' 
  :link='link'
  :image='image'
  />
  <footerComp />
</div>
</template>

<script>
import navBar from './components/nav-footer/navBar.vue'
import footerComp from './components/nav-footer/footerComp.vue'
import sectionComp from './components/section/sectionComp.vue'

export default {
  name: 'App',
  components:{
    navBar,
    footerComp,
    sectionComp
  },
  data() {
    return {
      sectionData:{
        fisrt: {
          id: 1,
          title: 'model 3',
          desc: 'Order Online for',
          link: 'Touchless Delivery',
          image: 'url(https://tesla-cdn.thron.com/delivery/public/image/tesla/538ac149-d103-4834-9d38-641d8ae447ef/bvlatuR/std/4096x2560/Homepage-Model-S-Desktop-LHD)',
        },
        second: {
          id: 2,
          title: 'model y',
          desc: 'Order Online for',
          link: 'Touchless Delivery',
          image: 'url(https://tesla-cdn.thron.com/delivery/public/image/tesla/8e2df1b9-a4bf-4eb9-beec-2cf5cc77fca0/bvlatuR/std/2880x2400/Desktop-ModelY?quality=70)',
        },
        third: {
          id: 3,
          title: 'model s',
          desc: 'Order Online for',
          link: 'Touchless Delivery',
          image: 'url(https://tesla-cdn.thron.com/delivery/public/image/tesla/03e533bf-8b1d-463f-9813-9a597aafb280/bvlatuR/std/4096x2560/M3-Homepage-Desktop-LHD)',
        },
        four: {
          id: 4,
          title: 'model x',
          desc: 'Order Online for',
          link: 'Touchless Delivery',
          image: 'url(https://tesla-cdn.thron.com/delivery/public/image/tesla/ddc135ed-1638-40fb-8ab1-f8045059ecef/bvlatuR/std/4096x2560/Homepage-Model-X-Desktop-LHD)',
        },
        five: {
          id: 5,
          title: 'Solar Panels',
          desc: 'Lowest Cost Solar Panels in America ',
          link: '',
          image: 'url(https://tesla-cdn.thron.com/delivery/public/image/tesla/16b04537-a4be-4bf9-8637-86862a858da8/bvlatuR/std/2880x1800/_25-HP-SolarPanels-D)',
        },
        six: {
          id: 6,
          title: 'Solar Panels',
          desc: 'Lowest Cost Solar Panels in America ',
          link: '',
          image: 'url(https://tesla-cdn.thron.com/delivery/public/image/tesla/4a41ec0e-7316-46a8-8ce9-e2f195ba644d/bvlatuR/std/2880x1800/Homepage-SolarRoof-Desktop-Global?quality=auto-medium&format=auto)',
        },
        seven: {
          id: 7,
          title: 'Solar Panels',
          desc: 'Lowest Cost Solar Panels in America ',
          link: '',
          image: 'url(https://tesla-cdn.thron.com/delivery/public/image/tesla/dd739764-bcaa-4263-9488-8c73bc9fb046/bvlatuR/std/0x0/dd739764-bcaa-4263-9488-8c73bc9fb046)',
        }
        }
    }
  }
}
</script>

<style lang='scss'>
*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  text-transform: capitalize;
  font-family: 'Roboto', sans-serif;
}
</style>
