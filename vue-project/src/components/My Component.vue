<template>
    <div>
        <h1>Hallo Dunia</h1> 
        <p>Ini Komponen Saya </p>  
        <!--props--> 
        <h4>Nama Saya: {{ nama }}</h4   >
        <p>Umur : {{ umur }}</p>
    </div>
</template>

<script>
export default {
   name: "MyComponent",
    props: ['nama', 'umur'],
    data () {
        return {
            message: "Ini pesan dari komponen"
        }
    },
    methods: {
        greet() {
            console.log("Haloo");
        }
    },
 }
</script>

<style>
h1{
    color:blueviolet;
}

p {
    size: 16px;
}
</style>