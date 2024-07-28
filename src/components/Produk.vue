<template>
    <section>
        <header>
            <h2>Produk</h2>
        </header>
        <article>
            <figure>
                <img src="/src/assets/img/produk.jpg" alt="gambar produk...">
                <figcaption>penjelasan produk</figcaption>
                <span>Rp. 10.000</span>
            </figure>
        </article>
    </section>

</template>

<style scoped>
@import '../assets/base.css';

section {
    padding: 2rem;
}
header h2 {
    color: var(--color-heading);
    text-align: center;
    font-weight: 500;
    text-transform: uppercase;
    margin-bottom: 2rem;
}

figure {
    width: 20rem;
    border: solid 1px var(--color-border);
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