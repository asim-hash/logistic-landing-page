<template>
  <section id="contact" class="section is-medium" style="background-color: rgba(0, 0, 0, 0.7)">
    <div class="container">
      <h1 class="title is-spaced has-text-centered has-text-grey-lighter">Оставить заявку</h1>

      <form action="https://formspree.io/pulsar.dev.team@gmail.com" method="POST">
        <div class="field">
          <label class="label" for="name">Имя</label>
          <div class="control">
            <input v-validate="'required'" v-model="name" class="input" :class="{ 'is-danger': errors.has('name') }" id="name" name="имя" type="text" placeholder="Name" required>
          </div>
          <span v-show="errors.has('name')" class="help is-danger">{{ errors.first('name') }}</span>
        </div>

        <div class="field">
          <label class="label" for="number">Номер телефона</label>
          <div class="control has-icons-left has-icons-right">
            <input v-validate="'required|number'" v-model="number" class="input" :class="{ 'is-danger': errors.has('number') }" id="number" name="number" type="text" placeholder="070054332452" required>
            <span class="icon is-small is-left has-text-grey"><i class="fa fa-envelope"></i></span>
            <span v-show="errors.has('number')" class="icon is-small is-right has-text-grey"><i class="fa fa-warning"></i></span>
          </div>
          <span v-show="errors.has('number')" class="help is-danger">{{ errors.first('number') }}</span>
        </div>
        <div class="field is-grouped">
          <div class="control">
            <input type="submit" class="button is-primary" value="Подать заявку">
          </div>
          <div class="control">
            <button class="button is-light" @click="cancel">Отменить</button>
          </div>
        </div>
      </form>
    </div>
  </section>
</template>

<script>
  export default {
    $_veeValidate: {
      validator: 'new'
    },
    name: 'contact',
    data () {
      return {
        name: '',
        number: ''
      }
    },
    methods: {
      cancel () {
        this.name = ''
        this.number = ''
      }
    }
  }
</script>

<style lang="scss" scoped>
  .input, .textarea {
    background-color: #363636;
    color: #dbdbdb;
  }

  .input:not(.is-danger), .textarea:not(.is-danger) {
    border: none;
  }

  .label {
    color: #b5b5b5;
  }
</style>
