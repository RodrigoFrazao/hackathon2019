<template xmlns="http://www.w3.org/1999/html">
  <div align="center" class="hello">
    <h1>{{ msg }}</h1>
    <p>
      This is to get an overview on which components are going to be released for <b>{{pi}}</b>
    </p>
    <div align="left">
      <b>Components</b>
      <div id="testdiv">
      </div>
    </div></div>

</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
@Component
export default class HelloWorld extends Vue {

  @Prop() private msg!: string;

  private pi = 'Product Increment 8';
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin-bottom: 2px;

}
ul {
  list-style-type: disc;
  padding: 1px;
  margin-top: 2px;
}
li {
  display: block;
  margin: 3px;
  width: 129px;
}
a {
  color: #42b983;
}
  .hello{
    margin-top: 50px;
  }
</style>
