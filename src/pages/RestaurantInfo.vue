<template>
    <div class="flex flex-wrap p-8">        
        <section
            class="overflow-hidden bg-no-repeat bg-cover w-full"
            :style="{
                'background-image': `url(${this.$route.params.restaurant.cover_picture})`,
                'background-position': '50%',
                'height': '500px',
            }"
        >
        </section>

        <section class="my-8 w-full text-left">
            <h2 class="text-3xl font-bold mb-6">{{ this.$route.params.restaurant.name }}</h2>
            <h3 class="text-2xl uppercase font-normal">{{ this.$route.params.restaurant.street_address }}</h3>
            <h3 class="text-2xl uppercase font-normal">{{ this.$route.params.restaurant.zip_code }} {{ this.$route.params.restaurant.city }}</h3>
        </section>

        <div class="flex flex-col">
            <h2 class="text-2xl font-bold">Menu</h2>
        </div>
        <section 
            class="flex flex-col w-full rounded-lg shadow-lg mb-8 py-2"
        >   
            <div class=w-full> 
                <h5 class="text-left text-2xl font-bold m-4">Entrées</h5>
            </div>
            <div 
                v-for="(item) in this.$route.params.restaurant.dishes.data"
                :key="item.id"
            >
                <div v-if="item.type === 'starter'">
                    <div class="flex justify-between px-4 py-1">
                        <div class="flex-row">
                            <p class="text-left text-base">
                                {{ item.name }}
                            </p>
                        </div>
                        <div class="flex-row	">
                            <p class="text-right text-base">
                                {{ Math.round(item.price /100) }},00 €
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section 
            class="flex flex-col w-full rounded-lg shadow-lg mb-8 py-2"
        >   
            <div class=w-full> 
                <h5 class="text-left text-2xl font-bold m-4">Plats</h5>
            </div>
            <div 
                v-for="(item) in this.$route.params.restaurant.dishes.data"
                :key="item.id"
            >
                <div v-if="item.type === 'main'">
                    <div class="flex justify-between px-4 py-1">
                        <div class="flex-row">
                            <p class="text-left text-base">
                                {{ item.name }}
                            </p>
                        </div>
                        <div class="flex-row	">
                            <p class="text-right text-base">
                                {{ Math.round(item.price /100) }},00 €
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section 
            class="flex flex-col w-full rounded-lg shadow-lg mb-8 py-2"
        >   
            <div class=w-full> 
                <h5 class="text-left text-2xl font-bold m-4">Désserts</h5>
            </div>
            <div 
                v-for="(item) in this.$route.params.restaurant.dishes.data"
                :key="item.id"
            >
                <div v-if="item.type === 'dessert'">
                    <div class="flex justify-between px-4 py-1">
                        <div class="flex-row">
                            <p class="text-left text-base">
                                {{ item.name }}
                            </p>
                        </div>
                        <div class="flex-row	">
                            <p class="text-right text-base">
                                {{ Math.round(item.price / 100) }},00 €
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section 
            class="flex flex-col w-full rounded-lg shadow-lg mb-8 py-2"
        >   
            <div class=w-full> 
                <h5 class="text-left text-2xl font-bold m-4">Boissons</h5>
            </div>
            <div 
                v-for="(item) in this.$route.params.restaurant.dishes.data"
                :key="item.id"
            >
                <div v-if="item.type === 'drink'">
                    <div class="flex justify-between px-4 py-1">
                        <div class="flex-row">
                            <p class="text-left text-base">
                                {{ item.name }}
                            </p>
                        </div>
                        <div class="flex-row">
                            <p class="text-right text-base">
                                {{ Math.round(item.price /100) }},00 €
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

    </div>
</template>

<script>

export default {
    name: 'RestaurantInfo',
    props: ['id'],
    data() {
        return {
            // id: this.$route.params.id,
            // restaurant: {},
        }
    },
}
</script>