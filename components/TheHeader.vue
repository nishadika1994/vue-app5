
<template>
    <header>

        <div class="brand-name">
            <nuxt-link to="/">Airudi</nuxt-link>
        </div>

        <div class="drawer-toggle" role="button" @click="$store.dispatch('nav/toggleSidebar')">
            <div class="bar"></div>
            <div class="bar"></div>
            <div class="bar"></div>
        </div>

        <div class="app-links">
            <app-links></app-links>
        </div>

    </header>
</template>

<script>

    import AppLinks from '~/components/AppLinks'

export default {

    components: { AppLinks }

}
</script>

<style scoped>

    header{
        display: grid;
        grid-template: 60px / auto 1fr;
        align-items: center;
        background-color: #333;
    }

    .app-links{
        justify-self: end;
    }

    .brand-name {
        margin: 0 10px;
        font-size: 1.3rem;
    }

    .brand-name a {
        text-decoration: none;
        color: white;
    }

    .drawer-toggle .bar {
        width: 90%;
        height: 2px;
        background-color: white;
    }

    .drawer-toggle {
        display: flex;
        justify-self: end;
        flex-direction: column;
        justify-content: space-around;
        height: 50%;
        width: 35px;
        padding-right: 16px;
        cursor: pointer;
    }

    @media (max-width: 767px) {
        header{
            padding: 0 16px;
        }
        header:nth-child{
            justify-self: end !important;
        }
        .app-links {
            display: none;
        }
    }

    @media (min-width: 768px) {
        header{
            padding: 0 64px;
        }
        .app-links {
            display: block;
        }
        .drawer-toggle {
            display: none;
        }
    
vertical-menu {
  width: 200px; /* Set a width if you like */
}

.vertical-menu a {
  background-color: #eee; /* Grey background color */
  color: black; /* Black text color */
  display: block; /* Make the links appear below each other */
  padding: 12px; /* Add some padding */
  text-decoration: none; /* Remove underline from links */
}

.vertical-menu a:hover {
  background-color: #ccc; /* Dark grey background on mouse-over */
}

.vertical-menu a.active {
  background-color: #04AA6D; /* Add a green color to the "active/current" link */
  color: white;
}
    }

</style>
