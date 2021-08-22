<template>
    <div class="mx-auto text-center w-2/5">
        <h1 class="text-3xl text-white text-mono py-6">Laravel official links</h1>

        <div>
            <list-item v-for="item in items" :key="item.title" :item="item" />
        </div>
    </div>
</template>

<script>
import ListItem from '@/components/ListItem.vue'
import officialLinks from '@/data/official.json'
import { sortByTitle } from '@/helpers'

export default {
    name: 'Official',
    components: {
        ListItem
    },
    data() {
        return {
            items: sortByTitle(officialLinks)
        }
    }
}
</script>