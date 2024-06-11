<template>
  <!-- <h1 v-bind:class="$style['m-class']">
    Using css module with $ syntax (kebab-case)
  </h1> -->
  <h1 :class="myClasses.anotherClass">
    Using css module with $ syntax (camel-case)
  </h1>
</template>

<style module="myClasses">
.m-class {
  background-color: firebrick;
  color: white;
}

.anotherClass {
  background-color: seagreen;
  color: white;
}
</style>
