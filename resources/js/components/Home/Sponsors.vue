<script setup lang="ts">
const sponsors = [
    {
        name: "NWRealite",
        logo: "/assets/sponsors-nwrealite.png",
        url: "https://nwrealite.co.ke",
    },
    {
        name: "Laravel Kenya",
        logo: "/assets/lke.jpeg",
        url: "https://laravelkenya.org",
    },
];
</script>

<template>
    <section class="">
        <div class="py-8 lg:py-16 mx-auto max-w-screen-xl px-4">
            <h2
                class="mb-8 lg:mb-16 text-3xl font-extrabold tracking-tight leading-tight text-center text-gray-900 dark:text-white md:text-4xl"
            >
                Our <span class="text-red-500">Sponsors</span>
            </h2>
            <div
                class="flex flex-col gap-8 md:flex-row justify-center text-gray-500 sm:gap-12 md:grid-cols-6 lg:grid-cols-6 dark:text-gray-400"
            >
                <a
                    v-for="(sponsor, index) in sponsors"
                    :key="index"
                    :href="sponsor.url"
                    class="flex justify-center items-center"
                    target="_blank"
                >
                    <img
                        class="h-9 hover:text-gray-900 dark:hover:text-white"
                        :src="sponsor.logo"
                        alt="NWRealite"
                    />
                </a>
            </div>
        </div>
    </section>
</template>

<style scoped></style>
