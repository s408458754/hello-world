<template>
  <div>
    <model-child
      v-model="searchText"
      v-model:first-name="firstName"
      v-model:last-name="lastName"
    ></model-child>
    <div>{{ firstName + lastName }}</div>
    <slot-example>
      <template v-slot:header="headerData">
          {{headerData.isMy}}
        <h1>Here might be a page title</h1>
      </template>
      <template v-slot:container>
        <p>zcxzcxz</p>
      </template>
    </slot-example>
  </div>
</template>
<script>
import ModelChild from "./ModelChild.vue";
import SlotExample from "./SlotExample.vue";
export default {
  data() {
    return {
      searchText: "",
      firstName: "",
      lastName: "",
    };
  },
  watch: {
    searchText(v) {
      console.log(v);
    },
  },
  components: {
    ModelChild,
    SlotExample,
  },
};
</script>