<template>
  <HelloWorld msg="Hello Vue 3 + TypeScript + Vite" />
</template>

<script lang="ts">
import { ref, Ref } from "vue";
import HelloWorld from "./components/HelloWorld.vue";

var test1: string = "test1";
test1 = "test11";

export default {
  components: { HelloWorld },
  setup() {
    const test2: Ref<string[]> = ref([]);

    const testFunc1 = async () => {};

    const testFunc = async () => {
      await testFunc1();
      test1 = "test111";
    };

    function testFunc2(param1: number, param2: string): Promise<void> {
      return testFunc1();
    }

    return {
      testFunc,
      testFunc2,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
