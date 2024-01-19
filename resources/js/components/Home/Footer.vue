<script setup lang="ts">
const navigation = [
    { name: "Home", href: "#" },
    { name: "About Us", href: "#" },
    { name: "Events", href: "#" },
    { name: "Blogs", href: "#" },
];

const mediaicons = [
    {
        name: "Facebook",
        logo: "/assets/facebook.png",
        url: "https://laravelkenya.org/",
    },
    {
        name: "Youtube",
        logo: "/assets/youtube.png",
        url: "https://laravelkenya.org/",
    },
    {
        name: "Twitter",
        logo: "/assets/twitter.png",
        url: "https://laravelkenya.org/",
    },
    {
        name: "Whatsapp",
        logo: "/assets/whatsapp.png",
        url: "https://laravelkenya.org/",
    },
];
</script>

<template>
    <div class="pt-40">
        <div class="bg-black flex flex-row justify-end py-5 px-3 rounded-xl">
            <div
                class="text-white text-4xl w-1/3 m-auto px-2 font-bold font-grotesque"
            >
                Register Now So You Don't Miss Our Events
            </div>
            <div class="bg-white w-2/3 p-3 justify-items-end rounded-xl">
                <div class="flex flex-row justify-center gap-2">
                    <div class="w-full py-4">
                        <input
                            type="email"
                            id="default-input"
                            placeholder="Enter your email"
                            class="bg-gray-50 border border-black text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
                        />
                    </div>
                    <div
                        class="bg-black text-white m-auto px-4 py-3 rounded-xl font-bold"
                    >
                        <input type="submit" value="Subscribe Now" />
                    </div>
                </div>
            </div>
        </div>
    </div>

    <div class="pt-10 flex flex-col md:flex-row justify-between">
        <div class="">
            <a
                class="font-bold pr-3"
                v-for="item in navigation"
                :key="item.name"
                :href="item.href"
                >{{ item.name }}</a
            >
        </div>
        <div class="flex flex-row gap-6">
            <a
                class=""
                v-for="(media, index) in mediaicons"
                :key="index"
                :href="media.url"
            >
                <img class="h-7" :src="media.logo" alt="" srcset="" />
            </a>
        </div>
    </div>

    <div>
        <hr class="h-px my-2 bg-red-500 border-0" />
    </div>

    <div class="flex flex-col md:flex-row justify-between py-8">
        <div class="text-red-500">&copy; Laravel Kenya All rights reserved</div>
        <div class="text-red-500 text-xl font-bold">Laravel Kenya</div>
        <div class="flex flex-row gap-4 text-red-500">
            <div>
                <a href="https://laravelkenya.org/">Terms of service</a>
            </div>
            <div>
                <a href="https://laravelkenya.org/">Privacy Policy</a>
            </div>
        </div>
    </div>
</template>

<style scoped></style>
