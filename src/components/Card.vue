<template>
  <b-col col>
    <b-card :img-src="imageUrl" img-alt="Card Image" img-top class="mb-4">
      <p v-if="mostRead" class="h4 mb-2 float-right" v-b-tooltip.hover title="Most Read">
        <b-icon icon="star-fill" aria-hidden="true" variant="warning"></b-icon>
      </p>
      <b-card-title>
        <b-link :href="url">
          {{ title }}
        </b-link>
      </b-card-title>
      <b-card-text>
        {{ excerpt }}
      </b-card-text>
      <template #footer>
        <small class="text-muted float-left">Last updated {{ formattedDate }}</small>
        <small class="text-muted float-right">{{ readingTime }}</small>
      </template>
    </b-card>
  </b-col>
</template>

<script>
export default {
  name: 'Card',
  props: {
    title: {
      type: String,
      required: true
    },
    imageUrl: {
      type: String,
      required: true
    },
    excerpt: {
      type: String,
      required: true
    },
    date: {
      type: String,
      required: true
    },
    readingTime: {
      type: String,
      required: true
    },
    url: {
      type: String,
      required: true
    },
    mostRead: {
      type: Boolean,
      required: true
    }
  },
  computed: {
    formattedDate () {
      return new Date(this.date * 1000).toLocaleString()
    }
  }
}
</script>
