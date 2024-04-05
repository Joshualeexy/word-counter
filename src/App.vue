<script setup>
import { ref } from 'vue';
const string = ref('');

function count() {
  let stringarray = string.value.split('');
  let noofwords = stringarray.length;
}
</script>

<template>

  <div
    class="w-full h-screen grid place-content-center grid-cols-1 brightness-10 bg-blue-200 sepia"
  >
    <form class="" @submit.preventds="">
      <h4
        class="text-center text-gray-800 mb-5 text-3xl font-bold"
        style="text-shadow: -3px 5px 7px rgba(0, 0, 0, 0.6)"
      >
        WORD COUNTER
      </h4>
      <fieldset
        class="shadow-lg relative border-black w-10/12 p-5 mx-auto rounded-bl-2xl rounded-tr-2xl sm:w-7/12"
      >
        <legend
          class="rounded-bl-2xl rounded-tr-2xl font-bold border border-black p-2"
        >
          <span class="bg-black absolute w-1 block h-16 top-10"></span>
          TEXT GOES HERE
        </legend>
        <textarea
          v-model="string"
          placeholder="TEXT GOES HERE"
          class="placeholder-gray-600 rounded-tr-2xl rounded-bl-2xl border border-black shadow outline-none h-72 w-full p-3 text-black"
          autofocus
        ></textarea>
        <div class="flex justify-end">
          <button
            @click="count"
            class="border border-black text-black px-5 py-3 rounded-bl-2xl rounded-tr-2xl"
          >
            Begin countng
          </button>
        </div>
      </fieldset>
    </form>
  </div>
</template>
