<template>
  <div id="question">
    <div class="card text-center">
      <div class="card-header">
        {{title}}
      </div>
      <div class="card-body">
        <h5 class="card-title">{{subtitle}}</h5>
        <p class="card-text">{{text}}</p>
        
      </div>
      <div class="card-footer text-muted">
        <input type="text" class="form-control" placeholder="Введите ответ" v-model="answer"></input>
        <a href="#" class="btn btn-primary" @click="showAnswer()">Ответить</a>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        title: "Заголовок",
        subtitle: "Подзаголовок вопроса",
        text: "Текст вопроса",
        answer: ""
      }
    },
    methods: {
      showAnswer() {
        alert(this.answer);
      }
    }
  }
</script>

<style lang="scss">
  
</style>
