<script setup>
    const pokemon = defineProps(["name", "xp", "height", "img","loading"])
</script>

<template>
    <div 
        class="card CardPokemonSelected"
        :class="loading ? '' : 'animate__animated animate__flipInY'"
    >
        <img 
            v-if="pokemon.name"
                :src="pokemon.img" 
                :alt="pokemon.name" 
                class="card-img-top pt-3"
                style="border: none; height: 300px" 
        />
        <img 
            v-else
                src="../assets/Pokemon_Egg_icon-icons.webp" 
                alt="PokVite" 
                class="card-img-top pt-3"
                style="border: none; width: 300px; margin: auto" 
        />
        <div class="card-body">
            <h5 class="card-title text-center">{{ pokemon.name || '???' }}</h5>
            <hr>
            <div class="row">
                <section class="col">
                    <strong>XP: </strong>
                    <span>{{ pokemon.xp }}</span>
                </section>
                <section class="col">
                    <strong>HEIGHT: </strong>
                    <span>{{ pokemon.height }}</span>
                </section>
            </div>
        </div>
    </div>

</template>

<style scoped>
    .CardPokemonSelected{
        height: 75vh;
        background: rgb(72,63,251);
        background: radial-gradient(circle, rgba(93, 235, 117, 0.8) 0%, rgba(236, 147, 30, 0.8) 60%);
    }
</style>