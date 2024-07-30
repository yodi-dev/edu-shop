<template>
    <nav>
        <img src="../assets/logo.png" alt="">
        <h1>Edu-shop</h1>
    </nav>
</template>

<style scoped>
@import url(../assets/base.css);
nav {
    background-color: var(--color-background-soft);
    display: flex;
    height: 15vh;
    border-bottom: solid 1px var(--color-border);
}

nav img {
    margin: auto 1rem auto 2rem;
    height: 4em;
}

nav h1 {
    margin: auto 0;
    color: var(--color-heading);
    font-weight: bold;
}
</style>