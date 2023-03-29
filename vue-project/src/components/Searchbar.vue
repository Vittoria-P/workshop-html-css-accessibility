<template>
    <article class="Searchbar">
        <!-- Non-accessible
        <div class="center searchbar">
        <input type="search" class="search" placeholder="Recherche..." />
        <i class="fa-solid fa-magnifying-glass"></i>
        </div> -->

        <!--Accessible-->
        <div class="center searchbar">
        <form class="center searchbar" role="search" action="/" method="get">
            <input type="text" class="search" placeholder="Recherche..." />
            <button type="submit" class="btn-search" aria-label="recherche">
            <i
                class="fa-solid fa-magnifying-glass"
                visually-hidden
                alt="icone recherche"
            ></i>
            </button>
        </form>
        </div>
    </article>
</template>