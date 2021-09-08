<template>
    <div id="modal" class="rounded-lg m-12 bg-white shadow-md">
        <div class="flex px-10 py-8 h-48 relative">
            <VCloseIcon class="absolute right-6 top-6"/>
            <div :class="{'text-red-700 bg-red-200' : type === 'error', 'text-blue-700 bg-blue-200' : type === 'info', 'text-yellow-500 bg-yellow-200' : type === 'warning', 'text-green-700 bg-green-200' : type === 'success' }" class="w-12 h-12 flex items-center justify-center rounded-full">
               <VWarningIcon />  
            </div>
            <div class="ml-4 w-10/12">
                <h2 class="text-gray-900 text-xl font-medium mb-2">
                    {{ title }}
                </h2>
                <p class="text-gray-700"> {{ msg }} </p>
            </div>
        </div>
        <div class="bg-gray-100 p-6 h-24">
            <div v-if="type === 'error'" class="flex space-x-4 justify-end">
                <VButton theme="transparent-btn">Cancel</VButton>
                <VButton theme="red-btn">Ok</VButton>
            </div>
            <div v-if="type === 'info'" class="flex justify-end">
                <VButton theme="blue-btn">Continue</VButton>
            </div>
        </div>
    </div>
</template>

<script>
import VWarningIcon from './VWarningIcon.vue'
import VCloseIcon from './VCloseIcon.vue'
import VButton from './VButton.vue'
export default {
  name: 'VModal',
  props: {
    title: String,  
    msg: String,
    type: String
  },
  components: {
      VWarningIcon,
      VCloseIcon,
      VButton
  }
}
</script>

<style scoped>
    #modal {
        width: 544px;
        max-width: 100%;
    }
</style>
