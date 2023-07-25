<template>
    <div>
        <!--h3>{{ text }}</h3!-->
        <my-component nama="Shadrina" umur="20"></my-component>
        <LatihanComponent name="Shadrina" umur="19"></LatihanComponent>
        <LatihanDuaComponent></LatihanDuaComponent>
        <h2>WatchersComponent</h2>
        <WatchersComponent nama="Shadrinaaa" umur="90"></WatchersComponent>
        <h2>EventsComponent</h2>
        <EventsComponent></EventsComponent>
        <EventsComponent :nama="nama" :umur="umur" @greeted="onGreeted">
        <template #footer>
            <div>
                <p>Ini adalah Footer Event</p>
            </div>
        </template>
        <template #header>
            <div>
                <p>Ini Adalah Header Event</p>
            </div>
        </template>
    </EventsComponent>
    </div>
</template>

<script setup>
import EventsComponent from './EventsComponent.vue';
import MyComponent from './My Component.vue';
import LatihanComponent from './LatihanComponent.vue';
import LatihanDuaComponent from './LatihanDuaComponent.vue';
import WatchersComponent from './WatchersComponent.vue';
// event
import { ref } from 'vue';
const nama = ref('Jhon');
const umur = ref(25);

const onGreeted = () => {
console.log('Kamu sudah disapa, bro!');
};

// export default {
//     name:'Header',
//     props: ['text'],
// }
</script>

<style>
h3 {
    color: black;
    background-color: violet;
    text-align: center;
}
</style>