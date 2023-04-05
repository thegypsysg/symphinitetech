<template>


  <div>
    <v-app-bar color="white" elevation="1" fixed>
      <img class="logo-img" src="@/assets/images/logo/mall-E-original-final-2.jpg" height="90" >
      <form class="navbar__search navbar__search__desktop" >
        <input class="form-control mr-sm-2" type="text" placeholder="Type a Mall or merchant" aria-label="Search" id="product_name" data-autocompleturl="https://boozards.com/merchant-product/search">
        <button class="btn btn--search" type="submit">
          <v-icon color="white">mdi-magnify</v-icon>
        </button>
      </form>
      <div class="desktop__app">
        <v-menu >
          <template v-slot:activator="{ props }">
            <v-btn style="margin-left:30px; margin-right:30px; font-size:16px; color: #494949" v-bind="props" variant="text">
              Singapore
              <v-icon right dark>mdi-menu-down</v-icon>
            </v-btn>
          </template>
          <v-list>
            <v-list-item v-for="(item, index) in items" :key="index" :value="index">
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>

      </div>
      <v-btn
        elevation="0"
        class="btn_sign__up"
      >Sign up / Register</v-btn>
      <v-btn icon @click="drawer = !drawer">
        <img src="@/assets/images/icons/user_icon.png" height="48" width="48">
      </v-btn>

      <template class="mobile__app" v-slot:extension>
        <div class="mobile__app text-center" style="padding: 8px">
          <div>
            <v-menu >
              <template v-slot:activator="{ props }">
                <v-btn style="margin-left:30px; margin-right:30px; font-size:16px; color: #494949" v-bind="props" variant="text">
                  Singapore
                  <v-icon right dark>mdi-menu-down</v-icon>
                </v-btn>
              </template>
              <v-list>
                <v-list-item v-for="(item, index) in items" :key="index" :value="index">
                  <v-list-item-title>{{ item.title }}</v-list-item-title>
                </v-list-item>
              </v-list>
            </v-menu>
          </div>
          <form class="navbar__search navbar__search__mobile" >
            <input class="form-control mr-sm-2" type="text" placeholder="Type a Mall or merchant" aria-label="Search" id="product_name" data-autocompleturl="https://boozards.com/merchant-product/search">
            <button class="btn btn--search" type="submit">
              <v-icon color="white">mdi-magnify</v-icon>
            </button>
          </form>
        </div>
      </template>
    </v-app-bar>
    <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
      location="right"
    >
      <div class="drawer__top">
        <a style="font-size: 1.125rem; color: white" >Sign up / Register</a>
      </div>
      <div class="drawer__heading">
        <div class="drawer-logo">
          <span class="logo">MALL-</span>
          <span class="text-danger">e</span>
        </div>
        <div class="text-muted" style="font-size: 10px">
          Version 1.0
        </div>
      </div>
      <v-divider/>
      <ul
        nav
        dense
      >

        <li class="v-list-item">
          <div class="v-list-item__icon">
            <img src="@/assets/images/icons/home.png">
          </div>
          <v-list-item-title>Home</v-list-item-title>
        </li>

        <li class="v-list-item">
          <div class="v-list-item__icon">
            <img src="@/assets/images/icons/shop.png">
          </div>
          <v-list-item-title>Merchants</v-list-item-title>
        </li>

        <li class="v-list-item">
          <div class="v-list-item__icon">
            <img src="@/assets/images/icons/shopping-mall.png">
          </div>
          <v-list-item-title>Mall owner</v-list-item-title>
        </li>

        <li class="v-list-item">
          <div class="v-list-item__icon">
            <img src="@/assets/images/icons/menu-drivers.png">
          </div>
          <v-list-item-title>Drivers / Riders</v-list-item-title>
        </li>
      </ul>

      <div class="drawer__bottom">
        <div class="text-center" style="width: 100%">
          <p style="font-size: 16px; margin-bottom: 2px;">Made in Singapore</p>
          <h3 style="font-size: 13px">Get connected</h3>
          <div class="d-flex justify-center">
            <img src="@/assets/images/icons/facebook.png" height="48" width="auto">
            <img src="@/assets/images/icons/insta.png" height="48" width="auto">
          </div>
          <div class="drawer-social d-flex" style="width: 100%">
            <div>
              <h6>WhatsApp</h6>
              <a style="text-decoration: none" href="https://api.whatsapp.com/send?phone=+65.94694136&text=Hello!">
                +65 9469 4136
              </a>
            </div>
            <div>
              <h6>Contact us</h6>
              <a style="text-decoration: none" href="mailto:help@mall-e.net">help@mall-e.net</a>
            </div>
          </div>
        </div>

      </div>
    </v-navigation-drawer>
  </div>


  <v-sheet class="d-flex align-center justify-center flex-wrap text-center mx-auto" elevation="0" min-height="600"
    width="100%">
    <v-img class="bg-image" width="100%" src="@/assets/header.png" />
    <div class="jumbotron-text">

      <h1 align="center" class="header-title" style="font-size:56px; font-family: 'Nunito' !important;
