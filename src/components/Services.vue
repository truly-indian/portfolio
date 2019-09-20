<template>
  <section
    id="services"
    class="hide-overflow"
  >
    <v-layout accent>
      <v-flex
        hidden-sm-and-down
        md6
      >
        <v-img
          :src="require('@/assets/services.png')"
          height="100%"
        />
      </v-flex>
      <v-flex
        xs12
        md6
        text-xs-center
        pa-5
      >
        <v-layout
          align-center
          justify-center
          fill-height
          wrap
        >
          <v-flex xs12>
            <base-bubble-2
              style="transform: translateX(55%)"
            />
            <base-heading class="info--text">
              Organisation
            </base-heading>

            
          </v-flex>
          <v-flex
            v-for="(service, i) in services"
            :key="i"
            md6
            text-xs-center
            mb-3
          >
          
            <v-img
                    :src="require(`@/assets/${service.icon}.png`)"
                    max-height="300"
                  />
             
            <base-text>
              <div
                class="mb-2"
                v-text="service.name"
              />
              <div v-html="service.blurb" />
            </base-text>
            <base-text>
              <div
                class="mb-2"
                v-text="service.name"
              />
              <div v-html="service.demo" />
            </base-text>
          </v-flex>
        </v-layout>
      </v-flex>
    </v-layout>
  </section>
</template>

<script>
export default {
  data: () => ({
    services: [
      {
        name: 'TechQuanta',
        icon: 'kitkat',
        blurb: 'Front-end Developer',
        demo:'Fixed bugs and made the website more responsive!!'
      },
      {
        name: 'Trelos',
        icon: 'trelos1',
        blurb: 'Lead backend Developer',
        demo:'Designed the full database and code the rest apis from scratch!!'
      }
    ]
  })
}
</script>
