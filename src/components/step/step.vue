<template>
  <div class="t-step" :class="[
    'is-horizon',
    status ? `t-step--${status}` : ''
  ]">
    <t-step-item
      v-for="(s, idx) in steps"
      :idx="idx"
      :active="active"
      :total="steps.length"
      :title="s.title"
      :desc="s.desc"
      :icon="s.icon"
      :completeIcon="s.completeIcon"
      :key="idx"
      :textCenter="textCenter"
      :flexBasis="flexBasis"
    />
  </div>
</template>

<script>
import TStepItem from './step-item.vue'
export default {
  components: {
    TStepItem
  },

  name: 't-step',

  props: {
    steps: Array,
    active: Number,
    textCenter: Boolean,
    flexBasis: String,
    status: String
  }
}
</script>
