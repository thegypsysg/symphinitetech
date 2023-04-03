<template>

  <v-toolbar app class="bg-white" style="margin-top: 15px; margin-bottom: 15px" >
    <v-spacer  />
<span class="hidden-sm-and-up">
      <v-toolbar-side-icon @click="sidebar = !sidebar">
      </v-toolbar-side-icon>
    </span>
    <v-toolbar-title>
      <router-link to="/" tag="span" style="cursor: pointer">
        <v-img height="50" src="@/assets/logo-1.png" />
      </router-link>
    </v-toolbar-title>



    <v-toolbar-items class="hidden-xs-only">
      <!-- <div class="coba">
         <v-text-field class="pencarian" v-model="firstName" :rules="rules" bg-color="white">

          </v-text-field>
          <v-btn type="submit" inline-block class="mt-2"></v-btn>
      </div> -->

         <v-toolbar-title>



    </v-toolbar-title>


  <div class="flex" style="margin-left:30px; margin-right:30px" >

  <div class="custom-search-container" >
              <div class="custom-search">
                <input type="text" placeholder="Nurse, Physia, Consultans, Oncologist, Medical, Executves">
                <div class="custom-search-icon">
                  <v-btn variant="text" icon="mdi-magnify"></v-btn>
                </div>
              </div>
            </div>

  </div>

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
      <v-btn  href='/home' variant="outlined" style="background-color: #0596D5;color:white; margin-left:30px; margin-right:30px;">
        <span>Sign Up/Register</span>
      </v-btn>
      <!-- <v-menu>
        <template v-slot:activator="{ props }">
          <v-img height="50" src="@/assets/logo-1.png" />
          <v-btn icon="mdi-menu" v-bind="props"></v-btn>
        </template>

        <v-list>
          <v-list-item v-for="(item, i) in items" :key="i">
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu> -->

    </v-toolbar-items>
     <v-toolbar-title>
      <router-link to="/" tag="span" style="cursor: pointer">
        <v-img height="50" src="@/assets/menu.png" />
      </router-link>
    </v-toolbar-title>
    <v-spacer/>
  </v-toolbar>

    <!-- <v-container>
    <v-row>
      <v-col cols="12">
        <div class="d-flex justify-space-between" style="">
      <router-link to="/" tag="span" style="cursor: pointer">
        <v-img height="50" width="50px" src="@/assets/logo-1.png" />
      </router-link>


      <v-row align="center" no-gutters>
    <v-col cols="12" sm="12" md="6">
      <v-text-field
        v-model="searchValue"
        label="Search"
        class="search-field"
        dense
        append-icon="mdi-magnify"
        append-icon-class="search-icon"
      />
    </v-col>
  </v-row>

      <router-link to="/" tag="span" style="cursor: pointer">
        <v-img height="50" width="50px" src="@/assets/logo-1.png" />
      </router-link>

      <router-link to="/" tag="span" style="cursor: pointer">
        <v-img height="50" width="150px" src="@/assets/logo-1.png" />
      </router-link>

      <router-link to="/" tag="span" style="cursor: pointer">
        <v-img height="50" width="150px" src="@/assets/logo-1.png" />
      </router-link>

      <router-link to="/" tag="span" style="cursor: pointer">
        <v-img height="50" width="100px" src="@/assets/logo-1.png" />
      </router-link>
        </div>
      </v-col>
    </v-row>
  </v-container> -->


  <v-sheet class="d-flex align-center justify-center flex-wrap text-center mx-auto" elevation="0" min-height="600"
    width="100%">
    <v-img width="100%" src="@/assets/header.png" />
    <div class="jumbotron-text">

      <h1 align="center" class="header-title" style="font-size:56px; font-family: 'Nunito' !important;
