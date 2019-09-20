<template>
  <section
    id="welcome"
    class="hide-overflow"
  >
    <v-layout>
      <v-flex
        hidden-sm-and-down
        md6
      >
        <v-img
          :src="require('@/assets/img1.jpg')"
          height="100vh"
        />
      </v-flex>

      <v-flex
        xs12
        md6
        align-content-space-between
        layout
        :pa-5="$vuetify.breakpoint.smAndDown"
        wrap
      >
        <base-bubble-1
          style="transform: rotate(180deg) translateY(25%)"
        />

        <v-layout
          align-center
          justify-center
        >
          <v-flex
            xs10
            md6
          >
            <base-heading>Welcome!</base-heading>
            <hr>
             <base-heading>Deepak Malik!</base-heading>
            <base-text>
              University School Of Information And Communication Technology

I am a computer science undergraduate.
A fun loving personality who would love to play outdoors during his spare time. My interests include programming, web developement, and machine learning ;)
            </base-text>
            <a href="https://www.linkedin.com/in/deepak-malik-82a75a175/" style="text-decoration:none"> 
              <base-btn class="mt-4">
                 Learn More!!
              </base-btn>
            </a>
           
          </v-flex>
        </v-layout>
        <base-bubble-2
          style="transform: rotate(180deg) translate(-200px, -15%)"
        />
      </v-flex>
    </v-layout>
  </section>
</template>
