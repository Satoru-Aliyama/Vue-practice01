<template>

    <div>
        <h1>Quates Added</h1>
        <div class="bar">
            <div class="inBar" :style="{width: quotes.length * 10 + '%'}">
                <div class="bar_text" v-if="quotes.length > 0">
                    <span>{{quotes.length}}/10</span>
                </div>
            </div>
        </div>
    </div>
    
</template>

<script>
export default {
    props:['quotes']
}
</script>

<style scoped>
.bar {
  width: 100%;
  height: 30px;
  background-color: #eae8e8;
  position:relative;
  border-radius: 10px;
  margin-top: 40px;
  
}
.inBar {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: blue;
  border-radius: 10px;
  transition: width .3s;
}
.bar_text {
  color: #fff;
  font-size:.75em;
  text-align: center;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
</style>