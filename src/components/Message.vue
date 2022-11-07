<template>
  <div class="message">
    <span v-if="!sender">{{ name }}</span>
    <div class="flex" :class="sender ? 'flex-row-reverse' : ''">
      <Clique class="mt-1" :src="photoUrl" />
      <div class="text w-3/4" :class="sender ? 'bg-blue-800' : 'bg-gray-800'">
        <slot />
      </div>
    </div>
  </div>
</template>

<script>
import Clique from './Clique.vue'
export default {
  components: { Clique},
  props: {
    name: { type: String, default: '' },
    photoUrl: { type: String, default: '' },
    sender: { type: Boolean, default: false }
  }
}
</script>
