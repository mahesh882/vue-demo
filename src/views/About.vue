<template>
  <div class="about" id="av">
    <!-- <h1>This is {{ datas.test2 | capitalize }} about page</h1> -->
    <div id="app-3">
      <span v-if="data">Now you see me</span>
      <HelloWorld msg="TestMahesh" />
      <!-- <input v-model="datas.test2" /> -->
    </div>
    <div id="app-4">
      <MaheshTest :msg="obj" />
      <VuexDemo msg="test" />
      <!-- <ol v-for="ob in obj">
        <li v-on:click="testData(ob.name)">{{ ob.name }}</li>
      </ol> -->
    </div>
  </div>
</template>

<script>
import HelloWorld from "@/components/HelloWorld.vue";
import MaheshTest from "@/components/MaheshTest.vue";
import VuexDemo from "@/components/VuexDemo.vue";
export default {
  components: {
    MaheshTest,
    HelloWorld,
    VuexDemo,
  },
  data() {
    return {
      data: false,
      obj: [{ name: "MaheshV" }, { name: "Tesr" }],
      datas: { test: "TestErrr", test2: "TestRRRR" },
    };
  },
  methods: {
    testData: function(name) {
      alert(name);
    },
  },
};
</script>

<style></style>
