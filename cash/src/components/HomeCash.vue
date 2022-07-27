<template>
  <LayoutCashVue>
    <template #headerSlot>
      <HeaderCashVue />
    </template>
    <template #resumeSlot>
      <ResumeCashVue
        :label="'Ahorro total:'"
        :total-amount="50000"
        :amount="amount"
        
      />
    </template>
    <template #movementsSlot>
      <MovementsCashVue />
    </template>
  </LayoutCashVue>
</template>

<script>
import LayoutCashVue from "./LayoutCash.vue";
import HeaderCashVue from "./HeaderCash.vue";
import ResumeCashVue from "./Resume/IndexResume.vue";
import MovementsCashVue from "./MovementsCash.vue";

export default {
  components: {
    LayoutCashVue,
    HeaderCashVue,
    ResumeCashVue,
    MovementsCashVue,
  },
  data() {
    return {
      amount: null,
      
    };
  },
};
</script>
