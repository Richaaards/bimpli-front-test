<template>
    <div 
        id="items"
        class="flex flex-col w-full rounded-lg shadow-lg mb-8 py-2"
    >   
        <div class=w-full> 
            <h5 class="text-left text-2xl font-bold m-4">{{ menuTypeTitle }}</h5>
        </div>
        <div 
            v-for="item in items"
            :key="item.id"
        >
            <div v-if="item.type === `${menuType}`">
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
    </div>
</template>

<script>

export default {
    name: 'MenuSection',
    props: {
        menuTypeTitle: {
            type: String,
            required: true,
        },
        items: {
            type: Array,
            required: true,
        },
        menuType: {
            type: String,
            required: true,
        },
    }
}
</script>
