<template>
    <button class="p-3 rounded-3xl" :class="{'bg-transparent border border-blue-800 text-blue-800 w-32' : theme === 'transparent-btn', 'bg-red-700 text-white w-64' : theme === 'red-btn', 'bg-blue-500 text-white w-64' : theme === 'blue-btn'}"><slot></slot></button>
</template>

<script>
export default {
  name: 'VButton',
  props: {
      theme: String
  },
}
</script>