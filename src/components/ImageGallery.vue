<script setup>
    import { defineProps } from 'vue'

    const colorProp = defineProps(['isWithColor'])

    const copyUrl = async (url) => {
        await navigator.clipboard.writeText(url)
    }
</script>

<template>
    <!-- add another v-card to act as a container -->
    <!-- this allows for customization in the form of vuetify classes -->
    <v-card class="mx-5 my-2 pa-3">
        <v-row>
            <!-- last 3 props - media query for mobile -->
            <v-col
                v-for="n in 200"
                cols="4"
                sm="3"
                md="2"
                lg="1"
            >
                <v-hover
                    v-slot="{isHovering, props}"
                >
                    <v-card
                        v-bind="props"
                        :elevation="isHovering ? 6 : 3"
                    >
                        <!-- image card -->
                        <v-img
                            :src="`https://picsum.photos/500/300?images=${n * 5 + 10}${colorProp.isWithColor ? '' : '&grayscale'}`"
                            :lazy-src="`https://picsum.photos/10/6?images=${n * 5 + 10}${colorProp.isWithColor ? '' : '&grayscale'}`"
                            @click="copyUrl(`https://picsum.photos/500/300?images=${n * 5 + 10}${colorProp.isWithColor ? '' : '&grayscale'}`)"
                            class="cursor-pointer"
                            aspect-ratio="1"
                            cover
                        >
                            <!-- loading animation -->
                            <template v-slot:placeholder>
                                <v-row
                                    class="fill-height ma-0"
                                    align="center"
                                    justify="center"
                                >
                                    <v-progress-circular 
                                        indeterminate
                                        color="grey-lighten-5"
                                    ></v-progress-circular >
                                </v-row>
                            </template>
                        </v-img>
                    </v-card>
                </v-hover>
            </v-col>
        </v-row>
    </v-card>
</template>