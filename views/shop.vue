<template>
  в доработке
</template>

<script>
import Catalog from '../components/Catalog.vue'
import Basket from '../components/Basket.vue'
// import catalogItem from '../components/Item'
export default {
    components: {
        
        'catalog': Catalog,
        'basket': Basket
    },
    data() {     
        return {
        }
    },
    props: {
    },
    methods: {
        addItem(item) {
            this.$refs.basket.add(item);
        },
        get(url) {
            return fetch(url).then(data => data.json());
        },
        post(url, obj) {
            return fetch(url, {
                method: 'POST',
                headers: { "Content-Type": "application/json" },
                body: JSON.stringify(obj)
            }).then(data => data.json());
        },
        put(url, obj) {
            return fetch(url, {
                method: 'PUT',
                headers: { "Content-Type": "application/json" },
                body: JSON.stringify(obj)
            }).then(data => data.json());
        },
        delete(url) {
            return fetch(url, {
                method: 'DELETE',
                headers: { "Content-Type": "application/json" }
            }).then(data => data.json());
        }
    },
    mounted() {
       
    }
}
</script>

<style>
</style>