font-style: normal;
font-weight: 700;">What are you Looking for.. ?</h1>
      <p class="header-title-sub" style="margin-top: 32px">The gypsy Trending Web Apps</p>
    </div>
  </v-sheet>




  <v-container align="center" class="wrapper-box">
    <v-row>
      <v-col>
        <div class="d-flex flex-row justify-center mb-6 " >
          <v-btn class="sub-menu-btn active " style="box-shadow: 0px 5px 25px rgba(0, 0, 0, 0);">
            <p style="font-size: 12px" eleva>View all</p>
            <span class="badge active">2.7K</span>
          </v-btn>
          <v-btn class="sub-menu-btn " style="box-shadow: 0px 5px 25px rgba(0, 0, 0, 0);">
            <p style="font-size: 12px; margin-left:16px;" eleva>Illustration</p>
            <span class="badge " >2.7K</span>
          </v-btn>
          <v-btn class="sub-menu-btn  flex" style="box-shadow: 0px 5px 25px rgba(0, 0, 0, 0);">
            <p style="font-size: 12px " eleva>Branding</p>
            <span class="badge ">2.7K</span>
          </v-btn>
          <v-btn class="sub-menu-btn  flex" style="box-shadow: 0px 5px 25px rgba(0, 0, 0, 0);">
            <p style="font-size: 12px" eleva>Product Design</p>
            <span class="badge ">2.7K</span>
          </v-btn>
          <v-btn class="sub-menu-btn  flex" style="box-shadow: 0px 5px 25px rgba(0, 0, 0, 0);">
            <p style="font-size: 12px" eleva>Typography</p>
            <span class="badge" >2.7K</span>
          </v-btn>
        </div>
      </v-col>
    </v-row>

    <v-row>
      <v-col cols="4">
        <v-card style="box-shadow: 0px 5px 25px rgba(0, 0, 0, 0.15); border-radius: 0px;">
          <v-img src="@/assets/gypsi-1.png" class="align-end" gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                 height="200px" cover></v-img>
          <v-card-title  class="text-black text-left" style="padding-bottom: 16px;" >Mall-e</v-card-title>
          <v-card-subtitle style="padding-bottom:32px" class="text-left">
            Promotion happening in malls
          </v-card-subtitle>
          <v-card-actions class="d-flex" style="margin-bottom:10px">
            <v-btn elevation="4" style="background-color: #FA2964; border-radius:50px; padding-left: 16px; padding-right: 16px; padding-top:10px; padding-bottom:10px">
              <span class="text-white" style="">View App</span>
              <v-icon right style="color: #fff">mdi-chevron-right</v-icon>
            </v-btn>
            <v-spacer></v-spacer>
            <div class="d-flex" >

              <!-- <v-icon style="color: #808080;">mdi-eye</v-icon> -->
              <svg align="center" width="24" height="24"   viewBox="0 0 36 36" fill="none" xmlns="http://www.w3.org/2000/svg">
                <g clip-path="url(#clip0_61_42)">
                  <path d="M33.62 17.53C30.25 11.3 24.34 7.53 17.8 7.53C11.26 7.53 5.34 11.3 2 17.53L1.72 18L1.98 18.48C5.35 24.71 11.26 28.48 17.8 28.48C24.34 28.48 30.26 24.76 33.62 18.48L33.88 18L33.62 17.53ZM17.8 26.43C12.17 26.43 7 23.29 4 18C7 12.71 12.17 9.57 17.8 9.57C23.43 9.57 28.54 12.72 31.59 18C28.54 23.29 23.42 26.43 17.8 26.43Z" fill="#808080"/>
                  <path d="M18.09 11.17C16.7341 11.1799 15.4116 11.5914 14.2894 12.3525C13.1673 13.1136 12.2958 14.1902 11.7852 15.4462C11.2745 16.7023 11.1475 18.0816 11.4203 19.4098C11.693 20.738 12.3533 21.9555 13.3176 22.9087C14.282 23.8619 15.5072 24.5079 16.8385 24.7652C18.1697 25.0225 19.5474 24.8794 20.7975 24.3542C22.0475 23.8289 23.1139 22.945 23.8619 21.8141C24.6098 20.6831 25.0059 19.3559 25 18C24.9961 17.0974 24.8141 16.2045 24.4644 15.3724C24.1148 14.5403 23.6044 13.7854 22.9625 13.1509C22.3206 12.5164 21.5598 12.0148 20.7236 11.6749C19.8875 11.335 18.9925 11.1634 18.09 11.17ZM18.09 22.89C17.1323 22.8801 16.1988 22.5875 15.4068 22.0488C14.6148 21.5101 13.9997 20.7495 13.6386 19.8623C13.2776 18.9752 13.1867 18.0012 13.3774 17.0625C13.5681 16.1239 14.0319 15.2626 14.7106 14.5867C15.3892 13.9108 16.2524 13.4505 17.1918 13.2637C18.1312 13.0768 19.1049 13.1716 19.9905 13.5363C20.8762 13.901 21.6343 14.5192 22.1698 15.3134C22.7052 16.1076 22.994 17.0422 23 18C23.0027 18.6446 22.8773 19.2833 22.6313 19.8791C22.3852 20.4749 22.0233 21.0159 21.5666 21.4708C21.1099 21.9257 20.5674 22.2853 19.9706 22.529C19.3738 22.7726 18.7346 22.8953 18.09 22.89Z" fill="#808080"/>
                </g>
                <defs>
                  <clipPath id="clip0_61_42">
                    <rect width="36" height="36" fill="white"/>
                  </clipPath>
                </defs>
              </svg>
              <span align="center" style="color: #808080; padding-right:16px">1336</span>

            </div>
          </v-card-actions>
        </v-card>
      </v-col>
      <v-col cols="4">
        <v-card style="box-shadow: 0px 5px 25px rgba(0, 0, 0, 0.15); border-radius: 0px;">
          <v-img src="@/assets/gypsy-2.png" class="align-end" gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                 height="200px" cover></v-img>
          <v-card-title class="text-black text-left" style="padding-bottom: 16px;">Boozards</v-card-title>
          <v-card-subtitle style="padding-bottom:32px" class="text-left">
            Marketplace for booz
          </v-card-subtitle>
          <v-card-actions class="d-flex" style="margin-bottom:10px">
            <v-btn elevation="4" style="background-color: #FA2964; border-radius:50px; padding-left: 16px; padding-right: 16px; padding-top:10px; padding-bottom:10px">
              <span class="text-white" style="">View App</span>
              <v-icon right style="color: #fff">mdi-chevron-right</v-icon>
            </v-btn>
            <v-spacer></v-spacer>
            <div class="d-flex" >

              <!-- <v-icon style="color: #808080;">mdi-eye</v-icon> -->
              <svg align="center" width="24" height="24"   viewBox="0 0 36 36" fill="none" xmlns="http://www.w3.org/2000/svg">
                <g clip-path="url(#clip0_61_42)">
                  <path d="M33.62 17.53C30.25 11.3 24.34 7.53 17.8 7.53C11.26 7.53 5.34 11.3 2 17.53L1.72 18L1.98 18.48C5.35 24.71 11.26 28.48 17.8 28.48C24.34 28.48 30.26 24.76 33.62 18.48L33.88 18L33.62 17.53ZM17.8 26.43C12.17 26.43 7 23.29 4 18C7 12.71 12.17 9.57 17.8 9.57C23.43 9.57 28.54 12.72 31.59 18C28.54 23.29 23.42 26.43 17.8 26.43Z" fill="#808080"/>
                  <path d="M18.09 11.17C16.7341 11.1799 15.4116 11.5914 14.2894 12.3525C13.1673 13.1136 12.2958 14.1902 11.7852 15.4462C11.2745 16.7023 11.1475 18.0816 11.4203 19.4098C11.693 20.738 12.3533 21.9555 13.3176 22.9087C14.282 23.8619 15.5072 24.5079 16.8385 24.7652C18.1697 25.0225 19.5474 24.8794 20.7975 24.3542C22.0475 23.8289 23.1139 22.945 23.8619 21.8141C24.6098 20.6831 25.0059 19.3559 25 18C24.9961 17.0974 24.8141 16.2045 24.4644 15.3724C24.1148 14.5403 23.6044 13.7854 22.9625 13.1509C22.3206 12.5164 21.5598 12.0148 20.7236 11.6749C19.8875 11.335 18.9925 11.1634 18.09 11.17ZM18.09 22.89C17.1323 22.8801 16.1988 22.5875 15.4068 22.0488C14.6148 21.5101 13.9997 20.7495 13.6386 19.8623C13.2776 18.9752 13.1867 18.0012 13.3774 17.0625C13.5681 16.1239 14.0319 15.2626 14.7106 14.5867C15.3892 13.9108 16.2524 13.4505 17.1918 13.2637C18.1312 13.0768 19.1049 13.1716 19.9905 13.5363C20.8762 13.901 21.6343 14.5192 22.1698 15.3134C22.7052 16.1076 22.994 17.0422 23 18C23.0027 18.6446 22.8773 19.2833 22.6313 19.8791C22.3852 20.4749 22.0233 21.0159 21.5666 21.4708C21.1099 21.9257 20.5674 22.2853 19.9706 22.529C19.3738 22.7726 18.7346 22.8953 18.09 22.89Z" fill="#808080"/>
                </g>
                <defs>
                  <clipPath id="clip0_61_42">
                    <rect width="36" height="36" fill="white"/>
                  </clipPath>
                </defs>
              </svg>
              <span align="center" style="color: #808080; padding-right:16px">1336</span>

            </div>
          </v-card-actions>
        </v-card>
      </v-col>
      <v-col cols="4">
        <v-card style="box-shadow: 0px 5px 25px rgba(0, 0, 0, 0.15); border-radius: 0px;">
          <v-img src="@/assets/gypsy-3.png" class="align-end" gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                 height="200px" cover></v-img>
          <v-card-title class="text-black text-left" style="padding-bottom: 16px;">Flea</v-card-title>
          <v-card-subtitle style="padding-bottom:32px" class="text-left">
            Promotion happening in street
          </v-card-subtitle>
          <v-card-actions class="d-flex" style="margin-bottom:10px">
            <v-btn elevation="4" style="background-color: #FA2964; border-radius:50px; padding-left: 16px; padding-right: 16px; padding-top:10px; padding-bottom:10px">
              <span class="text-white" style="">View App</span>
              <v-icon right style="color: #fff">mdi-chevron-right</v-icon>
            </v-btn>
            <v-spacer></v-spacer>
            <div class="d-flex" >

              <!-- <v-icon style="color: #808080;">mdi-eye</v-icon> -->
              <svg align="center" width="24" height="24"   viewBox="0 0 36 36" fill="none" xmlns="http://www.w3.org/2000/svg">
                <g clip-path="url(#clip0_61_42)">
                  <path d="M33.62 17.53C30.25 11.3 24.34 7.53 17.8 7.53C11.26 7.53 5.34 11.3 2 17.53L1.72 18L1.98 18.48C5.35 24.71 11.26 28.48 17.8 28.48C24.34 28.48 30.26 24.76 33.62 18.48L33.88 18L33.62 17.53ZM17.8 26.43C12.17 26.43 7 23.29 4 18C7 12.71 12.17 9.57 17.8 9.57C23.43 9.57 28.54 12.72 31.59 18C28.54 23.29 23.42 26.43 17.8 26.43Z" fill="#808080"/>
                  <path d="M18.09 11.17C16.7341 11.1799 15.4116 11.5914 14.2894 12.3525C13.1673 13.1136 12.2958 14.1902 11.7852 15.4462C11.2745 16.7023 11.1475 18.0816 11.4203 19.4098C11.693 20.738 12.3533 21.9555 13.3176 22.9087C14.282 23.8619 15.5072 24.5079 16.8385 24.7652C18.1697 25.0225 19.5474 24.8794 20.7975 24.3542C22.0475 23.8289 23.1139 22.945 23.8619 21.8141C24.6098 20.6831 25.0059 19.3559 25 18C24.9961 17.0974 24.8141 16.2045 24.4644 15.3724C24.1148 14.5403 23.6044 13.7854 22.9625 13.1509C22.3206 12.5164 21.5598 12.0148 20.7236 11.6749C19.8875 11.335 18.9925 11.1634 18.09 11.17ZM18.09 22.89C17.1323 22.8801 16.1988 22.5875 15.4068 22.0488C14.6148 21.5101 13.9997 20.7495 13.6386 19.8623C13.2776 18.9752 13.1867 18.0012 13.3774 17.0625C13.5681 16.1239 14.0319 15.2626 14.7106 14.5867C15.3892 13.9108 16.2524 13.4505 17.1918 13.2637C18.1312 13.0768 19.1049 13.1716 19.9905 13.5363C20.8762 13.901 21.6343 14.5192 22.1698 15.3134C22.7052 16.1076 22.994 17.0422 23 18C23.0027 18.6446 22.8773 19.2833 22.6313 19.8791C22.3852 20.4749 22.0233 21.0159 21.5666 21.4708C21.1099 21.9257 20.5674 22.2853 19.9706 22.529C19.3738 22.7726 18.7346 22.8953 18.09 22.89Z" fill="#808080"/>
                </g>
                <defs>
                  <clipPath id="clip0_61_42">
                    <rect width="36" height="36" fill="white"/>
                  </clipPath>
                </defs>
              </svg>
              <span align="center" style="color: #808080; padding-right:16px">1336</span>

            </div>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="4">
        <v-card style="box-shadow: 0px 5px 25px rgba(0, 0, 0, 0.15); border-radius: 0px;">
          <v-img src="@/assets/gypsy-4.png" class="align-end" gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                 height="200px" cover></v-img>
          <v-card-title  class="text-black text-left" style="padding-bottom: 16px;" >Mendesliga</v-card-title>
          <v-card-subtitle style="padding-bottom:32px" class="text-left">
            Market place for tournaments
          </v-card-subtitle>
          <v-card-actions class="d-flex" style="margin-bottom:10px">
            <v-btn elevation="4" style="background-color: #FA2964; border-radius:50px; padding-left: 16px; padding-right: 16px; padding-top:10px; padding-bottom:10px">
              <span class="text-white" style="">View App</span>
              <v-icon right style="color: #fff">mdi-chevron-right</v-icon>
            </v-btn>
            <v-spacer></v-spacer>
            <div class="d-flex" >

              <!-- <v-icon style="color: #808080;">mdi-eye</v-icon> -->
              <svg align="center" width="24" height="24"   viewBox="0 0 36 36" fill="none" xmlns="http://www.w3.org/2000/svg">
                <g clip-path="url(#clip0_61_42)">
                  <path d="M33.62 17.53C30.25 11.3 24.34 7.53 17.8 7.53C11.26 7.53 5.34 11.3 2 17.53L1.72 18L1.98 18.48C5.35 24.71 11.26 28.48 17.8 28.48C24.34 28.48 30.26 24.76 33.62 18.48L33.88 18L33.62 17.53ZM17.8 26.43C12.17 26.43 7 23.29 4 18C7 12.71 12.17 9.57 17.8 9.57C23.43 9.57 28.54 12.72 31.59 18C28.54 23.29 23.42 26.43 17.8 26.43Z" fill="#808080"/>
                  <path d="M18.09 11.17C16.7341 11.1799 15.4116 11.5914 14.2894 12.3525C13.1673 13.1136 12.2958 14.1902 11.7852 15.4462C11.2745 16.7023 11.1475 18.0816 11.4203 19.4098C11.693 20.738 12.3533 21.9555 13.3176 22.9087C14.282 23.8619 15.5072 24.5079 16.8385 24.7652C18.1697 25.0225 19.5474 24.8794 20.7975 24.3542C22.0475 23.8289 23.1139 22.945 23.8619 21.8141C24.6098 20.6831 25.0059 19.3559 25 18C24.9961 17.0974 24.8141 16.2045 24.4644 15.3724C24.1148 14.5403 23.6044 13.7854 22.9625 13.1509C22.3206 12.5164 21.5598 12.0148 20.7236 11.6749C19.8875 11.335 18.9925 11.1634 18.09 11.17ZM18.09 22.89C17.1323 22.8801 16.1988 22.5875 15.4068 22.0488C14.6148 21.5101 13.9997 20.7495 13.6386 19.8623C13.2776 18.9752 13.1867 18.0012 13.3774 17.0625C13.5681 16.1239 14.0319 15.2626 14.7106 14.5867C15.3892 13.9108 16.2524 13.4505 17.1918 13.2637C18.1312 13.0768 19.1049 13.1716 19.9905 13.5363C20.8762 13.901 21.6343 14.5192 22.1698 15.3134C22.7052 16.1076 22.994 17.0422 23 18C23.0027 18.6446 22.8773 19.2833 22.6313 19.8791C22.3852 20.4749 22.0233 21.0159 21.5666 21.4708C21.1099 21.9257 20.5674 22.2853 19.9706 22.529C19.3738 22.7726 18.7346 22.8953 18.09 22.89Z" fill="#808080"/>
                </g>
                <defs>
                  <clipPath id="clip0_61_42">
                    <rect width="36" height="36" fill="white"/>
                  </clipPath>
                </defs>
              </svg>
              <span align="center" style="color: #808080; padding-right:16px">1336</span>

            </div>
          </v-card-actions>
        </v-card>
      </v-col>
      <v-col cols="4">
        <v-card style="box-shadow: 0px 5px 25px rgba(0, 0, 0, 0.15); border-radius: 0px;">
          <v-img src="@/assets/gypsy-5.png" class="align-end" gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                 height="200px" cover></v-img>
          <v-card-title class="text-black text-left" style="padding-bottom: 16px;">Cake run</v-card-title>
          <v-card-subtitle style="padding-bottom:32px" class="text-left">
            Promotion happening in malls
          </v-card-subtitle>
          <v-card-actions class="d-flex" style="margin-bottom:10px">
            <v-btn elevation="4" style="background-color: #FA2964; border-radius:50px; padding-left: 16px; padding-right: 16px; padding-top:10px; padding-bottom:10px">
              <span class="text-white" style="">View App</span>
              <v-icon right style="color: #fff">mdi-chevron-right</v-icon>
            </v-btn>
            <v-spacer></v-spacer>
            <div class="d-flex" >

              <!-- <v-icon style="color: #808080;">mdi-eye</v-icon> -->
              <svg align="center" width="24" height="24"   viewBox="0 0 36 36" fill="none" xmlns="http://www.w3.org/2000/svg">
                <g clip-path="url(#clip0_61_42)">
                  <path d="M33.62 17.53C30.25 11.3 24.34 7.53 17.8 7.53C11.26 7.53 5.34 11.3 2 17.53L1.72 18L1.98 18.48C5.35 24.71 11.26 28.48 17.8 28.48C24.34 28.48 30.26 24.76 33.62 18.48L33.88 18L33.62 17.53ZM17.8 26.43C12.17 26.43 7 23.29 4 18C7 12.71 12.17 9.57 17.8 9.57C23.43 9.57 28.54 12.72 31.59 18C28.54 23.29 23.42 26.43 17.8 26.43Z" fill="#808080"/>
                  <path d="M18.09 11.17C16.7341 11.1799 15.4116 11.5914 14.2894 12.3525C13.1673 13.1136 12.2958 14.1902 11.7852 15.4462C11.2745 16.7023 11.1475 18.0816 11.4203 19.4098C11.693 20.738 12.3533 21.9555 13.3176 22.9087C14.282 23.8619 15.5072 24.5079 16.8385 24.7652C18.1697 25.0225 19.5474 24.8794 20.7975 24.3542C22.0475 23.8289 23.1139 22.945 23.8619 21.8141C24.6098 20.6831 25.0059 19.3559 25 18C24.9961 17.0974 24.8141 16.2045 24.4644 15.3724C24.1148 14.5403 23.6044 13.7854 22.9625 13.1509C22.3206 12.5164 21.5598 12.0148 20.7236 11.6749C19.8875 11.335 18.9925 11.1634 18.09 11.17ZM18.09 22.89C17.1323 22.8801 16.1988 22.5875 15.4068 22.0488C14.6148 21.5101 13.9997 20.7495 13.6386 19.8623C13.2776 18.9752 13.1867 18.0012 13.3774 17.0625C13.5681 16.1239 14.0319 15.2626 14.7106 14.5867C15.3892 13.9108 16.2524 13.4505 17.1918 13.2637C18.1312 13.0768 19.1049 13.1716 19.9905 13.5363C20.8762 13.901 21.6343 14.5192 22.1698 15.3134C22.7052 16.1076 22.994 17.0422 23 18C23.0027 18.6446 22.8773 19.2833 22.6313 19.8791C22.3852 20.4749 22.0233 21.0159 21.5666 21.4708C21.1099 21.9257 20.5674 22.2853 19.9706 22.529C19.3738 22.7726 18.7346 22.8953 18.09 22.89Z" fill="#808080"/>
                </g>
                <defs>
                  <clipPath id="clip0_61_42">
                    <rect width="36" height="36" fill="white"/>
                  </clipPath>
                </defs>
              </svg>
              <span align="center" style="color: #808080; padding-right:16px">1336</span>

            </div>
          </v-card-actions>
        </v-card>
      </v-col>
      <v-col cols="4">
        <v-card style="box-shadow: 0px 5px 25px rgba(0, 0, 0, 0.15); border-radius: 0px;">
          <v-img src="@/assets/gypsy-6.png" class="align-end" gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                 height="200px" cover></v-img>
          <v-card-title class="text-black text-left" style="padding-bottom: 16px;">Cafe run</v-card-title>
          <v-card-subtitle style="padding-bottom:32px" class="text-left">
            Market place for cafe around you
          </v-card-subtitle>
          <v-card-actions class="d-flex" style="margin-bottom:10px">
            <v-btn elevation="4" style="background-color: #FA2964; border-radius:50px; padding-left: 16px; padding-right: 16px; padding-top:10px; padding-bottom:10px">
              <span class="text-white" style="">View App</span>
              <v-icon right style="color: #fff">mdi-chevron-right</v-icon>
            </v-btn>
            <v-spacer></v-spacer>
            <div class="d-flex" >

              <!-- <v-icon style="color: #808080;">mdi-eye</v-icon> -->
              <svg align="center" width="24" height="24"   viewBox="0 0 36 36" fill="none" xmlns="http://www.w3.org/2000/svg">
                <g clip-path="url(#clip0_61_42)">
                  <path d="M33.62 17.53C30.25 11.3 24.34 7.53 17.8 7.53C11.26 7.53 5.34 11.3 2 17.53L1.72 18L1.98 18.48C5.35 24.71 11.26 28.48 17.8 28.48C24.34 28.48 30.26 24.76 33.62 18.48L33.88 18L33.62 17.53ZM17.8 26.43C12.17 26.43 7 23.29 4 18C7 12.71 12.17 9.57 17.8 9.57C23.43 9.57 28.54 12.72 31.59 18C28.54 23.29 23.42 26.43 17.8 26.43Z" fill="#808080"/>
                  <path d="M18.09 11.17C16.7341 11.1799 15.4116 11.5914 14.2894 12.3525C13.1673 13.1136 12.2958 14.1902 11.7852 15.4462C11.2745 16.7023 11.1475 18.0816 11.4203 19.4098C11.693 20.738 12.3533 21.9555 13.3176 22.9087C14.282 23.8619 15.5072 24.5079 16.8385 24.7652C18.1697 25.0225 19.5474 24.8794 20.7975 24.3542C22.0475 23.8289 23.1139 22.945 23.8619 21.8141C24.6098 20.6831 25.0059 19.3559 25 18C24.9961 17.0974 24.8141 16.2045 24.4644 15.3724C24.1148 14.5403 23.6044 13.7854 22.9625 13.1509C22.3206 12.5164 21.5598 12.0148 20.7236 11.6749C19.8875 11.335 18.9925 11.1634 18.09 11.17ZM18.09 22.89C17.1323 22.8801 16.1988 22.5875 15.4068 22.0488C14.6148 21.5101 13.9997 20.7495 13.6386 19.8623C13.2776 18.9752 13.1867 18.0012 13.3774 17.0625C13.5681 16.1239 14.0319 15.2626 14.7106 14.5867C15.3892 13.9108 16.2524 13.4505 17.1918 13.2637C18.1312 13.0768 19.1049 13.1716 19.9905 13.5363C20.8762 13.901 21.6343 14.5192 22.1698 15.3134C22.7052 16.1076 22.994 17.0422 23 18C23.0027 18.6446 22.8773 19.2833 22.6313 19.8791C22.3852 20.4749 22.0233 21.0159 21.5666 21.4708C21.1099 21.9257 20.5674 22.2853 19.9706 22.529C19.3738 22.7726 18.7346 22.8953 18.09 22.89Z" fill="#808080"/>
                </g>
                <defs>
                  <clipPath id="clip0_61_42">
                    <rect width="36" height="36" fill="white"/>
                  </clipPath>
                </defs>
              </svg>
              <span align="center" style="color: #808080; padding-right:16px">1336</span>

            </div>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>

  <v-container class="mb-6 mt-10 wrapper-box">
    <v-row>
      <v-col cols="12">
        <p align="center" class="header-title">Become Our Partner</p>
        <p class="header-title-sub">As a Rider , Merchant , Employer , Agency</p>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="4">
        <v-card class="partners_box">
          <v-img src="@/assets/partner-1.png" class="align-end" gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
            height="200px" cover></v-img>
          <v-card-title class="text-black text-center">As a Rirder/Driver</v-card-title>
          <v-card-text class="text-center">
            Earn money by delivering food from restaurant. All you need are the skills and a bike
          </v-card-text>
          <v-card-actions align="center">
            <v-btn elevation="0" class="mx-auto bg-info" style="background: #00CDCD !important">
              Ride with us
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
      <v-col cols="4">
        <v-card class="partners_box">
          <v-img src="@/assets/partner-2.png" class="align-end" gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
            height="200px" cover></v-img>
          <v-card-title class="text-black text-center">As a Merchant / Brand Owner</v-card-title>
          <v-card-text class="text-center">
            Quickbite helps restaurants grow with online ordering, loyalty, programs, and more
          </v-card-text>
          <v-card-actions align="center">
            <v-btn elevation="0" class="mx-auto bg-info"  style="background: #00CDCD !important">
              Partner with us
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
      <v-col cols="4">
        <v-card class="partners_box">
          <v-img src="@/assets/partner-3.png" class="align-end" gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
            height="200px" cover></v-img>
          <v-card-title class="text-black text-center">As an Employer / Agency</v-card-title>
          <v-card-text class="text-center">
            Be part of a team that’s building
            a top-notch delivery service.
          </v-card-text>
          <v-card-actions align="center">
            <v-btn elevation="0" class="mx-auto bg-info" style="background: #808080 !important;">
             Inquire now
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
  <hr>
  <v-container class="mt-6">
    <v-row>
      <v-col cols="12" sm="12" md="3">
        <h2 class="footer_title">About The Gypsy</h2>
        <p class="footer_paragraph" style="margin-bottom: 16px; margin-top: 34px;">The gypsy is a Super App that is useful for users travelling from point A to point B in search of anything
          and everything!!!</p>
        <ul class="footer_social">
          <li>
            <img src="@/assets/map-pointer.svg" height="24">
            Marine drive, Singapore
          </li>
          <li>
            <img src="@/assets/phone.svg" height="24">
            +917738282000
          </li>
          <li>
            <img src="@/assets/whatsapp.svg" height="24">
            +917738282000
          </li>
          <li>
            <img src="@/assets/mail.svg" height="24">
            <a href="mailto:support@the-gypsy.in">support@the-gypsy.in</a>
          </li>
        </ul>
      </v-col>
      <v-col cols="12" sm="12" md="3">
        <h2 class="footer_title" style="margin-bottom: 16px;">Quick links</h2>
        <ul class="footer_links" style="margin-top: 37px">
          <li>
            <img src="@/assets/links-arrow.svg" height="12">
            Our Apps
          </li>
          <li>
            <img src="@/assets/links-arrow.svg" height="12">
            Sign Up/Register
          </li>
          <li>
            <img src="@/assets/links-arrow.svg" height="12">
            Delivery partners
          </li>
          <li>
            <img src="@/assets/links-arrow.svg" height="12">
            Merchants
          </li>
          <li>
            <img src="@/assets/links-arrow.svg" height="12">
            Employers
          </li>
        </ul>
      </v-col>
      <v-col cols="12" sm="12" md="3">
        <h2 class="footer_title">Our Apps</h2>
        <v-row class="footer_apps" style="margin-top: 37px; padding-right: 20px">
          <v-col cols="4">
            <p style="margin-bottom: 10px;">Mall-e</p>
            <img src="@/assets/gypsi-1.png">
          </v-col>
          <v-col cols="4">
            <p style="margin-bottom: 10px;">Boozards</p>
            <img src="@/assets/gypsy-2.png">
          </v-col>
          <v-col cols="4">
            <p style="margin-bottom: 10px;">Flea</p>
            <img src="@/assets/gypsy-3.png">
          </v-col>
          <v-col cols="4">
            <p style="margin-bottom: 10px;">Mendesliga</p>
            <img src="@/assets/gypsy-4.png">
          </v-col> <v-col cols="4">
          <p style="margin-bottom: 10px;">Cake run</p>
          <img src="@/assets/gypsy-5.png">
        </v-col>
          <v-col cols="4">
            <p style="margin-bottom: 10px;">Cafe run</p>
            <img src="@/assets/gypsy-6.png">
          </v-col>
          <v-col>
            <a href="javascript:void(0)" style="color: #00CDCD;font-size: 14px;font-weight: 600;line-height: 19px; text-decoration: none"> View all</a>
          </v-col>

        </v-row>
      </v-col>
      <v-col cols="12" sm="12" md="3">
        <h2 class="footer_title">Sign up / Register</h2>
        <p class="footer_paragraph" style="margin-bottom: 16px; margin-top: 34px;">
          Sign up and be part of the Gypsy Community.
          Please Register for a Gypsy ID which can be used for all our Apps.<br>
          Type your email and press get started.</p>
        <input class="footer_input" placeholder="Type your email">
        <v-btn style="width: inherit; border-radius: 0!important; margin-top: 16px;background: #00CDCD; color: white">Get started</v-btn>
      </v-col>
    </v-row>
  </v-container>

  <v-footer class="bg-black text-center d-flex flex-column">
    <div class="pt-0" style="display: flex; align-items: center">
      @ The gypsy International | Singapore, India 2023 - 2025
      <v-btn style="margin-left: 100px" variant="text" color="#00CDCD" icon="mdi-facebook"></v-btn>
      <v-btn variant="text" color="#00CDCD" icon="mdi-twitter"></v-btn>
      <v-btn variant="text" color="#00CDCD" icon="mdi-instagram"></v-btn>
      <v-btn variant="text" color="#00CDCD" icon="mdi-youtube"></v-btn>
    </div>
  </v-footer>



