<script setup lang="ts">
import { Link } from "@inertiajs/vue3";
import { cn } from "@/lib/utils";
import { buttonVariants } from "@/components/ui/button";
</script>

<template>
    <div class="relative isolate px-6">
        <div class="mx-auto max-w-2xl py-20 sm:py-48 lg:py-32">
            <div class="text-center">
                <h1
                    class="text-4xl font-bold tracking-tight text-gray-900 sm:text-6xl font-grotesque"
                >
                    <span class="text-red-500">LARAVEL</span> KENYA<br />
                    it's more fun
                </h1>
                <p class="mt-6 font-inter">
                    Embark on a journey to amplify Laravel's impact in Kenya
                    through our thriving community.Join us to elevate your
                    skills and experiences, as we unite passionate Laravel
                    enthusiasts, foster innovation, and drive the advancement of
                    technology in the heart of Kenya.
                </p>
                <div class="mt-10 flex items-center justify-center gap-x-6">
                    <Link
                        href=""
                        :class="
                            cn(
                                buttonVariants({
                                    variant: 'default',
                                    class: 'bg-red-500 hover:bg-red-600 text-2xl rounded-full py-6',
                                    size: 'lg',
                                })
                            )
                        "
                        >Join Community</Link
                    >
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped></style>
