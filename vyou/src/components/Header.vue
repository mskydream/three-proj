<template>
    <div>
        <v-app-bar 
        color="red"
        app>
            <v-col class="font-weight-bold white--text d-flex">
                <v-app-bar-nav-icon @click.stop="drawer = !drawer">
                </v-app-bar-nav-icon>
                <v-app-bar-title class="d-flex align-center">
                    iFood
                </v-app-bar-title>
            </v-col>      
        </v-app-bar>
        <v-navigation-drawer
        v-model="drawer"
        absolute
        left
        temporary
        >
            <v-list
                nav
                dense
            >
                <v-list-item-group
                v-model="group"
                active-class="text--accent-4"
                >

                <v-list-item>
                    <router-link to="/">List of cafes</router-link>
                </v-list-item>

                <v-list-item>
                    About
                </v-list-item>

                <v-list-item>
                    Contact
                </v-list-item>
                </v-list-item-group>
            </v-list>
        </v-navigation-drawer>
    </div>
</template>
<script>
export default {
    name: 'Header',
    data(){
        return{
            drawer: false,
            group: null
        }
    },
}
</script>