<template>
    <div class="news-list-nav">
        <router-link v-if="page > 1" :to="`/${feed}/${page -1}`">
            &lt; prev
        </router-link>
        <a v-else class="disbled">&lt; prev</a>
        <span>{{ page }}/{{ maxPage }}</span>
        <router-link v-if="hasMore" :to="`/${feed}/${page + 1}`">
        more &gt;
        </router-link>
        <a v-else class="disabled">more &gt;</a>
        </div>
</template>

<script>
export default {
    prps: {
        feed: {
            type: String,
            required: true
        },
        page: {
            type: Number,
            required: true
        },
        maxPage:{
            type: Number,
            required: true
        }

    }
}
</script>