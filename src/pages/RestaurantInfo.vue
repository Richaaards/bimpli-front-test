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
        <menu-section
            :menuTypeTitle="'Entrées'"
            :items="this.$route.params.restaurant.dishes.data"
            :menuType="'starter'"
        />
        
        <menu-section
            :menuTypeTitle="'Plats'"
            :items="this.$route.params.restaurant.dishes.data"
            :menuType="'main'"
        />

        <menu-section
            :menuTypeTitle="'Désserts'"
            :items="this.$route.params.restaurant.dishes.data"
            :menuType="'dessert'"
        />

        <menu-section
            :menuTypeTitle="'Boissons'"
            :items="this.$route.params.restaurant.dishes.data"
            :menuType="'drink'"
        />

    </div>
</template>

<script>
import MenuSection from '../components/MenuSection'

export default {
	components: { MenuSection },
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