</template>

<script setup>
</script>

<script>
//import HelloWorld from "./components/HelloWorld";

export default {
  name: "App",
  data() {
    return {
      drawer: false,
      appTitle: 'Awesome App',
      sidebar: false,
      menuItems: [
        { title: 'Home', path: '/home', icon: 'home' },
        { title: 'Sign Up', path: '/signup', icon: 'face' },
        { title: 'Sign In', path: '/signin', icon: 'lock_open' }
      ],
      items: [
        { title: 'Home', path: '/home', icon: 'home' },
        { title: 'Sign Up', path: '/signup', icon: 'face' },
        { title: 'Sign In', path: '/signin', icon: 'lock_open' }
      ]
    }
  },
};
</script>

<style>
@font-face {
  font-family: 'Nunito';
  font-style: normal;
  font-weight: normal;
  src: url('@/assets/font/nunito/Nunito-VariableFont_wght.ttf') format('opentype');
}
*{
  font-family: Nunito;
  text-transform: none;
}

body {
  font-family: Nunito;
}
.v-text-field,.v-input__control{
  height: 50px !important;
}

.h1-title {
  font-family: 'Poppins' sans-serif;
font-style: normal;
font-weight: 700;
}

:deep(.pencarian){
  border-block-color: red;
}
.input-area {
  width: 300px;
  border-top: 1px solid black;
  border-bottom: 1px solid black;
  border-left: 5px solid red;
  height: 42px;
  display: inline-block;
}

