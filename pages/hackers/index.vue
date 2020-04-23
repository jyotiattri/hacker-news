<template>
  <div>
    <Hacker v-for="(item, index) in hackers" :key="item.id" :index="index + 1"  :hacker="item" />
  </div>
</template>

<script>
import Hacker from '../../components/Hacker';
import axios from 'axios'
export default {
  components: {
    Hacker
  },
  data() {
    return {
      hackers: []
    }
  },
  async created() {
    const config = {
      headers: {
        Accept: 'application/json'
      }
    }
    try {
      const res = await this.$axios.get(
        'https://api.hackerwebapp.com/news?page=1',
        config
      )
    console.log(res)
      this.hackers = res.data
    } catch (err) {
      console.log(err)
    }
  },

  head() {
    return {
      title: 'Hacker News',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Hacker News'
        }
      ]
    }
  }
}
</script>

<style>
</style>