<template>
    <nuxt-link :to="'hackers/'+id">
    <div class="hacker">
        <ul>
            <li> <nuxt-link :to="`/news/${hacker.id}`">
            <div>
            {{index}}
                <div class="votearrow" title="upvote"></div>
                <span class="title">{{ hacker.title }}</span>
                <span>({{hacker.domain}})</span>
            </div>
            <div>
                <span>{{hacker.points}}</span> 
                <span>points by</span> 
                <span>{{hacker.user}}</span>
                <span>{{hacker.time_ago}}</span> |
                <span>{{hacker.comments_count}}</span>
            </div>
            </nuxt-link>
            </li>
        </ul>
        
    </div>
    </nuxt-link>
</template>

<script>
export default {
    name: 'hacker',
    props: ['hacker', 'index']
}
</script>

<style>
.hacker {
    padding: 0 1rem;
    margin: 1rem;
}
.votearrow {
    width: 10px;
    height: 10px;
    border: 0px;
    margin: 3px 2px 6px;
    background: url("~assets/images/grayarrow.gif") no-repeat;
    position: absolute;
}
span {
    font-size: 12px;
    color: #999;
}
span.title {
    font-size: 14px;
    color: #000;
}
</style>