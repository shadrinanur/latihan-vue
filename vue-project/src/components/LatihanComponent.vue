<template>
<div v-if="umur > 18">
    <p>Selamat datang {{ name }}</p>
</div>
<div v-else>
    <p>Maaf Kamu Belum Cukup Umur</p>
</div>
<button @click="greet">Sapa</button>
</template>
<script>
export default {
    props: ['name', 'umur'],
    methods: {
        greet () {
            alert("Hallo" + this.name);
        }
    },
}
</script>