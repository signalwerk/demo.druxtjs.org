<template>
  <div>
    <!-- Header -->
    <b-row v-if="$scopedSlots.header">
      <b-col>
        <h3 class="text-center"><slot name="header" /></h3>
      </b-col>
    </b-row>

    <!-- Results. -->
    <b-row>
      <slot
        name="results"
        :wrapper="{
          component: 'b-col',
          class: 'mb-3',
          propsData: {
            cols: 12,
            sm: 6,
          },
        }"
      />
    </b-row>
  </div>
</template>
