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

        <div class="flex flex-col">
            <h2 class="text-2xl font-bold">Menu</h2>
        </div>
        <div class="flex w-full rounded-lg shadow-lg mb-8">
            <div class="p-4 flex-col w-full">
                <h5 class="text-left text-2xl font-bold mb-2">Entrées</h5>
                <div class="flex justify-between">
                    <div class="flex-col">
                        <p class="text-left text-base">
                            Potatoes
                        </p>
                    </div>
                    <div class="flex-col">
                        <p class="text-right text-base">
                            2,80€
                        </p>
                    </div>
                </div>
            </div>
        </div>
        <div class="flex w-full rounded-lg shadow-lg mb-8">
            <div class="p-4 flex flex-col w-full">
                <h5 class="text-left text-2xl font-bold mb-2">Plats</h5>
                <div class="flex justify-between">
                    <div class="flex-col">
                        <p class="text-left text-base">
                            Basic Burger 
                        </p>
                    </div>
                    <div class="flex-col">
                        <p class="text-right text-base">
                            5,00€
                        </p>
                    </div>
                </div>
            </div>
        </div>
        <div class="flex w-full rounded-lg shadow-lg mb-8">
            <div class="p-4 flex flex-col w-full">
                <h5 class="text-left text-2xl font-bold mb-2">Desserts</h5>
                <div class="flex justify-between">
                    <div class="flex-col">
                        <p class="text-left text-base">
                            Vanilla Ice cream
                        </p>
                    </div>
                    <div class="flex-col">
                        <p class="text-right text-base">
                            2,50€
                        </p>
                    </div>
                </div>
            </div>
        </div>
        <div class="flex w-full rounded-lg shadow-lg mb-8">
            <div class="p-4 flex flex-col w-full">
                <h5 class="text-left text-2xl font-bold mb-2">Boissons</h5>
                <div class="flex justify-between">
                    <div class="flex-col">
                        <p class="text-left text-base">
                            Coca Cola
                        </p>
                    </div>
                    <div class="flex-col">
                        <p class="text-right text-base">
                            2,00€
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

export default {
    name: 'RestaurantInfo',
}
</script>