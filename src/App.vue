<template>
  <h1>{{ title }}</h1>
  <input type="text" ref="bebo">
  <button @click="handleClick"></button>
  <br>
  <div v-if="toggle">
  
    <mmodel :header="header" :text="text" theme="sale" @closeModel="toggleModel">                              <!--https://youtu.be/GWRvrSqnFbM?t=2266-->
    <!--حتى اربط بين الكليك او دكمه بالموديل فيو السطر بال3 ويه فانكشن بالفيو الاب الي هي مال توكل موديل $emitالكلوس موديل هاي كوستم فانكشن مال فيو اني سويته عنطريق ال-->
    <!-- https://youtu.be/KM1U6DqZf8M?t=1322 -->
       <div>
         <h2>hala wala bil shabab</h2>
         <h4>3teeeh</h4>
       </div> <!--ذني راح يندزن للسلوت الديفولت المابيه ارتبدتيود بالموديل فيو-->

       <template v-slot:named-slot>  
          <a href="http://" target="_blank" rel="noopener noreferrer">gega</a>
       </template> <!--ذني راح يندزن للسلوت الي اسمه نايمدسلوت بالموديل فيو  و السلوت فكرته مثل بروبس بس ينقل تمبلات جبيرة بدل بيانات مفرده للكومبونتس-->
    </mmodel>
  
  </div>
  <button @click.alt="toggleModel">click me! (alt)</button>
</template>

<script>
import mmodel from './components/model.vue'       //https://youtu.be/GWRvrSqnFbM?t=2220

export default {

  components: {mmodel},                            //https://youtu.be/GWRvrSqnFbM?t=2259
  name: 'App',
  data(){
    return{
      title:'my first vue pro',               //https://youtu.be/GWRvrSqnFbM?t=1279
      header:'you won a giveaway !',
      text:'take it ',
      toggle: false,
    }
  },
  methods:{
   handleClick(){
    console.log(this.$refs.bebo);           //https://youtu.be/GWRvrSqnFbM?t=1667
    this.$refs.bebo.classList.add('gg');
    this.$refs.bebo.focus();                 //https://youtu.be/GWRvrSqnFbM?t=1742
   },
   toggleModel(){
    this.toggle=!this.toggle
   }

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h1{
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;
}
</style>
