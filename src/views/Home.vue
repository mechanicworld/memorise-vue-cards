<template>
  <div>
    <Start  />
    <h1>Hello world</h1>

    <Cards />
  </div>
</template>

<script>
// @ is an alias to /src
import Start from "../components/Start";
import Cards from "../components/Cards";

export default {
  name: "Home",
 
  components: {
    Start,
    Cards,
  },
};
</script>
