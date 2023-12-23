<script lang="ts">
    import { page } from "$app/stores";
    import HamburgerButton from "$lib/navComponents/HamburgerButton.svelte";
    import NavbarMenu from "$lib/navComponents/NavbarMenu.svelte";
    import "../input.css";
    let currentPage = $page.url.pathname;
    $: currentPage = $page.url.pathname; // if this line is absent, it causes an updating bug
    let pageName = "";
    // handle the base path aka "Home"
    $: {
        if (currentPage === "/") {
        pageName = "Documentation";
        } else {
        // format the page name to be a title instead of a pathname
        pageName = currentPage.charAt(1).toUpperCase() + currentPage.slice(2);
        }
    }
  
</script>

<title>BotForge — {pageName}</title>
<main>
    <NavbarMenu />
    <div class="bg-slate-800 rounded-xl m-4 p-4">
        <slot />
    </div>
    <HamburgerButton />
</main>
