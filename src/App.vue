<template lang="pug">
 v-app#inspire
      navigation-component(:drawer='drawer' app)
      v-app-bar(app, color='indigo', dark)
        v-app-bar-nav-icon(@click.stop='drawer = !drawer')
        v-toolbar-title Application
      v-content
        v-container(fluid)
        v-row()
          v-col.green(cols="8")
            | Main Body
          v-col.yellow(cols="4")
            | Trends

        //- v-container.fill-height(fluid)
        //-   | Hello world
      

</template>

<script>
import NavigationComponent from "@/components/navigation/NavigationComponet.vue"
export default {
  components:{
    NavigationComponent
  },
  props: {
    source: String
  },
  data: () => ({
    drawer: null
  })
};
</script>
