<!-- <script setup>
import { createApp } from 'vue'

const app = createApp({
    data() {
        return {
            products: ""
        }
    },
    created: function() {
        this.getData()
    },
    methods: {
        getData: function(){
            var requestOptions = {
                method: 'GET',
                redirect: 'follow'
            };

            fetch("https://sistemtoko.com/public/demo/product", requestOptions)
                .then(response => response.json())
                // .then(result => this.products = result.aaData)
                .then(result => console.log(result))
                .catch(error => console.log('error', error));
            
            // console.log(this.products);
        }
    }
})

// console.log(products)
</script> -->
<template>
    <section>
        <header>
            <h2>Produk</h2>
        </header>
        <article>
            <!-- {{ products }} -->
            <div v-for="product in products" :key="product.id">
                <figure>
                    <img :src="product.photo" alt="gambar produk...">
                    <figcaption>{{ product.name }}</figcaption>
                    <span>{{ product.price }}</span>
                </figure>
            </div>
        </article>
    </section>
</template>

<script>
    export default {
        name: "App",
        data() {
            return {
                products: []
            }
        },
        mounted() {
            var requestOptions = {
                method: 'GET',
                redirect: 'follow'
            };

            fetch("https://sistemtoko.com/public/demo/product", requestOptions)
                .then(response => response.json())
                .then(result => this.products = JSON.parse(JSON.stringify(result.aaData)))
                // .then(result => console.log(this.products))
                .catch(error => console.log('error', error));
        }
    }

</script>


<style scoped>
@import '../assets/base.css';

section {
    padding: 2rem 0;
}

header h2 {
    color: var(--color-heading);
    text-align: center;
    font-weight: 500;
    text-transform: uppercase;
    /* margin-bottom: 2rem; */
}

article {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
}

figure {
    margin: 1rem 0;
    width: 17rem;
    /* border: solid 1px var(--color-border); */
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 1rem 0;
}

figure img {
    height: 15rem;
}

figure span {
    font-weight: 500;
}

</style>