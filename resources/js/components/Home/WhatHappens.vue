<script setup lang="ts">
import { Card, CardTitle, CardContent, CardHeader } from "@/components/ui/card";
import { Avatar, AvatarImage } from "@/components/ui/avatar";
import {
    BookOpenIcon,
    MapIcon,
    UsersIcon,
    GlobeAltIcon,
    UserIcon,
    ArrowTrendingUpIcon,
} from "@heroicons/vue/24/solid";

const contents = [
    {
        icon: BookOpenIcon,
        title: "Master Classes",
        description:
            "Volunteer to teach a masterclass yourself or join one on a subject you're passionate about any time you are available",
    },
    {
        icon: MapIcon,
        title: "Group trips",
        description:
            "Imagine traveling together with a group of people that think like you. We work, play, and discover ourselves on these trips",
    },
    {
        icon: UsersIcon,
        title: "City Hangouts and Mixers",
        description:
            "We’ll be visiting different cities and hosting social events. A great opportunity to leave your workspace and get to meet others like you",
    },
    {
        icon: ArrowTrendingUpIcon,
        title: "Opportunities & Resources",
        description:
            "We’ll be visiting different cities and hosting social events. A great opportunity to leave your workspace and get to meet others like you",
    },
    {
        icon: GlobeAltIcon,
        title: "Virtual Networking",
        description:
            "Exclusive access to some of the most ambitious and resourceful people from various digital work fields, so hop in.",
    },
    {
        icon: UserIcon,
        title: "Personal Growth",
        description:
            "Grow your audience, following, and authority by engaging and sharing your content with an exclusive group of forward thinkers.",
    },
];
</script>

<template>
    <div class="pt-48">
        <div class="flex justify-center">
            <h1 class="text-4xl font-grotesque">
                <span class="font-weight-500"> What Happens at </span
                ><span class="text-red-500 font-weight-700">Laravel Kenya</span>
            </h1>
        </div>
        <div class="pt-10">
            <div class="md:grid md:grid-cols-12 md:gap-8">
                <div
                    class="col-span-4 mt-3"
                    v-for="content in contents"
                    :key="content.title"
                >
                    <Card>
                        <CardHeader>
                            <div class="flex justify-center">
                                <div
                                    class="w-12 h-12 rounded-full bg-white border border-black flex items-center justify-center"
                                >
                                    <component
                                        :is="content.icon"
                                        class="h-6 w-6"
                                    />
                                </div>
                            </div>
                            <CardTitle
                                class="flex justify-center font-grotesque pt-3 text-xl"
                                >{{ content.title }}</CardTitle
                            >
                        </CardHeader>
                        <CardContent class="pt-2">
                            <p class="font-inter font-weight-300">
                                {{ content.description }}
                            </p>
                        </CardContent>
                    </Card>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped></style>
