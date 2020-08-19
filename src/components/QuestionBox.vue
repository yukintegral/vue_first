<template>
  <div class="question-box-container">
  <b-jumbotron header="利き脳診断" lead="Bootstrap v4 Components for Vue.js 2">
    <template v-slot:lead>
      {{ currentQuestion.question }}
    </template>

    <hr class="my-4" />
    <!-- 出題 -->
    <b-list-group>
        <b-list-group-item
            <p v-for="(answer, index) in answers"
            :key="index" >
            {{ answer }}
        </p>
        </b-list-group-item>
    </b-list-group>


    <!-- 回答が出てくる -->
    
    <b-button variant="primary" href="#">Submit</b-button>
    <b-button @click="next" variant="success" href="#">Next</b-button> 
  </b-jumbotron>

</div>
</template>

<script>
export default {
  props: {
    currentQuestion: Object,
    next: Function
  },

  computed: {
    answers() {
      let answers = [...this.currentQuestion.incorrect_answers]
      return answers.push(this.currentQuestion.correct_answer)
    }
  },

  // methods: {
  //   selectAnswer(index){
  //     this.selectedIndex = index
  //   }  
  //   },

  mounted(){     
      console.log(this.currentQuestion)
    }
  }
</script>

<style>
  .list-group {
    margin-bottom: 15px;
  }
  .btn {
    margin: 0 5px;
  }
</style>