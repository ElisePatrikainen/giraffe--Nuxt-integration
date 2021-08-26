<template>
  <div>
    <v-btn color="blue darken-1" dark :small="small"><slot /></v-btn>
  </div>
</template>

<script>
export default {
  props: {
    small: Boolean
  }
}
</script>
