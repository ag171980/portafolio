<template>
  <div class="img">
    <img
      :src="img"
      alt=""
    />
  </div>
</template>
<script>
export default {
  name:"Foto",
  props:["img"]
}
</script>