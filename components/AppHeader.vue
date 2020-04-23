<template>
    <header class="header">
        <ul>
            <li>
                <nuxt-link to='/hackers'><img src="~assets/images/y18.gif" alt="logo" style="border:1px solid #fff;"/></nuxt-link>
            </li>
            <li>
                <nuxt-link to='/hackers'><b>Hacker News</b></nuxt-link>
            </li>
             <li>
                <nuxt-link to='/news'>News</nuxt-link>|
            </li>
             <li>
                <nuxt-link to='/past'>Past</nuxt-link>|
            </li>
             <li>
                <nuxt-link to='/comments'>comments</nuxt-link>|
            </li>
             <li>
                <nuxt-link to='/ask'>ask</nuxt-link>|
            </li>
             <li>
                <nuxt-link to='/show'>show</nuxt-link>|
            </li>
            <li>
                <nuxt-link to='/jobs'>jobs</nuxt-link>|
            </li>
            <li>
                <nuxt-link to='/submit'>submit</nuxt-link>
            </li>
            <li class="right">
                <nuxt-link to='/login'>login</nuxt-link>
            </li>
        </ul>
    </header>
</template>

<script>
export default {
    name: 'AppHeader',

}


</script>

<style>
.header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 1rem;
    background: #ff6600;
    width: 100%;
}
.header .title {
    font-size: 3rem;
    color: #526488;
}

.header ul {
    display: flex;
}

.header a {
    display: inline-block;
    color: #000;
    padding: 0.3rem;
}

.right {
    float: right;
}
</style>