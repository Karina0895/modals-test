<template>
    <div id="modal" class="rounded-lg m-12 bg-white shadow-md">
        <div class="flex px-10 py-8 h-48">
            <div class="w-12 h-12 flex items-center justify-center rounded-full bg-red-200">
               <VWarningIcon />  
            </div>
            <div class="ml-4 w-10/12">
                <h2 class="text-gray-900 text-xl font-medium mb-2">
                    {{ title }}
                </h2>
                <p class="text-gray-700"> {{ msg }} </p>
            </div>
        </div>
        <div class="bg-gray-100 p-6 h-24"></div>
    </div>
</template>

<script>
import VWarningIcon from './VWarningIcon.vue'
export default {
  name: 'VModal',
  props: {
    title: String,  
    msg: String
  },
  components: {
      VWarningIcon
  }
}
</script>

<style scoped>
    #modal {
        width: 544px;
        max-width: 100%;
    }
</style>
