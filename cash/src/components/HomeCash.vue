<template>
  <LayoutCashVue>
    <template #headerSlot>
      <HeaderCashVue />
    </template>
  </LayoutCashVue>
</template>

<script>
import LayoutCashVue from "./LayoutCash.vue";
import HeaderCashVue from "./HeaderCash.vue";

export default {
  components: {
    LayoutCashVue,
    HeaderCashVue
  },
};
</script>
