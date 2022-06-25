<template>
    <div class="tw-flex tw-justify-center tw-items-center tw-h-full">
        <div>
            <div class="tw-text-4xl md:tw-text-5xl tw-font-black tw-text-center tw-mb-4">
                {{ quote }}
            </div>
            <div class="tw-text-2xl md:tw-text-3xl tw-text-center tw-mb-4 tw-italic tw-font-serif">
                {{ author }}
            </div>
            <div class="tw-flex tw-justify-center">
              <v-btn
                :loading="btnLoading"
                :disabled="btnLoading"
                color="deep-orange"
                class="ma-2 white--text"
                @click="nextQuote()"
              >
                Next
                <v-icon
                  right
                  dark
                >
                  mdi-arrow-right
                </v-icon>
              </v-btn>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'IndexPage',
    layout: 'home',

    data () {
      return {
        quote: "...",
        author: "",
        btnLoading: false
      }
    },

    mounted() {
      this.fetchQuote()
    },

    methods: {
      async fetchQuote () {
        await this.$axios.get('https://api.quotable.io/random')
          .then(response => {
            // console.log(response)
            this.quote = '"' + response.data.content + '"'
            this.author = response.data.author
          })
          .finally(() => {
            if (this.btnLoading) {
              this.btnLoading = false
            }
          })
      },

      nextQuote () {
        this.btnLoading = true
        this.fetchQuote()
      }
    },
}
</script>

<style>

</style>
