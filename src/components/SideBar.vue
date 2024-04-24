<script setup>
    import { defineEmits } from 'vue'

    const emits = defineEmits(['selectOption'])

    const selectOption = (isColor) => {
        emits('selectOption', isColor)
    }
</script>

<template>
    <v-navigation-drawer
        expand-on-hover
        rail
        permanent
    >
        <v-list>
            <v-list-item
                prepend-avatar="https://media.licdn.com/dms/image/D4D03AQHaSxFDfq7U2Q/profile-displayphoto-shrink_200_200/0/1698306517777?e=1719446400&v=beta&t=9vKs_IMs8yKnG6dotVlgf1JidK1JQh5jzoCW_oYNPxY"
                subtitle="aqeelhanslo@gmailcom"
                title="Aqeel Hanslo"
            />
        </v-list>
        <v-divider/>
        <v-list density="compact" nav>
            <v-list-item
                prepend-icon="mdi-image"
                title="Color Gallery"
                value="color"
                @click="selectOption(true)"
            />
            <v-list-item
                prepend-icon="mdi-dialpad"
                title="Greyspace Gallery"
                value="color"
                @click="selectOption(false)"
            />
        </v-list>
    </v-navigation-drawer>
</template>