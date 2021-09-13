<template>
    <v-row>
        <v-col class="cafe__component">
            <h1 class="py-4">List of cafes</h1>
            <v-row class="cafe__list mx-2">
                <v-col
                    v-for="(cafe,i) in cafes" :key="i.id"
                    md="4" xl="4"
                >
                    <v-card class="cafe__card">
                        <v-img
                            height="250"
                            :src="cafe.img"
                        ></v-img>
                        <v-card-title>
                            <router-link to="/cafe/view">{{ cafe.name }}</router-link>
                        </v-card-title>
                        <v-card-text>
                            <p>{{cafe.description}}</p>
                            <b>Raiting: {{cafe.rating}} of 5</b>
                        </v-card-text>
                    </v-card>
                </v-col>
            </v-row>
        </v-col>
    </v-row>
</template>
<script>
export default {
    name:'Cafe',
    data(){
        return{
            cafes:[
                {
                    id: 0, 
                    name:'K-FOOD', 
                    description: 'Here we can cook nice korean food', 
                    img: 'https://www.expatolife.com/wp-content/uploads/2020/07/bibimbap-Korean-food.jpg',
                    tags:['Asian'],
                    rating: 5
                },
                {
                    id: 1, 
                    name:'WTC', 
                    description: 'All italian food here', 
                    img: 'https://642659-2093756-raikfcquaxqncofqfm.stackpathdns.com/wp-content/uploads/2018/02/Italian-Pizza.jpg',
                    tags:['italian'],
                    rating: 4.9
                },
                {
                    id: 2, 
                    name:'Chinese Food', 
                    description: 'Chinese Food', 
                    img: 'https://www.chinatours.com/wp-content/uploads/2015/03/popular-chinese-dish.jpg',
                    tags:['Asian'],
                    rating: 5
                },
                {
                    id: 3, 
                    name:'Qazaq food', 
                    description: 'Beshbarmak the best food for anyone', 
                    img: 'https://visitmangystau.kz/storage/archive/-2s9EQcmD1C0W.jpg',
                    tags:['qazaq'],
                    rating: 5
                },
                {
                    id: 4, 
                    name:'Palau', 
                    description: 'Mmmmm nice food', 
                    img: 'https://www.people-travels.com/images/Uzbek%20food/Uzbekistan-traditional-food.jpg',
                    tags:['ozbek'],
                    rating: 4.8
                },
                {
                    id: 5, 
                    name:'Sushi', 
                    description: 'curry with rice', 
                    img: 'https://rimage.gnst.jp/livejapan.com/public/article/detail/a/00/00/a0000370/img/basic/a0000370_main.jpg',
                    tags:['japan food'],
                    rating: 4.8
                },
            ]
        }
    }
}
</script>