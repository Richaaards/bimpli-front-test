<template>
    <div class="flex flex-wrap justify-around">
        <div class="flex justify-center w-full mt-8">
            <h1 class="text-3xl font-bold">Liste des restaurants</h1>
        </div>
        <div v-for="restaurant in restaurants" v-bind:key="restaurant.id" class="p-10" >
            <div class="rounded-lg shadow-lg bg-white max-w-md">
                <router-link :to="{name: 'RestaurantInfo', params: { restaurant: restaurant, id: restaurant.id }}">
                    <img class="rounded-t-lg" :src="restaurant.img" alt=""/>
                </router-link>
                    <div class="p-6">
                        <h5 class="text-gray-900 text-xl font-medium mb-2">{{ restaurant.name }}</h5>
                        <p class="text-gray-700 text-base mb-4">
                            {{ restaurant.location }} {{ restaurant.category }}
                        </p>
                        <div class="rounded-full bg-blue-300 w-6">{{ restaurant.rating }}</div>
                    </div>
                </div>
            </div>
        </div>
</template>

<script>
export default {
    name: 'RestaurantsList',
    data() {
        return  {
            restaurants: [
                {
                    id: 1,
                    name: 'Burger King',
                    location: 'Paris',
                    img: 'https://mdbootstrap.com/img/new/standard/nature/184.jpg',
                    category: 'Fast Food',
                    rating: 4,
                },
                {
                    id: 2,
                    name: 'McDO',
                    location: 'Paris',
                    img: 'https://mdbootstrap.com/img/new/standard/nature/185.jpg',
                    category: 'Fast Food',
                    rating: 3,
                },
                {
                    id: 3,
                    name: 'Chippotle',
                    location: 'Paris',
                    img: 'https://mdbootstrap.com/img/new/standard/nature/186.jpg',
                    category: 'Fast Food',
                    rating: 5,
                },
                {
                    id: 4,
                    name: 'Quick',
                    location: 'Paris',
                    img: 'https://mdbootstrap.com/img/new/standard/nature/187.jpg',
                    category: 'Fast Food',
                    rating: 3,
                },
                {
                    id: 5,
                    name: 'Subway',
                    location: 'Paris',
                    img: 'https://mdbootstrap.com/img/new/standard/nature/188.jpg',
                    category: 'Fast Food',
                    rating: 3,
                },
                {
                    id: 6,
                    name: 'Five Guys',
                    location: 'Paris',
                    img: 'https://mdbootstrap.com/img/new/standard/nature/189.jpg',
                    category: 'Fast Food',
                    rating: 2,
                },
                {
                    id: 7,
                    name: 'Otacos',
                    location: 'Paris',
                    img: 'https://mdbootstrap.com/img/new/standard/nature/190.jpg',
                    category: 'Fast Food',
                    rating: 1,
                },
                {
                    id: 8,
                    name: 'Camion qui fume',
                    location: 'Paris',
                    img: 'https://mdbootstrap.com/img/new/standard/nature/191.jpg',
                    category: 'Fast Food',
                    rating: 5,
                },
            ],
        }
    },
}
</script>
