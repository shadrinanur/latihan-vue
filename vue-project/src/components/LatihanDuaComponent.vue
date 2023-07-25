<template>
    <div>
        <input type="text" v-model="cari" placeholder="Cari Data">
        <ul v-if="cariData.length > 0">
            <li v-for="item in cariData" key="item.id">
                {{ item.title }} - {{ item.price }}
            </li>
        </ul>
        <p v-else> Pencarian Tidak Ditemukan.</p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            cari: '',
            products: []
        };
    },
    created() {
        this.products = [
            {id: 1, title: "Baju Anak", price: 25000},
            {id: 2, title: "Susu Anak", price: 75000},
            {id: 3, title: "Topi", price: 10000},
            {id: 4, title: "Balon", price: 1000},
            {id: 5, title: "Kinder Joy", price: 15000}
        ]
    },
    computed: {
        cariData() {
            return this.products.filter((item) => {
                return item.title.match(this.cari);
            });
        }
    }
}
</script>