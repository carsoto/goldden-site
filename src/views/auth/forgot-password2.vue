<template>
  <div class="loginwrapper">
    <div class="lg-inner-column">
      <div class="right-column relative">
        <div
          class="inner-content h-full flex flex-col bg-white dark:bg-slate-800"
        >
          <div class="auth-box2 flex flex-col justify-center h-full">
            <div class="mobile-logo text-center mb-6 block">
              <router-link to="/"
                ><img
                  :src="logo"
                  alt=""
                  class="mx-auto"
              /></router-link>
            </div>
            <div class="text-center 2xl:mb-10 mb-5">
              <h4 class="font-medium mb-4">¿Ha olvidado su contraseña?</h4>
              <div class="text-slate-500 dark:text-slate-400 text-base">
                Restablecer contraseña con Goldden.
              </div>
            </div>
            <div
              class="font-normal text-base text-slate-500 dark:text-slate-400 text-center px-2 bg-slate-100 dark:bg-slate-600 rounded py-3 mb-4 mt-10"
            >
              Introduzca su dirección de correo electrónico y le enviaremos las instrucciones!
            </div>

            <ForgotPass />
            <div
              class="md:max-w-[345px] mx-auto font-normal text-slate-500 dark:text-slate-400 2xl:mt-12 mt-8 uppercase text-sm"
            >
              Olvídalo,
              <router-link
                to="/"
                class="text-slate-900 dark:text-white font-medium hover:underline"
              >
                DEVUÉLVEME
              </router-link>
              al inicio de sesión
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
import ForgotPass from "./common/forgot";
// Image Import
import pageBg from "@/assets/images/all-img/guest-bg.svg"
import logoWhite from "@/assets/images/logo/logo-white.png"
import logo from "@/assets/images/logo/logo.png"

export default {
  data () {
    return {
      logoWhite,logo,pageBg
    }
  },
  components: {
    ForgotPass,
  },
};
</script>
<style lang="scss"></style>
