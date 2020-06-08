<template>
    <div class="added">
      <div class="each_quote" 
           v-for="(quote, index) in quotes" 
           :key="index" @click="dele(index)" >

        {{quote}}

      </div>
    </div>
</template>

<script>
export default {
    props:['quotes'],
    data() {
        return {
            show: false
        }
    },
    methods: {
        dele(index) {
            this.quotes.splice(index,1);
        }
    },
}

</script>

<style scoped>
.added {
  display: flex;
  flex-wrap: wrap;
  max-width: 900px;
  margin: 0 auto;
}
.each_quote:hover {
    background: #bbbbbb;
}
.each_quote {
  border: 1px solid #bbbbbb;
  width: 280px;
  height: 120px;
  border-radius: 10px;
  padding: 8px;
  font-size:1.5em;
  cursor: pointer;
  margin: 10px;
  position: relative;
}

</style>