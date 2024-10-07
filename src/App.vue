<script setup>
import { ref } from "vue";

import HelloWorld from "./components/HelloWorld.vue";
import Navbar from "./components/Navbar.vue";
import Profile from "./components/Profile.vue";
import CollapseButtonList from "./components/CollapseButtonList.vue";
import Detail from "./components/Detail.vue";
const section_select = ref("home");
</script>

<template>
  <div class="header">
    <Navbar></Navbar>

  </div>
  <div class="container cover">
    <div class="body-container row ">
      <div class="col-lg-4 ">
        <Profile></Profile>
      </div>
      <div class="col-lg-8">
        <div class="d-flex justify-content-center justify-content-lg-end">
          <CollapseButtonList
            :section="section_select"
            @change="
              (val) => {
                section_select = val;
              }
            "
          ></CollapseButtonList>
        </div>
        <div>
          <Detail :section="section_select"></Detail>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.cover {
  padding: 100px 10px;
  overflow: hidden;
}
</style>
