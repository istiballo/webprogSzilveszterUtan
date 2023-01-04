<template>
    <div>
      <item-card :item="{
        title: 'Pringles Kürtöskalács',
        kep: 'https://picsum.photos/200/220',
        price: '12.99 RON'
      }"></item-card>
      <item-card :item="{
        title: 'Pringles Mézeskalács',
        kep: 'https://picsum.photos/200/220',
        price: '12.99 RON'
      }"></item-card>
      <item-card :item="{
        title: 'Pringles Töltöttkáposzta',
        kep: 'https://picsum.photos/200/220',
        price: '12.99 RON'
      }"></item-card>
      <item-details :item="{
        title: 'Pringles Kürtöskalács',
        kep: 'https://picsum.photos/500/600',
        price: '12.99 RON',
        available: true
      }"></item-details>
      <cart-check>
      </cart-check>

    </div>
</template>

<script>
import itemCard from "~/components/item-card.vue"

export default {
  name: 'IndexPage',
  layout: 'test',
  components: {
    itemCard,
  },

}
</script>
