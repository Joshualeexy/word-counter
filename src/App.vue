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
      class="w-full h-screen bg-gradient-to-tr from-blue-500 via-indigo-400 to-purple-700 grid place-content-center grid-cols-1 brightness-10"
    >
      <form class="">
        <h4
          class="text-center text-gray-800 mb-5 text-3xl font-bold"
          style="text-shadow: -3px 5px 7px rgba(0, 0, 0, 0.6)"
        >
          WORD COUNTER
        </h4>
        <fieldset
          class="border w-10/12 p-5 mx-auto rounded-bl-2xl rounded-tr-2xl shadow-lg"
        >
          <legend
            class="rounded-bl-2xl rounded-tr-2xl font-bold text-gray-700 border p-2"
          >
            TEXT GOES HERE
          </legend>
          <textarea
            v-model="string"
            placeholder="TEXT GOES HERE"
            class="placeholder-gray-600 rounded-tr-2xl text-balance rounded-bl-2xl bg-transparent border-2 border-indigo-300 shadow outline-none h-72 w-full p-3 text-black"
            autofocus
          ></textarea>
          <div class="flex justify-end">
            <button
              @click="count"
              class="border px-5 py-3 rounded-bl-2xl rounded-tr-2xl"
            >
              Begin countng
            </button>
          </div>
        </fieldset>
      </form>
    </div>
</template>
