<template>
  <div class="select-armor">
    <div class="armors">
      <img class="armor" src="@/assets/armor1.jpg" />
      <img class="armor" src="@/assets/armor2.jpg" />
      <img class="armor" src="@/assets/armor3.jpg" />
      <img class="armor" src="@/assets/armor1.jpg" />
      <img class="armor" src="@/assets/armor2.jpg" />
      <img class="armor" src="@/assets/armor3.jpg" />
    </div>
  </div>
</template>

<script>
export default {
  name: "SelectArmor",
};
</script>

<style lang="scss" scoped>
.select-armor {
  background: rgba(black, 0.7);
  border-radius: 10px;
  .armors {
    display: flex;
    justify-content: space-around;
    .armor {
      margin: 1rem;
      cursor: pointer;
      height: 15rem;
      // border: 3px solid orange;
    }
  }
}
</style>
