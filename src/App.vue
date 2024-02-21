

<template>
  <div>
    <h1> student shedule of college</h1>
    <h4 v-if="play1"> The students are playing the cricket everyday</h4>
    <h4 v-if="!play1"> they will play tomorrow evening because they have the classes on they shedule </h4>
     <br>
     <hr>
     <h1> holidays in this month</h1>

     <button @click="holiday =!holiday">reverse on it</button>
      <h4 v-if="holiday">tomorrow is not a holiday</h4>
      <h4 v-else> next five days as holiday the government declared</h4>

      <hr>



    <h1>the next day</h1>
    <h4 v-if="whether===1">its is Monday</h4>
    <h4 v-else-if="whether==2"> its tuesday</h4>
    <h4 v-else-if="whether==3">its is wendesday 😢</h4>
    <h4 v-else-if="whether==4">its thursday </h4>
    <h4 v-else-if="whether==5">its friday </h4>
    <h4 v-else-if="whether==6">its saturday</h4>
    <h4 v-else> ist sunday</h4>
    <br>
    <hr>
    <h2>subjects in 2 years </h2>
    <ul>
      <li>
    <div v-for="subject in subjects">{{parentmsg}}--{{ subject.title}}</div>
  </li>
  </ul>
  <br>
  <hr>
  <ul>
    <li v-for="value in myobject">{{value}}</li>
  </ul>

  </div>
  <hr>
  <EventHandle/>
</template>

<script setup>
import { reactive ,ref} from 'vue';
const play1=ref(false);
const holiday= ref(true);
const whether= ref(1);
setInterval(()=>{whether.value++;},5000);

const parentmsg=ref('subjects in classes')

const subjects=reactive([{title:'java'},{title:'python'},{title:'javascript'},{title:'angularjs'}])
 
 const myobject=reactive({
  title:'obugs',
  author:'janny'
 });


 import EventHandle from './components/EventsHandle.vue'
</script>