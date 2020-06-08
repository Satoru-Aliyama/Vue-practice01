<template>
    <div class="all">
        <Bar :quotes="quotes"></Bar>
        
        <div class="quote">
            <h2>Quate</h2>
            <p class="alert" v-if="quotes.length > 9">Limited</p>
            <div class="quote_inner">
                <textarea class="textArea" v-model="quote"></textarea>
                <button class="addBtn" @click="add">Add Quote</button>
            </div>
        </div>
    
        <Added :quotes="quotes"></Added>
    </div>
    
</template>

<script>
import Bar from './Bar'
import Added from './Added'
export default {
    data() {
        return{
            quotes: [],
            quote: ''
        }
    },
    components:{
        Bar,
        Added
    },
    methods: {
        add() {
            if(this.quote && this.quotes.length < 10) {
            this.quotes.unshift(this.quote);
            } else if(!this.quote){
                alert('Type text')
            } else if(this.quotes.length > 10){
                alert('Limited is 10');
            }
            this.quote = '';
        },
    }
}
</script>

<style scoped>
.textArea {
  border: 1px solid #bbbbbb;
  width: 100%;
  height: 100px;
  border-radius: 10px;
  padding: 8px;
}
.quote {
  max-width: 600px;
  padding: 4%;
  margin: 0 auto;
}
.quote_inner {
 text-align: center;
}

.addBtn {
  display: inline-block;
  background-color: blue;
  color: #fff;
  border-radius: 5px;
  padding: 5px;
  margin-top: 30px;
}

.alert {
  color: red;
}
</style>