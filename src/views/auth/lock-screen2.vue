<template>
  <div class="loginwrapper">
    <div class="lg-inner-column">
      <div class="right-column relative">
        <div
          class="inner-content h-full flex flex-col bg-white dark:bg-slate-800"
        >
          <div class="auth-box2 flex flex-col justify-center h-full">
            <div class="mobile-logo text-center mb-6 lg:hidden block">
              <router-link to="/"
                ><img
                  :src="logo"
                  alt=""
                  class="mx-auto"
              /></router-link>
            </div>
            <div class="text-center mb-10">
              <h4 class="font-medium mb-4">Lock Screen</h4>
              <div class="text-slate-500 dark:text-slate-400 text-base">
                Enter your password to unlock the screen!
              </div>
            </div>
            <div class="author-bio text-center mb-8">
              <div class="h-14 w-14 mx-auto rounded-full">
                <img
                  :src="userBg"
                  alt=""
                  class="w-full h-full object-cover block"
                />
              </div>
              <div
                class="text-slate-900 dark:text-white text-base font-medium mt-4"
              >
                Kathryn Murphy
              </div>
            </div>
            <Lockscreen />

            <div
              class="md:max-w-[345px] mx-auto font-normal text-slate-500 dark:text-slate-400 mt-12 uppercase text-sm"
            >
              Not you ? return
              <router-link
                to="/"
                class="text-slate-900 dark:text-white ml-1 font-medium hover:underline"
              >
                Sign In
              </router-link>
            </div>
          </div>
          <div class="auth-footer text-center">
            Copyright 2024, Goldden All Rights Reserved.
          </div>
        </div>
      </div>
      <div
        class="left-column bg-cover bg-no-repeat bg-center"
        :style="{
          backgroundImage:
            'url(' + pageBg + ')',
        }"
      >
        <div class="flex flex-col h-full justify-center">
          <div class="pb-10 pt-80">
            <div
              class="bg-slate-900 bg-opacity-25 black-500-title max-w-[525px] mx-auto pt-10 pb-10 text-center"
            >
              Insurance
              <span class="text-green-goldden font-bold">BROKER</span>
              Solutions
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import Lockscreen from "./common/lockscreen";
// Image Import
import pageBg from "@/assets/images/all-img/guest-bg.svg"
import userBg from "@/assets/images/all-img/user-big.png"
import logoWhite from "@/assets/images/logo/logo-white.png"
import logo from "@/assets/images/logo/logo.png"

export default {
  data () {
    return {
      logoWhite,logo,pageBg,userBg
    }
  },
  components: {
    Lockscreen,
  },
};
</script>
<style lang="scss"></style>
