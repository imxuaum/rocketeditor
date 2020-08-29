<template>
  <div class="py-5 rounded-sm bg-brand-black2">

    <div class="p-5">
      <h4 class="text-xl font-bold text-white">Saturação</h4>
      <p class="-mt-1 text-sm text-white">O quão viva a imagem será</p>
      <custom-range class="mt-4" :value="state.fx.saturate" @update="setSaturate" />
    </div>

    <div class="p-5">
      <h4 class="text-xl font-bold text-white">Desfoque</h4>
      <p class="-mt-1 text-sm text-white">O quão nítida a imagem será</p>
      <custom-range class="mt-4" :value="state.fx.blur" @update="setBlur" />
    </div>

    <div class="p-5">
      <h4 class="text-xl font-bold text-white">Brilho</h4>
      <p class="-mt-1 text-sm text-white">O quão clara a imagem será</p>
      <custom-range class="mt-4" :value="state.fx.brightness" @update="setBrightness" />
    </div>

    <div class="p-5">
      <h4 class="text-xl font-bold text-white">P&B</h4>
      <p class="-mt-1 text-sm text-white">O quão preto/branco a imagem será</p>
      <custom-range class="mt-4" :value="state.fx.grayscale" @update="setGrayscale" />
    </div>

    <div class="p-5">
      <h4 class="text-xl font-bold text-white">Contraste</h4>
      <p class="-mt-1 text-sm text-white">O quão definido das cores da imagem serão</p>
      <custom-range class="mt-4" :value="state.fx.contrast" @update="setContrast" />
    </div>

    <div class="p-5">
      <button class="w-full py-4 text-2xl font-medium text-white uppercase rounded-sm bg-brand-main">
        baixar imagem
      </button>
    </div>
  </div>
</template>

<script>
import CustomRange from "./CustomRange";
import {
  setGrayscale,
  setBlur,
  setBrightness,
  setContrast,
  setSaturate,
  useStore
} from '../story'

export default {
    components: {
        CustomRange
    },
    setup() {
      const state = useStore() 

      return {
        state,
        setGrayscale,
        setBrightness,
        setContrast,
        setBlur,
        setSaturate,
      }
    }
}
</script>

<style>

</style>