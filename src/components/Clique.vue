<template>
  <img class="clique" :src="src" />
  <!-- <img class="clique" :src="images/jeff.jpeg" /> -->
</template>

<script>
export default {
  props: { src: { type: String, default: '' } }
}
</script>