font-style: normal;
font-weight: 700;">What are you Looking for.. ?</h1>
      <p class="header-title-sub">The gypsy Trending Web Apps</p>
    </div>
  </v-sheet>




  <v-container align="center">
    <v-row>
      <v-col cols="6" offset="3">
        <div class="d-flex flex-row justify-center mb-6 " >
          <v-btn class="sub-menu-btn active " style="box-shadow: 0px 5px 25px rgba(0, 0, 0, 0);">
            <p style="font-size: 12px" eleva>View all</p>
            <span class="badge active" style="margin-left: 16px;">2.7K</span>
          </v-btn>
          <v-btn class="sub-menu-btn active" style="box-shadow: 0px 5px 25px rgba(0, 0, 0, 0);">
            <p style="font-size: 12px; margin-left:16px;" eleva>Illustration</p>
            <span class="badge active" style="margin-left: 16px; margin-right:24px">2.7K</span>
          </v-btn>
          <v-btn class="sub-menu-btn active flex" style="box-shadow: 0px 5px 25px rgba(0, 0, 0, 0);">
            <p style="font-size: 12px " eleva>Branding</p>
            <span class="badge active" style="margin-left: 16px;">2.7K</span>
          </v-btn>
          <v-btn class="sub-menu-btn active flex" style="box-shadow: 0px 5px 25px rgba(0, 0, 0, 0);">
            <p style="font-size: 12px" eleva>Product Design</p>
            <span class="badge active" style="margin-left: 16px;">2.7K</span>
          </v-btn>
          <v-btn class="sub-menu-btn active flex" style="box-shadow: 0px 5px 25px rgba(0, 0, 0, 0);">
            <p style="font-size: 12px" eleva>Typography</p>
            <span class="badge active" style="margin-left: 16px;">2.7K</span>
          </v-btn>



          <!-- <v-btn class="sub-menu-btn" >
            Illustration
            <span class="badge">2.7K</span>
          </v-btn>
          <v-btn class="sub-menu-btn">
            Branding
            <span class="badge">2.7K</span>
          </v-btn>
          <v-btn class="sub-menu-btn">
            Product Design
            <span class="badge">2.7K</span>
          </v-btn>
          <v-btn class="sub-menu-btn">
            Typography
            <span class="badge">2.7K</span>
          </v-btn> -->
        </div>
      </v-col>
    </v-row>

<div class="card-container">

        <v-card style="box-shadow: 0px 5px 25px rgba(0, 0, 0, 0.15); border-radius: 0px; width:300px;">
          <v-img src="@/assets/gypsi-1.png" class="align-end" gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
            height="200px" width="300px" cover></v-img>
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

        <v-card style="box-shadow: 0px 5px 25px rgba(0, 0, 0, 0.15); border-radius: 0px; width:300px;">
          <v-img src="@/assets/gypsi-1.png" class="align-end" gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
            height="200px" width="300px" cover></v-img>
          <v-card-title class="text-black text-left" style="padding-bottom: 16px;">Mall-e</v-card-title>
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

        <v-card style="box-shadow: 0px 5px 25px rgba(0, 0, 0, 0.15); border-radius: 0px; width:300px;">
          <v-img src="@/assets/gypsi-1.png" class="align-end" gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
            height="200px" width="300px" cover></v-img>
          <v-card-title class="text-black" style="padding-bottom: 16px;">Mall-e</v-card-title>
          <v-card-subtitle style="padding-bottom:32px">
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

</div>
<div class="card-container" style="padding-top:24px">

        <v-card style="box-shadow: 0px 5px 25px rgba(0, 0, 0, 0.15); border-radius: 0px; width:300px;">
          <v-img src="@/assets/gypsi-1.png" class="align-end" gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
            height="200px" width="300px" cover></v-img>
          <v-card-title class="text-black" style="padding-bottom: 16px; ">Mall-e</v-card-title>
          <v-card-subtitle style="padding-bottom:32px">
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

        <v-card style="box-shadow: 0px 5px 25px rgba(0, 0, 0, 0.15); border-radius: 0px; width:300px;">
          <v-img src="@/assets/gypsi-1.png" class="align-end" gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
            height="200px" width="300px" cover></v-img>
          <v-card-title class="text-black" style="padding-bottom: 16px;">Mall-e</v-card-title>
          <v-card-subtitle style="padding-bottom:32px">
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

        <v-card style="box-shadow: 0px 5px 25px rgba(0, 0, 0, 0.15); border-radius: 0px; width:300px;">
          <v-img src="@/assets/gypsi-1.png" class="align-end" gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
            height="200px" width="300px" cover></v-img>
          <v-card-title class="text-black" style="padding-bottom: 16px;">Mall-e</v-card-title>
          <v-card-subtitle style="padding-bottom:32px">
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

