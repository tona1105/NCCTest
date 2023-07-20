<template>
  <div id="app">
    <div class="width-10">
      <div class="menubar" @click="toggleMenu">
        <img src="https://cdn-icons-png.flaticon.com/512/8471/8471100.png" alt="" style="width: 30px; height: 30px;">
      </div>
      <SideBar :class="{ sidebarOpen: showMenu === true }" />
    </div>
    <div class="width-90">
      <div class="header-title">
        <div class="title">
          <img src="https://avatars.githubusercontent.com/u/57796807?s=200&v=4" alt="" class="title-img">NCC
        </div>
        <span class="title-sub">
          We do <span style="color:red">it</span> with passion
        </span>
      </div>
      <div class="content">
        <div class="content-main">
          <div class="content-lorem">
            <b style="font-size: 1.2rem;">Lorem ipsum dolor sit amet?</b>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed non dui sodales, faucibus
              libero ut, posuere felis. Donec imperdiet suscipit accumsan. Aenean consequat
              condimentum velit ut tempor. Nam porta massa in metus bibendum congue.
              Pellentesque ultrices vestibulum mattis. Aliquam egestas nunc at ullamcorper ultricies.
              Donec feugiat velit nulla, vel sodales est ullamcorper id.
            </p>
          </div>
        </div>
        <div class="content-item">
          <ItemContent :imgUrl="imgUrl[1]" class="pr-20" />
          <ItemContent :imgUrl="imgUrl[2]" class="pr-20" />
          <ItemContent :imgUrl="imgUrl[3]" />
        </div>
        <div class="footer">
          Copyright © 2021
        </div>
      </div>
    </div>

  </div>
</template>

<script>

import ItemContent from './components/ItemContent.vue'
import SideBar from './components/SideBar.vue';
export default {
  components: {
    SideBar,
    ItemContent
  },
  data() {
    return {
      showMenu: false,
      imgUrl: {
        1: 'https://st2.depositphotos.com/46079520/47507/v/1600/depositphotos_475078456-stock-illustration-css-letter-logo-design-black.jpg',
        2: 'https://media.istockphoto.com/id/1207788367/vi/vec-to/vector-thi%E1%BA%BFt-k%E1%BA%BF-logo-ch%E1%BB%AF-dw-ban-%C4%91%E1%BA%A7u-v%E1%BB%9Bi-m%C3%A0u-v%C3%A0ng-v%C3%A0-b%E1%BA%A1c-thi%E1%BA%BFt-k%E1%BA%BF-logo-dw.jpg?s=1024x1024&w=is&k=20&c=GYIJDAiZ1aEVFSFGnMkp9rSjp-vnbY_Guo9gnkkSptY=',
        3: 'https://static.vecteezy.com/system/resources/previews/008/998/006/non_2x/url-logo-url-letter-url-letter-logo-design-initials-url-logo-linked-with-circle-and-uppercase-monogram-logo-url-typography-for-technology-business-and-real-estate-brand-vector.jpg'
      }
    }
  },
  mounted() {
    // Bắt sự kiện cuộn trang
    window.addEventListener('scroll', this.handleScroll);
  },
  methods: {
     toggleMenu() {
      this.showMenu = !this.showMenu;
    },
    handleScroll() {
      // Thực hiện các xử lý khi cuộn trang xuống ở đây
      // Ví dụ: kiểm tra vị trí cuộn để hiển thị / ẩn các phần tử, v.v.
      this.showMenu = false
    }
  }
}
</script>

<style>
.width-10 {
  max-width: 10%;
}

.width-90 {
  max-width: 90%;
  text-align: center;
  padding-left: 10%;
}

.header-title {
  margin-bottom: 30px;
}

.title {
  font-size: 4rem;
  font-weight: bold;
  line-height: 0.9;
}

.title-img {
  width: 45px;
  height: 45px;
  padding-right: 4px;
}

.title-sub {
  font-size: 22px;
}

.content {
  margin-left: 50px;
  max-width: 85%;
  margin: auto;


}

.content-main {
  background-color: #EFEFEF;
  padding: 25px 0 0 0;
}

.content-lorem {
  max-width: 60%;
  margin: auto;
  padding: 20px 0;
}

.content-item {
  background-color: white;
  margin: auto;
  width: 100%;
  display: flex;
  flex-wrap: wrap;
}

.footer {
  position: relative;
  background-color: white;
  font-size: 14px;
  color: #464646;
  text-align: start;
  margin-top: 8%;
  padding: 20px 0;
}

.footer::after {
  content: '';
  position: absolute;
  top: 0;
  left: -10%;
  width: 119%;
  height: 1px;
  background-color: #c7c7c7;
}


.pr-20 {
  padding-right: 30px;
}

@media screen and (min-width: 320px) and (max-width: 767px) {
  .width-90 {
    padding-left: 0;
    margin: auto;
  }

  .pr-20 {
    padding-right: 0;
  }

  .bg-sidebar {
    width: 20%;
    display: none;

  }

  .menubar {
    height: 100%;
 
  }

  .sidebarOpen {
    display: block;
    top: 40px;
    width: 20%;
  }
}

@media screen and (min-width: 768px) and (max-width: 1200px) {
  .pr-20 {
    padding-right: 20px;
  }
}
</style>

