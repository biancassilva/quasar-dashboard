<template>
  <q-page class="container bg-grey-1">
    <div class="q-pa-sm row q-col-gutter-md">
      <div class="col-xs-12 col-sm-6 col-lg-3 col-md-3" v-for="(item, index) in dataMiniCard" :key="index">
        <mini-card :value="item.value" :description="item.description" :icon="item.icon" ></mini-card>
      </div>
    </div>
    <div class="row q-pa-sm q-col-gutter-md">
      <div class="col-xs-12 col-lg-8 col-md-8">
        <q-card class="fit">
          <apex-line />
        </q-card>
      </div>
      <div class="col-xs-12 col-lg-4 col-md-4">
        <tabs-donut />
      </div>
    </div>
  </q-page>
</template>

<script>
export default {
  name: 'Index',
  components: {
    ApexLine: () => import('components/ApexLine'),
    MiniCard: () => import('components/MiniCards'),
    TabsDonut: () => import('components/TabsDonut')
  },
  data () {
    return {
      dataMiniCard: [
        { value: '2.000', description: 'Food', icon: 'fastfood' },
        { value: '1.500', description: 'Rent', icon: 'house' },
        { value: '20.000', description: 'Employees', icon: 'person' },
        { value: '900', description: 'Education', icon: 'book' }
      ]
    }
  }
}
</script>