</div>
  </v-container>

  <v-container class="mb-6">
    <v-row>
      <v-col cols="12">
        <p align="center" class="header-title">Become Our Partner</p>
        <p class="header-title-sub">As a Rider , Merchant , Employer , Agency</p>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="4">
        <v-card>
          <v-img src="@/assets/partner-1.png" class="align-end" gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
            height="200px" cover></v-img>
          <v-card-title class="text-black text-center">As a Rirder/Driver</v-card-title>
          <v-card-text class="text-center">
            Earn money by delivering food from restaurant. All you need are the skills and a bike
          </v-card-text>
          <v-card-actions align="center">
            <v-btn elevation="0" class="mx-auto" style="background: #FA2964 !important">
              Explore
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
      <v-col cols="4">
        <v-card>
          <v-img src="@/assets/partner-1.png" class="align-end" gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
            height="200px" cover></v-img>
          <v-card-title class="text-black text-center">As a Rirder/Driver</v-card-title>
          <v-card-text class="text-center">
            Earn money by delivering food from restaurant. All you need are the skills and a bike
          </v-card-text>
          <v-card-actions align="center">
            <v-btn elevation="0" class="mx-auto bg-info">
              Explore
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
      <v-col cols="4">
        <v-card>
          <v-img src="@/assets/partner-1.png" class="align-end" gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
            height="200px" cover></v-img>
          <v-card-title class="text-black text-center">As a Rirder/Driver</v-card-title>
          <v-card-text class="text-center">
            Earn money by delivering food from restaurant. All you need are the skills and a bike
          </v-card-text>
          <v-card-actions align="center">
            <v-btn elevation="0" class="mx-auto bg-info" >
              View app
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
  <hr>
  <v-container class="mt-6">
    <v-row>
      <v-col cols="12">
        <div class="d-flex flex-row justify-center mb-6 ">
          <div class="about">
            <h2>About the gypsum</h2>
            <hr width="25%">
            <p>The gypsy is a Super App that is useful for users travelling from point A to point B in search of anything
              and everything!!!</p>
            <p>
              <a>
                <v-icon color="blue">mdi-menu</v-icon> Marine drive, Singapore
              </a>
            </p>
            <p>
              <a>
                <v-icon color="blue">mdi-menu</v-icon> Marine drive, Singapore
              </a>
            </p>
            <p>
              <a>
                <v-icon color="blue">mdi-menu</v-icon> Marine drive, Singapore
              </a>
            </p>
            <p>
              <a>
                <v-icon color="blue">mdi-menu</v-icon> Marine drive, Singapore
              </a>
            </p>

          </div>
          <div class="about">
            <h2>About the gypsum</h2>
            <hr width="25%">
            <p>The gypsy is a Super App that is useful for users travelling from point A to point B in search of anything
              and everything!!!</p>
            <p>
              <a>
                <v-icon color="blue">mdi-menu</v-icon> Marine drive, Singapore
              </a>
            </p>
            <p>
              <a>
                <v-icon color="blue">mdi-menu</v-icon> Marine drive, Singapore
              </a>
            </p>
            <p>
              <a>
                <v-icon color="blue">mdi-menu</v-icon> Marine drive, Singapore
              </a>
            </p>
            <p>
              <a>
                <v-icon color="blue">mdi-menu</v-icon> Marine drive, Singapore
              </a>
            </p>

          </div>
          <div class="about">
            <h2>About the gypsum</h2>
            <hr width="25%">
            <p>The gypsy is a Super App that is useful for users travelling from point A to point B in search of anything
              and everything!!!</p>
            <p>
              <a>
                <v-icon color="blue">mdi-menu</v-icon> Marine drive, Singapore
              </a>
            </p>
            <p>
              <a>
                <v-icon color="blue">mdi-menu</v-icon> Marine drive, Singapore
              </a>
            </p>
            <p>
              <a>
                <v-icon color="blue">mdi-menu</v-icon> Marine drive, Singapore
              </a>
            </p>
            <p>
              <a>
                <v-icon color="blue">mdi-menu</v-icon> Marine drive, Singapore
              </a>
            </p>

          </div>
          <div class="about">
            <h2>About the gypsum</h2>
            <hr width="25%">
            <p>The gypsy is a Super App that is useful for users travelling from point A to point B in search of anything
              and everything!!!</p>
            <p>
              <a>
                <v-icon color="blue">mdi-menu</v-icon> Marine drive, Singapore
              </a>
            </p>
            <p>
              <a>
                <v-icon color="blue">mdi-menu</v-icon> Marine drive, Singapore
              </a>
            </p>
            <p>
              <a>
                <v-icon color="blue">mdi-menu</v-icon> Marine drive, Singapore
              </a>
            </p>
            <p>
              <a>
                <v-icon color="blue">mdi-menu</v-icon> Marine drive, Singapore
              </a>
            </p>

          </div>

        </div>

      </v-col>
    </v-row>
  </v-container>

  <v-footer class="bg-black text-center d-flex flex-column">
    <div class="pt-0">
      @ The gypsy International | Singapore, India 2023 - 2025
      <v-btn variant="text" icon="mdi-home"></v-btn>
      <v-btn variant="text" icon="mdi-home"></v-btn>
      <v-btn variant="text" icon="mdi-home"></v-btn>
      <v-btn variant="text" icon="mdi-home"></v-btn>
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
*{
  @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap');
font-family: 'Poppins' sans-serif;
text-transform: none;
}

body {
  font-family: 'Poppins' sans-serif;
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
gap: 16px;

width: 152px;
height: 44px;

border: 1px solid #D9D9D9;
border-radius: 50px;


}

.sub-menu-btn.active {
  background: #C2D5E9 !important;
  border-radius: 50px !important;
  color: black !important;
  padding: 6px 16px !important;
  margin: 2px;
  width: 139px !important;
height: 44px !important;


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
</style>
