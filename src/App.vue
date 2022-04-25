<template>
  <q-layout view="hHh LpR lFf">
    <div class="bg-grey-8 q-mb-md text-center">
      <h4 class="q-my-none text-white">Text Generator</h4>
      <p class="text-body1 q-my-none text-white">Image to Text Generator</p>
    </div>
    <div class="row justify-center">
      <div class="col-12 text-center q-my-sm">
        <Button
          style="width: 200px"
          color="green"
          label="Take a photo"
          @click="fileRef.click()"
        />
      </div>
      <div class="col-12 text-center q-my-sm">
        <Button
          style="width: 200px"
          color="green"
          label="Upload Image"
          @click="fileUploadRef.click()"
        />
      </div>
      <div class="col-12 hidden">
        <input ref="fileRef" accept="image/*" capture="camera" type="file" />
      </div>
      <div class="col-12 hidden">
        <input ref="fileUploadRef" accept="image/*" type="file" />
      </div>
    </div>
  </q-layout>
</template>

<script lang="ts" setup>
import { ref } from "vue";

const fileRef = ref();
const fileUploadRef = ref();

// const onClick = () => {
//   const msg = new SpeechSynthesisUtterance();
//   msg.text = "Hello World";
//   window.speechSynthesis.speak(msg);
// };
</script>

<style lang="scss">
@font-face {
  font-family: "Poppins-rg";
  src: url("./assets/fonts/Poppins-Regular.ttf");
}

body {
  h1,
  h2,
  h3,
  h4,
  h5,
  h6,
  p,
  span {
    font-family: "Poppins-rg";
  }
  font-family: "Poppins-rg" !important;
}
.screen-center {
  max-width: 1200px;
  margin: auto;
}
.brdr {
  border: 1px solid #e6e7e9 !important;
  &-br {
    border: 1px solid #e6e7e9 !important;
    border-radius: 8px !important;
  }
  &-dashed {
    border: 1px dashed #9e9e9e !important;
    border-radius: 1% !important;
  }
}
</style>
