<template>
  <v-layout class="base-input">
    <v-flex>
      <v-text-field outline
                    v-on="$listeners"
                    v-bind="$attrs"
                    v-model="inputValue">
      </v-text-field>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  inheritAttrs: false,
  props: ['value'],
  data: () => ({
    inputValue: ''
  }),
  mounted() {
    this.inputValue = this.value
  }
}
</script>
