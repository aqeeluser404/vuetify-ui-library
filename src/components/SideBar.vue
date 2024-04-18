<template>
    <v-navigation-drawer
        expand-on-hover
        rail
    >
        <v-list>
            <v-list-item
                prepend-avatar="https://randomuser.me/api/portraits/women/85.jpg"
                subtitle="aqeelhanslo@gmailcom"
                title="Aqeel Hanslo"
            />
        </v-list>

        <v-divider />

        <v-list density="compact" nav>

            <v-list-item
                prepend-icon="mdi-image"
                title="Color Gallery"
                value="color"
            />

            <v-list-item
                prepend-icon="mdi-dialpad"
                title="Greyspace Gallery"
                value="color"
            />


        </v-list>

    </v-navigation-drawer>
</template>