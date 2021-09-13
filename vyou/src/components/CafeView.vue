<template>
    <div>
        <v-row>
            <v-col>
                <v-breadcrumbs :items="breadcrumbs_items"></v-breadcrumbs>
            </v-col>
        </v-row>

        <v-row>
            <v-col md="5">
                <v-card>
                    <v-img
                        height="350"
                        src="https://media.cntraveler.com/photos/59ef8712029986662c420322/master/pass/Wild-And-The-Moon_WM-012.jpg"
                        class="d-flex align-end"
                    >
                        <v-card-title>
                            <h2 class="text-h2 white--text">K-FOOD</h2>
                        </v-card-title>
                    </v-img>
                </v-card>
            </v-col>
            <v-col md="7">
                <v-card class="h-100">
                    <v-card-text>
                        <h4 class="text-h5 md-4">
                            Come here if you wanna to taste cool ramen
                        </h4>
                        <v-divider></v-divider>

                        <p class="mt-4 text-body-1 mr-5">
                            In publishing and graphic design, 
                            Lorem ipsum is a placeholder text 
                            commonly used to demonstrate the visual 
                            form of a document or a typeface without 
                            relying on meaningful content. Lorem ipsum
                            may be used as a placeholder before final 
                            copy is available.
                        </p>
                    </v-card-text>
                </v-card>
            </v-col>
        </v-row>

        <v-row class="cafe__menu">
            <v-col md="6">
                <v-card>
                    <v-img
                    height="450"
                    src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTSljfV0i5g-le7uBY41gQK6puQ-t3XVQFMgw&usqp=CAU"
                    class="flex align-end"
                    >
                        <v-card-title>
                            <h2 class="text-h2 white--text">MENU</h2>
                        </v-card-title>
                    </v-img>
                </v-card>
            </v-col>
            <v-col md="6">
                <v-card>
                    <v-card-text>
                        <v-list-item-group>
                            <v-list-item 
                            v-for="(item,i) in menu_items"
                            :key="i"
                            >
                                <v-list-item-avatar>
                                    <v-img :src="item.img"></v-img>
                                </v-list-item-avatar>
                                
                                <v-list-item-content>
                                    <v-list-item-title>
                                        {{item.title}}
                                    </v-list-item-title>

                                    <v-list-item-subtitle class="text-body-1">
                                        {{item.price}}$
                                    </v-list-item-subtitle>
                                </v-list-item-content>

                                <v-list-item-action>
                                    <v-btn icon>
                                        <v-icon color="grey lighten-1">mdi-plus</v-icon>
                                    </v-btn>
                                </v-list-item-action>
                            </v-list-item>
                        </v-list-item-group>
                    </v-card-text>
                </v-card>
            </v-col>
        </v-row>
        <CafeComment/>
    </div>
</template>
<script>
import CafeComment from '@/components/CafeComment'
export default {
    data(){
        return{
            breadcrumbs_items:[
                {
                    text: 'Home',
                    disabled: false,
                    href:'/'
                },
                {
                    text:'K-FOOD',
                    disabled: true,
                    href: '/cafe/view'
                }
            ],
            menu_items:[
                {
                    id: 0,
                    title: 'Sapporo Miso Ramen',
                    img:'https://images.unsplash.com/photo-1585032226651-759b368d7246?ixid=MnwxMjA3fDB8MHxzZWFyY2h8NHx8bm9vZGxlc3xlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&w=1000&q=80',
                    price: 35.99
                },
                {
                    id: 1,
                    title: 'Lorem',
                    img:'https://wallpaperaccess.com/full/3708151.jpg',
                    price: 35.99
                },
                {
                    id: 2,
                    title: 'Sapporo Miso Ramen',
                    img:'https://images.unsplash.com/photo-1569718212165-3a8278d5f624?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTJ8fG5vb2RsZXN8ZW58MHx8MHx8&ixlib=rb-1.2.1&w=1000&q=80',
                    price: 35.99
                },
                {
                    id: 3,
                    title: 'Sapporo Miso Ramen',
                    img:'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRLOqtm82G80CASgIqkNeLjlDIHKe1PgLRhRw&usqp=CAU',
                    price: 35.99
                },
                {
                    id: 4,
                    title: 'Sapporo Miso Ramen',
                    img:'https://wallpapercave.com/wp/wp2393893.jpg',
                    price: 35.99
                },
            ]
        }
    },
    components:{
        CafeComment
    }
}
</script>
<style scoped>
.h-100{
    height: 100%;
}
</style>