.button-search {
  display: inline-block;
  height: 43px !important;
  width: 42px !important;
  background-color: red;
}

.search-field .v-icon.mdi-magnify {
  background-color: blue;
  color: white;
  padding: 24px;
}




.my-custom-class {
  background-color: red;
}



.sub-menu-btn {
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 6px 10px !important;
  border: 1px solid #D9D9D9 !important;
  border-radius: 50px !important;
  margin: 2px;
  height: inherit !important;
}
.sub-menu-btn .badge {
  margin-left: 16px;
}
.sub-menu-btn.active {
  background: #C2D5E9 !important;
  border-radius: 50px !important;
  color: black !important;
}

.badge {
  border-radius: 50px;
  background: #D9D9D9;
  color: black;
  padding: 5px;

}

.badge.active {
  border-radius: 50px;
  background: #0596D5;
  color: white;
  padding: 5px;
}



.jumbotron-text {
  padding-top: 50px;
  padding-bottom: 50px;
}
.search-field .v-icon.mdi-magnify {
  background-color: blue;
  color: white;

}

.search-icon {
  background-color: blue;
  color: white;
}

.header-title {
  color: black;
  font-family: 'Nunito' !important;
  font-style: normal;
  font-weight: 700;
  font-size: 56px;
  line-height: 76px;
}

