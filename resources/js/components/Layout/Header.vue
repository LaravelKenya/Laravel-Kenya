<script setup lang="ts">
import { ref } from "vue";
import { Dialog, DialogPanel } from "@headlessui/vue";
// @ts-ignore
import { Bars3Icon, XMarkIcon } from "@heroicons/vue/24/outline";
import { Link } from "@inertiajs/vue3";
import { cn } from "@/lib/utils";
import { buttonVariants } from "@/components/ui/button";

const navigation = [
    { name: "Home", href: "#" },
    { name: "About Us", href: "#" },
    { name: "Events", href: "#" },
    { name: "Blogs", href: "#" },
    { name: "Media", href: "#" },
];

const mobileMenuOpen = ref(false);
</script>

<template>
    <header class="bg-white">
        <nav
            class="mx-auto flex max-w-7xl items-center justify-between gap-x-6 p-6 lg:px-8"
            aria-label="Global"
        >
            <div class="flex lg:flex-1">
                <a href="#" class="-m-1.5 p-1.5">
                    <span class="text-2xl font-bold font-inter"
                        >Laravel Kenya</span
                    >
                </a>
            </div>
            <div class="hidden lg:flex lg:gap-x-12">
                <a
                    v-for="item in navigation"
                    :key="item.name"
                    :href="item.href"
                    class="text-sm font-normal leading-6 text-black"
                    >{{ item.name }}</a
                >
            </div>
            <div class="flex flex-1 items-center justify-end gap-x-6">
                <Link
                    href=""
                    :class="[
                        cn(
                            buttonVariants({
                                variant: 'outline',
                                class: 'hidden md:block text-red-500 hover:text-red-500 rounded-full border border-red-300 hover:bg-white',
                            })
                        ),
                    ]"
                    >Login</Link
                >
                <Link
                    href=""
                    :class="[
                        cn(
                            buttonVariants({
                                variant: 'outline',
                                class: 'hidden md:block text-black hover:text-black rounded-full border border-black hover:bg-red-600 bg-red-500',
                            })
                        ),
                    ]"
                    >Sign up</Link
                >
            </div>
            <div class="flex lg:hidden">
                <button
                    type="button"
                    class="-m-2.5 inline-flex items-center justify-center rounded-md p-2.5 text-gray-700"
                    @click="mobileMenuOpen = true"
                >
                    <span class="sr-only">Open main menu</span>
                    <Bars3Icon class="h-6 w-6" aria-hidden="true" />
                </button>
            </div>
        </nav>
        <Dialog
            as="div"
            class="lg:hidden"
            @close="mobileMenuOpen = false"
            :open="mobileMenuOpen"
        >
            <div class="fixed inset-0 z-10" />
            <DialogPanel
                class="fixed inset-y-0 right-0 z-10 w-full overflow-y-auto bg-white px-6 py-6 sm:max-w-sm sm:ring-1 sm:ring-gray-900/10"
            >
                <div class="flex justify-between">
                    <div class="flex items-center gap-x-6">
                        <a href="#" class="-m-1.5 p-1.5">
                            <span class="">Laravel Kenya</span>
                            <!-- <img
                            class="h-8 w-auto"
                            src="https://tailwindui.com/img/logos/mark.svg?color=indigo&shade=600"
                            alt=""
                        /> -->
                        </a>
                        <!-- <a
                        href="#"
                        class="ml-auto rounded-md bg-indigo-600 px-3 py-2 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600"
                        >Sign up</a -->
                        <!-- > -->
                        <button
                            type="button"
                            class="-m-2.5 rounded-md p-2.5 text-gray-700"
                            @click="mobileMenuOpen = false"
                        >
                            <span class="sr-only">Close menu</span>
                            <XMarkIcon class="h-6 w-6" aria-hidden="true" />
                        </button>
                    </div>
                </div>
                <div class="mt-6 flow-root">
                    <div class="-my-6 divide-y divide-gray-500/10">
                        <div class="space-y-2 py-6">
                            <a
                                v-for="item in navigation"
                                :key="item.name"
                                :href="item.href"
                                class="-mx-3 block rounded-lg px-3 py-2 text-base font-normal leading-7 text-black hover:bg-gray-50"
                                >{{ item.name }}</a
                            >
                        </div>
                        <!-- <div class="py-6">
                            <a
                                href="#"
                                class="-mx-3 block rounded-lg px-3 py-2.5 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50"
                                >Log in</a
                            >
                        </div> -->
                    </div>
                </div>
            </DialogPanel>
        </Dialog>
    </header>
</template>

<style scoped></style>
