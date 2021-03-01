<template>
  <div id="app">
    <b-container>
      <b-row cols="1" cols-md="2" cols-lg="3">
        <Card v-for="i in getRange(0, 3)" :key="i"
          :title="cards[i].title"
          :imageUrl="cards[i].image"
          :excerpt="cards[i].excerpt"
          :date="cards[i].date"
          :readingTime="cards[i].reading_time"
          :url="cards[i].url"
          :mostRead="cards[i].most_read"
        />
      </b-row>
      <b-row cols="1" cols-md="2" cols-lg="3">
        <Card v-for="i in getRange(3, 6)" :key="i"
          :title="cards[i].title"
          :imageUrl="cards[i].image"
          :excerpt="cards[i].excerpt"
          :date="cards[i].date"
          :readingTime="cards[i].reading_time"
          :url="cards[i].url"
          :mostRead="cards[i].most_read"
        />
      </b-row>
      <b-row cols="1" cols-md="2" cols-lg="3">
        <Card v-for="i in getRange(6, 8)" :key="i"
          :title="cards[i].title"
          :imageUrl="cards[i].image"
          :excerpt="cards[i].excerpt"
          :date="cards[i].date"
          :readingTime="cards[i].reading_time"
          :url="cards[i].url"
          :mostRead="cards[i].most_read"
        />
      </b-row>
    </b-container>
  </div>
</template>

<script>
import Card from './components/Card.vue'

const _ = require('lodash')

export default {
  name: 'App',
  data: () => ({
    cards: [
      {
        title: 'The Hidden Agenda Of Leads',
        image: 'https://picsum.photos/id/620/600.webp',
        excerpt: 'Mauris blandit placerat eros, vitae facilisis sapien pretium vitae. Vestibulum est libero, pretium et eleifend sit amet, tincidunt vulputate diam. Cras fringilla feugiat dui, in sagittis tellus laoreet non. Phasellus.',
        date: '1609261387',
        reading_time: '7 min',
        url: '#',
        most_read: false
      },
      {
        title: 'Ten Secrets That Experts Of Seo Don\'t Want You To Know',
        image: 'https://picsum.photos/id/619/600.webp',
        excerpt: 'Fusce malesuada ligula non nisl ultricies rutrum. Sed ac varius justo. Donec ac venenatis dui. Curabitur non sem nec ex tincidunt venenatis in non nunc. Sed posuere pretium turpis, vitae.',
        date: '1609347787',
        reading_time: '5 min',
        url: '#',
        most_read: false
      },
      {
        title: 'Learn From These Mistakes Before You Learn Seo',
        image: 'https://picsum.photos/id/618/600.webp',
        excerpt: 'Vestibulum quam neque, pellentesque sed felis vitae, luctus faucibus arcu. Donec sagittis sem ac cursus venenatis. Mauris fermentum ex ut lectus rhoncus, luctus placerat turpis rutrum. Praesent interdum justo non.',
        date: '1609174987',
        reading_time: '2 min',
        url: '#',
        most_read: false
      },
      {
        title: 'The Billionaire Guide On Boosting Your Sales That Will Get You Rich',
        image: 'https://picsum.photos/id/617/600.webp',
        excerpt: 'Aenean ac neque ut nisl sodales varius. Curabitur vel nisl vel lorem dignissim dapibus id vitae velit. Vivamus scelerisque sodales augue eget commodo. Nunc maximus, felis vel tristique placerat, velit.',
        date: '1609434187',
        reading_time: '20 min',
        url: '#',
        most_read: false
      },
      {
        title: '7 Various Ways To Do Marketing',
        image: 'https://picsum.photos/id/616/600.webp',
        excerpt: 'Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Ut velit nunc, euismod et finibus vel, tincidunt et massa. Nulla rutrum ornare enim, in pellentesque nisi.',
        date: '1609520587',
        reading_time: '30 seg',
        url: '#',
        most_read: true
      },
      {
        title: 'Why Is Everyone Talking About Marketing?',
        image: 'https://picsum.photos/id/615/600.webp',
        excerpt: 'Aenean rutrum erat quam, ut congue dolor pharetra ac. Nullam mauris mauris, dictum et congue ac, euismod vitae nisi. Quisque dolor mauris, sagittis ac ex sit amet, vehicula sodales orci.',
        date: '1609606987',
        reading_time: '3 min',
        url: '#',
        most_read: false
      },
      {
        title: 'Ten Unexpected Ways Marketing Can Make Your Life Better',
        image: 'https://picsum.photos/id/614/600.webp',
        excerpt: 'Morbi eget nisi sed justo tempus fringilla. Vestibulum nec dui nisi. Proin laoreet maximus ex, at mattis quam congue vitae. Duis erat dui, posuere ac laoreet quis, ultrices vitae dolor.',
        date: '1609693387',
        reading_time: '15 min',
        url: '#',
        most_read: true
      },
      {
        title: '5 Mind Numbing Facts About Leads',
        image: 'https://picsum.photos/id/617/600.webp',
        excerpt: 'Etiam vel elit sodales, gravida leo eget, ultrices dui. Morbi efficitur aliquam mi, ut molestie sem sollicitudin ac. Suspendisse posuere ante id massa tincidunt, quis tempus eros luctus. Nunc non.',
        date: '1609779787',
        reading_time: '1 min',
        url: '#',
        most_read: true
      }
    ]
  }),
  methods: {
    getRange (start, end) {
      return _.range(start, end)
    }
  },
  components: {
    Card
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
