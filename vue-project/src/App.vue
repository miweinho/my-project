<script setup>
import { ref, defineProps } from 'vue';



const title = ref('Welcome to our P03 Frontend longrunning container');
const text = ref('');
const props = defineProps({
  msg: String,
});

function send() {
  alert(`Sie haben folgende Daten gesendet: ${text.value}`);
}

function onInput(event) {
  text.value = event.target.value;
}
</script>

<template>
  <v-app>
    <v-main>
      <v-container>
        <v-row cols="1">
          <v-col cols="12">
            <h1 class="text-h3 mb-4">{{ title }}</h1>
            <v-textarea :value="text" @input="onInput" label="Label"></v-textarea>
            <v-btn @click="send">Daten Senden</v-btn>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
