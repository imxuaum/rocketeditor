<template>
  <div class="h-64 rounded-sm bg-brand-black2">

    <label v-if="!state.hasImage" for="file" class="flex flex-col items-center justify-center w-full h-full cursor-pointer">
      <input 
        @change="handleUpload"
        type="file" id="file" class="hidden">
      <span class="text-6xl">😍</span>
      <span class="text-2xl font-bold text-center text-white">
        Clique aqui para fazer o <br>
        upload da imagem.
      </span>
    </label>

    <div v-else class="flex items-center justify-center w-full h-full p-8">
      <img
        ref="refImage"
        class="w-full"
        :src="state.image"
        alt="">
    </div>

  </div>
</template>

<script>
import { reactive, computed } from "vue";

export default {
    setup() {
        const state = reactive({
            image: null,
            hasImage: computed(() => !!state.image),
        })

        const handleUpload = (event) => {
            const [file] = event.target.files   
            const reader = new FileReader(file)

            reader.onloadend = () => {
                state.image = reader.result
            }

            reader.readAsDataURL(file)
        }

        return { state, handleUpload }
    }
}
</script>
