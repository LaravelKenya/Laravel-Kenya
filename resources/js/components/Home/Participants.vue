<script setup lang="ts">
import { Card, CardContent, CardFooter } from "@/components/ui/card";
import { Button } from "@/components/ui/button";

const images = [
    {
        src: "https://th.bing.com/th/id/OIP.oQ5Em62UVTCdCthozZXIdQHaFj?w=271&h=203&c=7&r=0&o=5&pid=1.7",
        name: "Kemboi Elvis",
        role: "Laravel Developer",
    },
    {
        src: "https://th.bing.com/th/id/OIP.xOaSRMkA3x7bc3MWUZrghQHaE8?w=304&h=203&c=7&r=0&o=5&pid=1.7",
        name: "Collins Rono",
        role: "Laravel& Flutter Developer",
    },
    {
        src: "https://th.bing.com/th/id/OIP.V90cO3woNBCQKrUPXXTotwHaE8?w=274&h=183&c=7&r=0&o=5&pid=1.7",
        name: "John Ngondi",
        role: "Laravel Developer",
    },
];
</script>

<template>
    <div class="pt-48">
        <div class="flex justify-center">
            <h1 class="text-4xl font-bold font-grotesque">
                We are <span class="text-red-500">Laravel Kenya</span>
            </h1>
        </div>
        <div
            class="mx-auto max-w-2xl pt-10 sm:pt-16 lg:pt-10 font-inter font-normal"
        >
            A diverse group of remote and digital workers including software
            engineers, freelancers, designers, creatives & influencers, writers,
            product, growth & sales specialists, operators, investors, and
            founders united with a common mission of building the home for
            digital talents.
        </div>
        <div class="md:grid md:grid-cols-12 md:gap-4 pt-4">
            <div
                class="col-span-3"
                v-for="(image, index) in images"
                :key="index"
            >
                <div
                    class="relative flex flex-col shadow-md rounded-xl overflow-hidden hover:shadow-lg hover:-translate-y-1 transition-all duration-300 max-w-sm"
                >
                    <a href="" class="z-20 absolute h-full w-full top-0 left-0"
                        >&nbsp;</a
                    >
                    <div class="h-auto overflow-hidden">
                        <div class="h-44 overflow-hidden relative">
                            <img :src="image.src" class="w-full" alt="" />
                        </div>
                    </div>
                    <div class="bg-white py-4 px-3">
                        <div class="flex justify-center">
                            <h3 class="mb-2 font-bold">{{ image.name }}</h3>
                        </div>
                        <div class="flex justify-center items-center">
                            <p class="font-bold">
                                {{ image.role }}
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="pt-10 flex justify-center">
            <Button :variant="'destructive'" size="lg" class="rounded-full"
                >Join Us Today</Button
            >
        </div>
    </div>
</template>

<style scoped></style>
