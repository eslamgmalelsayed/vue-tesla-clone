<template>
<div :class="show && 'blur'">
  <!-- side bar -->
  <sideBarComp :toggler='toggler' :show='show' />
  <!-- nav bar -->
  <navBar :toggler='toggler' />
  <!-- section -->
  <sectionComp
    :hideSideBar='hideSideBar'
    v-for=" ({id, title, desc, link, image}) in sectionData"
    :key="id"
    :title="title" 
    :desc='desc' 
    :link='link'
    :image='image'
    :id='id'
  />
  <a href="#2" class="x"></a>
  <!-- footer -->
  <footerComp />
</div>
</template>

<script>
// imports
import navBar from './components/nav-footer/navBar.vue'
import footerComp from './components/nav-footer/footerComp.vue'
import sectionComp from './components/section/sectionComp.vue'
import sideBarComp from './components/sideBarComp.vue'

export default {
  name: 'App',
  components:{
    navBar,
    footerComp,
    sectionComp,
    sideBarComp
  },
  data() {
    return {
      sectionData:[
        {
          id: 1,
          title: 'model 3',
          desc: 'Order Online for',
          link: 'Touchless Delivery',
          image: 'url(https://tesla-cdn.thron.com/delivery/public/image/tesla/03e533bf-8b1d-463f-9813-9a597aafb280/bvlatuR/std/4096x2560/M3-Homepage-Desktop-LHD)',
        },
        {
          id: 2,
          title: 'model y',
          desc: 'Order Online for',
          link: 'Touchless Delivery',
          image: 'url(https://tesla-cdn.thron.com/delivery/public/image/tesla/8e2df1b9-a4bf-4eb9-beec-2cf5cc77fca0/bvlatuR/std/2880x2400/Desktop-ModelY?quality=70)',
        },
        {
          id: 3,
          title: 'model s',
          desc: 'Order Online for',
          link: 'Touchless Delivery',
          image: 'url(https://tesla-cdn.thron.com/delivery/public/image/tesla/538ac149-d103-4834-9d38-641d8ae447ef/bvlatuR/std/4096x2560/Homepage-Model-S-Desktop-LHD)',
        },
        {
          id: 4,
          title: 'model x',
          desc: 'Order Online for',
          link: 'Touchless Delivery',
          image: 'url(https://tesla-cdn.thron.com/delivery/public/image/tesla/ddc135ed-1638-40fb-8ab1-f8045059ecef/bvlatuR/std/4096x2560/Homepage-Model-X-Desktop-LHD)',
        },
        {
          id: 5,
          title: 'Solar Panels',
          desc: 'Lowest Cost Solar Panels in America ',
          link: '',
          image: 'url(https://tesla-cdn.thron.com/delivery/public/image/tesla/16b04537-a4be-4bf9-8637-86862a858da8/bvlatuR/std/2880x1800/_25-HP-SolarPanels-D)',
        },
        {
          id: 6,
          title: 'Solar Panels',
          desc: 'Lowest Cost Solar Panels in America ',
          link: '',
          image: 'url(https://tesla-cdn.thron.com/delivery/public/image/tesla/4a41ec0e-7316-46a8-8ce9-e2f195ba644d/bvlatuR/std/2880x1800/Homepage-SolarRoof-Desktop-Global?quality=auto-medium&format=auto)',
        },
        {
          id: 7,
          title: 'Solar Panels',
          desc: 'Lowest Cost Solar Panels in America ',
          link: '',
          image: 'url(https://tesla-cdn.thron.com/delivery/public/image/tesla/dd739764-bcaa-4263-9488-8c73bc9fb046/bvlatuR/std/0x0/dd739764-bcaa-4263-9488-8c73bc9fb046)',
        }
        ],
        show: false,
    }
  },
  methods:{
    // hide side bar
    hideSideBar(){
      console.log('xx')
      this.show = false
    },
    // toggle side bar
    toggler(){
      this.show = !this.show
    }
  }
}
</script>

<style lang='scss'>
// base
*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  text-transform: capitalize;
  font-family: 'Roboto', sans-serif;
  scroll-behavior: smooth;
}
// overlay blur
.blur{
  height: 100vh;
  overflow: hidden;
  &::before{
  content: '';
  position: absolute;
  width: 100%;
  height: 100%;
  pointer-events: none;
  overflow: hidden;
  top: 0;
  left: 0;
  backdrop-filter: blur(6px);
  background: rgba(0,0,0,.3);
  z-index: 1010;
  }
}
 .x{
        &:after{
            content: '⌵';
            position: absolute;
            width: 20px;
            height: 20px;
            top: 90%;
            left: 49%;
            font-weight: bold;
            font-size: 1.7rem;
            color: #000;
            animation: bounce 1s linear infinite;
        }
    }
  // animation
  @keyframes bounce {
      0%{
          transform: translateY(-4px);
      }
      25%{
          transform: translateY(2px);
      }
      50%{
          transform: translateY(-4px);
      }
      100%{
          transform: translateY(4px);
      }
  }
</style>
