<template>
  <LayoutCashVue>
    <template #headerSlot>
      <HeaderCashVue />
    </template>
    <template #resumeSlot>
      <ResumeCashVue
        :label="labelmsg"
        :label-msg="'Ahorro Total:'"
        :total-amount="50000"
        :amount="amount"
      >
        <template #graphicSlot> graphic </template>

        <template #actionSlot>
          <ActionButtonCashVue/>
        </template>
        
      </ResumeCashVue>
    </template>
    <template #movementsSlot>
      <MovementsCashVue
      :movements="movements"
        />
    </template>
  </LayoutCashVue>
</template>

<script>
import LayoutCashVue from "./LayoutCash.vue";
import HeaderCashVue from "./HeaderCash.vue";
import ResumeCashVue from "./Resume/IndexResume.vue";
import MovementsCashVue from "./Movements/IndexMovements.vue";
import ActionButtonCashVue from "./ActionButtonCash.vue";

export default {
  components: {
    LayoutCashVue,
    HeaderCashVue,
    ResumeCashVue,
    MovementsCashVue,
    ActionButtonCashVue,
  },
  data() {
    return {
      amount: null,
      labelmsg: null,
      movements: [
        {
          id: 1,
          title: "Movimiento",
          description: "Deposito de salario",
          amount: "1000",
        },
        {
          id: 2,
          title: "Movimiento 1",
          description: "Deposito de honorarios",
          amount: "500",
        },
        {
          id: 3,
          title: "Movimiento 3",
          description: "Comida",
          amount: "-100",
        },
        {
          id: 4,
          title: "Movimiento 4",
          description: "Colegiatura",
          amount: "1000",
        },
        {
          id: 5,
          title: "Movimiento 5",
          description: "Reparación equipo",
          amount: "1000",
        },
      ],
    };
  },
};
</script>
