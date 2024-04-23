<template>
    <v-row>
        <v-col
            v-for="n in 200"
            cols="1"
        >
            <v-card>
                <!-- image card -->
                <v-img
                    :src="`https://picsum.photos/500/300?images=${n * 5 + 10}`"
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
        </v-col>
    </v-row>
</template>