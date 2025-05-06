<script lang="ts">
    import type { Component } from "svelte";
    type Link = {
        href: string;
        value: string;
    }
    const links: Link[] = [
        {
            href: '/',
            value: 'home'
        },
        {
            href: '/about',
            value: 'about me'
        },
        {
            href: '/projects',
            value: 'my projects'
        },
        {
            href: '/resume',
            value: 'resume'
        }
    ];
</script>
<div class="flex justify-center items-center mt-2">
    {#each links as link}
        <a class="bg-blue-500 font-bold text-white m-1 py-2 px-4 hover:bg-blue-700 rounded-2xl" href='{link.href}'>{link.value}</a>
    {/each}
</div>