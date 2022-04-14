<template>
  <div class="hello">
    <ui-button :class="hiButton">Hi!</ui-button>
    <ui-button outlined>Outlined</ui-button>
    <ui-button
      v-ripple
      :class="[
        $theme.getThemeClass('secondary-bg'),
        $theme.getThemeClass('on-secondary'),
      ]"
    >
      Secondary background button
    </ui-button>
    <ui-button unelevated>Unelevated</ui-button>

    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  methods:{
    onClick(){
      this.isActive =!this.isActive
    },
  },
  data() {
    return {
      isActive: false,
      hasError: false,
    };
  },
  name: "HelloWorld",
  props: {
    msg: String,
  },
  computed(){
  
  
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.hello{
  min-height: 110vh;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.active {
  color: pink;
}
button{
  margin: 3px;
}
</style>
