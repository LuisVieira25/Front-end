<template>
    <div class="produtos">
        <div class="produto">
            <h2>Produto XYZ</h2>
            <p>25 Euros</p>
        </div>
        <div class="produto">
            <h2>Produto XYZ</h2>
            <p>25 Euros</p>
        </div>
        <div class="produto">
            <h2>Produto XYZ</h2>
            <p>25 Euros</p>
        </div>
    </div>
</template>

<style scoped>
.produtos{
    display: flex;
    flex-direction: column;
    height: 90vh;
    align-items: center;
    justify-content: center;
}
.produto{
    background-color: lightgrey;
    padding: 3rem;
    width: 400px;
    box-shadow: 0 0 24px rgba(0, 0, 0, 3);
}
</style>