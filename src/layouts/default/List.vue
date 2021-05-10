<template>
  <v-list
    expand
    nav
    v-bind="$attrs"
    v-on="$listeners"
  >
    <template v-for="(item, i) in items">
      <default-list-group
        v-if="item.items"
        :key="`group-${i}`"
        :item="item"
      />

      <default-list-item
        v-else
        :key="`item-${i}`"
        :item="item"
      />
    </template>
  </v-list>
</template>

<script>
  export default {
    name: 'DefaultList',

    components: {
      DefaultListGroup: () => import('./ListGroup'),
      DefaultListItem: () => import('./ListItem'),
    },

    props: {
      items: {
        type: Array,
        default: () => ([]),
      },
    },
  }
</script>
<style>
.v-list--nav .v-list-item, .v-list--nav .v-list-item:before {
    border-radius: 0px;
}
.v-application .px-2 {
    padding-right: 0px !important;
    padding-left: 0px !important;
}
.v-navigation-drawer__image .v-image .v-image__image {
    background-image: none  !important;
    background-position: center center;
}
</style>
