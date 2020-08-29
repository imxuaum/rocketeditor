<template>
  <div class="py-5 rounded-sm bg-brand-black2">

    <div class="p-5">
      <h4 class="text-xl font-bold text-white">Saturação</h4>
      <p class="-mt-1 text-sm text-white">O quão viva a imagem será</p>
      <custom-range class="mt-4" />
    </div>

    <div class="p-5">
      <h4 class="text-xl font-bold text-white">Desfoque</h4>
      <p class="-mt-1 text-sm text-white">O quão nítida a imagem será</p>
      <custom-range class="mt-4" />
    </div>

    <div class="p-5">
      <h4 class="text-xl font-bold text-white">Brilho</h4>
      <p class="-mt-1 text-sm text-white">O quão clara a imagem será</p>
      <custom-range class="mt-4" />
    </div>

    <div class="p-5">
      <h4 class="text-xl font-bold text-white">P&B</h4>
      <p class="-mt-1 text-sm text-white">O quão preto/branco a imagem será</p>
      <custom-range class="mt-4" />
    </div>

    <div class="p-5">
      <h4 class="text-xl font-bold text-white">Contraste</h4>
      <p class="-mt-1 text-sm text-white">O quão definido das cores da imagem serão</p>
      <custom-range class="mt-4" />
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

export default {
    components: {
        CustomRange,
    }
}
</script>

<style>

</style>