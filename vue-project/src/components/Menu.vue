<template>
        <div class="aria-navbar">
        <button @click="$event => toggleMenu = !toggleMenu"
            id="menu-toggle"
            class="btn-menu-toggle"
            aria-controls="menu"
            aria-expanded="false"
            aria-haspopup="true"
            aria-label="menu-toggle"
        >Menu<i class="fa-solid fa-bars" alt="icone du menu"></i>
        </button>
        <nav v-show="toggleMenu" id="menu" class="aria-nav" aria-label="Voir ou cacher le menu">
            <ul>
                <li>
                    <a
                    href="../index.html"
                    alt="lien vers la page principale"
                    tabindex="0"
                    >Home</a>
                </li>
                <li>
                    <a
                    href="../pages/allmovies.html"
                    alt="lien vers la page avec tous les films"
                    tabindex="-1"
                    >Films</a>
                </li>
                <li>
                    <a
                    href="../pages/allseries.html"
                    alt="lien vers la page avec toutes les series"
                    tabindex="-1"
                    >Series</a>
                </li>
                <li>
                    <a href="#" alt="lien vers la page de contact" tabindex="-1"
                    >Contact</a>
                </li>
            </ul>
        </nav>
    </div>
</template>

<script setup>
    import { ref } from "vue"
    const toggleMenu = ref(false)
</script>