<template>
  <v-app>
    <v-content>
      <menuBar/>
      <v-container>
        <v-layout row wrap>
          <v-flex xs12 md3 lg4>

          </v-flex>
          <v-flex xs12 md7 lg4>
            <userList v-if="isLogged()"/>
            <signIn v-if="!isLogged()"/>
          </v-flex>
          <v-flex xs12 md2 lg4>
              
          </v-flex>
        </v-layout>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
import menuBar from "@/components/MenuBar.vue";
import signIn from "@/components/signIn.vue";
import userList from "@/components/userList.vue";

export default {
  name: "home",
  components: {
    menuBar,
    signIn,
    userList
  },
  methods: {
    isLogged(){
      return localStorage.getItem("loginStatus")
    }
  },
  return(){
  }
};
</script>
