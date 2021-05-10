<template>
  <v-text-field
    v-model="search"
    placeholder="Buscar"
    prepend-inner-icon="mdi-magnify"
    class="expanding-search mt-1 ml-2 v-btn v-btn--flat v-btn--router v-btn--text theme--light v-size--default"
    :class="{ 'closed' : searchClosed && !search }"
    filled
    dense
    clearable
    @focus="searchClosed = false"
    @blur="searchClosed = true"
  />
</template>

<script>
  export default {
    name: 'DefaultSearch',
    data: () => ({
      fab: false,
      hidden: false,
      tabs: null,
      search: null,
      searchClosed: true,
    }),
  }
</script>

<style lang="sass">
  .v-input.expanding-search
    transition: max-width 0.3s
    .v-input__slot
      &:before, &:after
        border-color: transparent !important
        cursor: pointer !important
    &.closed
      max-width: 45px
      .v-input__slot
      background: transparent !important
  .theme--light.v-text-field--filled > .v-input__control > .v-input__slot
    background: transparent !important
</style>
