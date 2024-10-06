<template>
  <div class="detail">
    <div class="detail-list-collapse">
      <button
        v-for="(btn, i) in list_collapses"
        type="button"
        @click="btn_selected = btn.value"
        :class="
          btn_selected === btn.value
            ? 'btn btn-sm btn-drop btn-active'
            : 'btn btn-sm btn-drop'
        "
      >
        <div class="icon">
          <i :class="`${btn.icon}`"></i>
        </div>
      </button>
    </div>
  </div>
</template>

<script setup>
import { ref, watch, defineEmits, defineProps } from "vue";

const props = defineProps({
  section: {
    type: String, //[{ text: string, completed: boolean }]
    default: "",
  },
});

const list_collapses = [
  {
    _id: 1,
    value: "home",
    icon: "fa-solid fa-house",
  },
  {
    _id: 2,
    value: "stack",
    icon: "fa-solid fa-cubes",
  },
  {
    _id: 3,
    value: "exp",
    icon: "fa-solid fa-briefcase",
  },
  {
    _id: 4,
    value: "education",
    icon: "fa-solid fa-diagram-project",
  },
];
const btn_selected = ref(props.section);

const emit = defineEmits(["change"]);

watch(btn_selected, (value) => {
  console.log(`x is ${value}`);
  emit("change", value);
});
</script>
<style lang="scss">
.detail {
  &-list-collapse {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 20px;
    padding: 20px;
    .btn-drop {
      color: #ff512f;
      padding: 16px 20px;
      display: flex;
      justify-content: center;
      align-items: center;
      border: 1px solid #ff512f;
      transition: all 0.2s linear;
      &:hover {
        color: #fff;
        background-image: linear-gradient(to right, #ff512f, #f09819);
      }
      &:focus {
        box-shadow: none;
      }
    }

    .btn-active {
      color: #fff;
      background-image: linear-gradient(to right, #ff512f, #f09819);
      border: 1px solid #ff512f;
    }
  }
}
</style>
