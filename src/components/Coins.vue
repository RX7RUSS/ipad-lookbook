<template>
  <div>
    <p>Name: {{ coin.name }}</p>
    <p>Symbol: {{ coin.symbol }}</p>
    <p>Price (USD): {{ coin.price_usd }}</p>
    <p>Percentage Change Over 7 Days: {{ coin.percent_change_7d }}</p>
    <p>Rank: {{ coin.rank }}</p>
  </div>

</template>

<script>
import axios from 'axios'

export default {
  name: 'Coins',

  data () {
    return {
      coin: {}
    }
  },

  created () {
    this.fetchData()
  },

  watch: {
    '$route': 'fetchData'
  },

  methods: {
    fetchData () {
      axios.get('https://api.coinmarketcap.com/v1/ticker/' + this.$route.params.id + '/')
        .then((resp) => {
          this.coin = resp.data[0]
          console.log(resp)
        })
        .catch((err) => {
          console.log(err)
        })
    }
  }
}
</script>