.card-container {
  display: flex;
  justify-content: space-between;
  width: 948px;

}

.header-title-sub {
  text-align: center;
  font-family: 'Nunito';
  font-style: normal;
  font-weight: 700;
  font-size: 32px;
  line-height: 44px;
  color: #808080;
}

.custom-search-container{
  border: solid 1px #ccc;
  margin-top: 1rem;
  width: 100%;
}

.custom-search {
  /* border-radius: 50px; */
  /* background: #D9D9D9; */

  display: flex;
  place-items: center;
  color: black;
  height:100%;

  border-left: 4px #fc2865 solid;
}
.custom-search > input {
  display: block;
  width:100%;
  height:2rem;
  padding: 0 1rem;
  outline: none;
}

.custom-search > input::placeholder {
  font-size: 0.75rem;
}

.custom-search-icon {
  background: #fc2865;
  padding:5px 2px 5px 2px;
  color:white;
}
.partners_box {
  border-radius: 0!important;
}
.partners_box .v-card-title, .partners_box .v-card-text {
  margin-bottom: 25px;
}
.partners_box .v-btn {
  margin-bottom: 16px;
  border-radius: 0!important;
}

.footer_title {
  font-family: Nunito;
  font-size: 24px;
  font-weight: 700;
  line-height: 33px;
  letter-spacing: 0em;
  text-align: left;
  position: relative;
  display: inline;
  margin-bottom: 34px;
}
.footer_title::before {
  position: absolute;
  top: 30px;
  content: "";
  width: 60px;
  height: 2px;
  background-color: #00CDCD;
}
.footer_social, .footer_links {
  list-style: none;
}
.footer_social li, .footer_links li {
  display: flex;
  align-items: center;
  margin-bottom: 16px;
}
.footer_social img, .footer_links img {
  margin-right: 10px;
}
.footer_paragraph {
  font-family: Nunito;
  font-size: 14px;
  font-weight: 400;
  line-height: 20px;
  letter-spacing: 0em;
  text-align: left;

}
.footer_social a {
  color: #00CDCD;
  text-decoration: none;
}
.footer_apps .v-row {
  margin: 27px -6px;
}
.footer_apps .v-col {
  padding: 6px;
}
.footer_apps p {
  font-family: Nunito;
  font-size: 14px;
  font-weight: 400;
  line-height: 19px;
  letter-spacing: 0em;
  text-align: left;

}
.footer_apps img {
  width: -webkit-fill-available;
}
.footer_input {
  border: 1px solid #00CDCD;
  box-sizing: border-box;
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  padding: 10px;
  gap: 10px;
  height: 40px;
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 140%;
  width: inherit;
}
.footer_input:focus {
  outline: none;
}
</style>
