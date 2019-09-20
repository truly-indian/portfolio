<template>
  <section
    id="recent-projects"
    class="hide-overflow"
  >
    <v-layout>
      <v-flex
        xs12
        md6
        primary
        text-xs-center
        pa-5
        white--text
      >
        <base-bubble-1
          style="transform: rotate(180deg) translateX(25%)"
        />
        <base-heading>
          Recent Projects
        </base-heading>

        <base-text class="mb-5">
         Here are Some of My recent projects!!
        </base-text>

        <v-card color="secondary">
          <v-container
            grid-list-md
            pa-2
          >
            <v-layout wrap>
              <v-flex
                v-for="project in projects"
                :key="project"
                xs12
                md6
               >
               <a href="https://github.com/truly-indian">
                  <v-img
                    :src="require(`@/assets/${project.name}.png`)"
                    max-height="300"
                  />
                </a>
              </v-flex>
            </v-layout>
          </v-container>
        </v-card>
      </v-flex>
      <v-flex
        hidden-sm-and-down
        md6
      >
        <v-img
          :src="require('@/assets/recentprojects.png')"
          height="100%"
        />
      </v-flex>
    </v-layout>
  </section>
</template>

<script>
export default {
  data: () => ({
    projects: [{
      name:'blogging',
      url:'https://mighty-depths-98651.herokuapp.com'
    },
    {
      name:'todo',
      url:'https://powerful-shore-44038.herokuapp.com/'
    },
    {
      name:'weather',
      url:'https://serene-ocean-70255.herokuapp.com/'
    },
    {
      name:'trelos',
      url:'http://ec2-52-68-49-86.ap-northeast-1.compute.amazonaws.com:3000/'
    }
    ]
  })
}
</script>
