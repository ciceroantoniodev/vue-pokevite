<script setup>
    const pokemon = defineProps(["name", "urlBaseSvg"])
</script>

<template>
    <div class="col-4">
        <div class="card mb-3 p-3 cardListPokmon">
            <p class="text-center">{{ pokemon.name }}</p>
            <img 
                :src="urlBaseSvg" 
                class="card-img-top" 
                alt="..." 
                height="80"
            />
        </div>
    </div>
</template>

<style scoped>
    .cardListPokmon{
        background: rgb(72,63,251);
        background: radial-gradient(circle, rgba(72,63,251,0.5) 0%, rgba(70,254,244,0.50) 100%);
        cursor: pointer;
    }

    .cardListPokmon:hover{ opacity: 0.7; }
</style>