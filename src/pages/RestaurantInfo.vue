<template>
    <div class="flex flex-wrap p-8">        
        <section
            class="overflow-hidden bg-no-repeat bg-cover w-full"
            style="
                background-position: 50%;
                background-image: url('https://mdbcdn.b-cdn.net/img/new/slides/146.webp');
                height: 500px;
            "
        >
        </section>

        <section class="my-8 w-full text-left">
            <h2 class="text-3xl font-bold">{{ this.$route.params.restaurant.name }}</h2>
            <h3 class="text-2xl uppercase font-normal">{{ this.$route.params.restaurant.location }}</h3>
        </section>
    </div>
</template>

<script>

export default {
    name: 'RestaurantInfo',
}
</script>