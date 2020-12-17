<template>
    <div class="">
        <input type="range" min="0" max="100" v-bind:value="startValue" v-on:input="startValue = $event.target.value">
        <input type="range" min="0" max="100" v-bind:value="endValue" v-on:input="endValue = $event.target.value">      
      <p> endValue {{endValue}} </p>         
      <p> startValue {{startValue}} </p>         
    </div>
</template>

<script>
    export default {
        data() {
            return {
                startValue: 0,
                endValue: 100
            }
        },
    }
</script>

<style scoped>

input[type=range] {
  width: 100%;
  margin: 8.55px 0;
  background-color: transparent;
  -webkit-appearance: none;
}
input[type=range]:focus {
  outline: none;
}
input[type=range]::-webkit-slider-runnable-track {
  background: #000000;
  border: 1px solid #000000;
  border-radius: 25px;
  width: 100%;
  height: 2.9px;
  cursor: pointer;
}
input[type=range]::-webkit-slider-thumb {
  margin-top: -9.55px;
  width: 20px;
  height: 20px;
  background: #ffffff;
  border: 0.5px solid #000000;
  border-radius: 20px;
  cursor: pointer;
  -webkit-appearance: none;
}
input[type=range]:focus::-webkit-slider-runnable-track {
  background: #000000;
}
input[type=range]::-moz-range-track {
  background: #000000;
  border: 1px solid #000000;
  border-radius: 25px;
  width: 100%;
  height: 2.9px;
  cursor: pointer;
}
input[type=range]::-moz-range-thumb {
  width: 20px;
  height: 20px;
  background: #ffffff;
  border: 0.5px solid #000000;
  border-radius: 20px;
  cursor: pointer;
}
input[type=range]::-ms-track {
  background: transparent;
  border-color: transparent;
  border-width: 8.55px 0;
  color: transparent;
  width: 100%;
  height: 2.9px;
  cursor: pointer;
}
input[type=range]::-ms-fill-lower {
  background: #000000;
  border: 1px solid #000000;
  border-radius: 50px;
}
input[type=range]::-ms-fill-upper {
  background: #000000;
  border: 1px solid #000000;
  border-radius: 50px;
}
input[type=range]::-ms-thumb {
  width: 20px;
  height: 20px;
  background: #ffffff;
  border: 0.5px solid #000000;
  border-radius: 20px;
  cursor: pointer;
  margin-top: 0px;
  /*Needed to keep the Edge thumb centred*/
}
input[type=range]:focus::-ms-fill-lower {
  background: #000000;
}
input[type=range]:focus::-ms-fill-upper {
  background: #000000;
}
/*TODO: Use one of the selectors from https://stackoverflow.com/a/20541859/7077589 and figure out
how to remove the virtical space around the range input in IE*/
@supports (-ms-ime-align:auto) {
  /* Pre-Chromium Edge only styles, selector taken from hhttps://stackoverflow.com/a/32202953/7077589 */
  input[type=range] {
    margin: 0;
    /*Edge starts the margin from the thumb, not the track as other browsers do*/
  }
}


</style>