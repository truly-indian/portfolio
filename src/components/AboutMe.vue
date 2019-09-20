<template>
  <section
    id="about"
    class="hide-overflow"
  >
    <v-layout white>
      <v-flex
        xs12
        md6
        pa-5
      >
        <base-bubble-1
          style="transform: translate(5%, -5%)"
        />
        <base-heading class="info--text">
          About Me
        </base-heading>

        <base-text class="mb-5">
          I am a computer science undergraduate.<br>Who loves to code complex backend and develop amazing website.
        </base-text>

        <base-subheading class="info--text">
          Skills
        </base-subheading>
       

        <v-alert
          outlined
          color="info"
        >
          <v-layout
            v-for="(skill, i) in skills"
            :key="i"
            style="color: #69A1BB;"
            wrap
          >
            <v-flex
              xs6
              text-uppercase
              v-text="skill.name"
            />
            <v-flex
              xs6
              text-xs-right
              v-text="`${skill.value}%`"
            />
            <v-progress-linear
              :value="skill.value"
              color="info"
              height="8"
            />
          </v-layout>
        </v-alert>
      </v-flex>
      <v-flex
        hidden-sm-and-down
        md6
      >
        <v-img
          :src="require('@/assets/aboutme.png')"
          height="100%"
        />
      </v-flex>
    </v-layout>
  </section>
</template>

<script>
export default {
  data: () => ({
    skills: [
      {
        name: 'HTML / CSS',
        value: 95
      },
      {
        name: 'Nodejs / MongoDb',
        value: 90
      },
      {
        name: 'C++',
        value: 85
      },
      {
        name: 'javascript',
        value: 85
      },
       {
        name: 'Vuejs / vuex',
        value: 80
      },
       {
        name: 'MySQL',
        value: 75
      },
       {
        name: 'Bootstrap',
        value: 95
      }


    ]
  })
}
</script>
