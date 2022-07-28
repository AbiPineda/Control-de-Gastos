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
        <template #graphicSlot>
          <GraphicCashVue :amounts="amounts" />
        </template>

        <template #actionSlot>
          <ActionButtonCashVue />
        </template>
      </ResumeCashVue>
    </template>
    <template #movementsSlot>
      <MovementsCashVue :movements="movements" />
    </template>
  </LayoutCashVue>
</template>

<script>
import LayoutCashVue from "./LayoutCash.vue";
import HeaderCashVue from "./HeaderCash.vue";
import ResumeCashVue from "./Resume/IndexResume.vue";
import MovementsCashVue from "./Movements/IndexMovements.vue";
import ActionButtonCashVue from "./ActionButtonCash.vue";
import GraphicCashVue from "./GraphicCash.vue";
export default {
  components: {
    LayoutCashVue,
    HeaderCashVue,
    ResumeCashVue,
    MovementsCashVue,
    ActionButtonCashVue,
    GraphicCashVue,
  },
  data() {
    return {
      amount: null,
      labelmsg: null,
      amounts: [100, 200, 500, 200, -400, -600, -300, 0, 300, 500],
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
