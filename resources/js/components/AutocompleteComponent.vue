<template>
    <div>
        <input type="text" v-model="keyword">
        <ul v-if="Products.length > 0">
            <li v-for="product in Products" :key="product.id" v-text="product.name"></li>
        </ul>
    </div>
</template>

<script>
export default {
    data() {
        return {
            keyword: null,
            Products: []
        };
    },
    watch: {
        keyword(after, before) {
            this.getResults();
        }
    },
    methods: {
        getResults() {
            axios.get('/livesearch', { params: { keyword: this.keyword } })
                .then(res => this.Products = res.data)
                .catch(error => {});
        }
    }
}
</script>
