<template>
  <section id="team" class="hero is-medium" style="background-color: whitesmoke">
    <div class="hero-body">
      <div class="container has-text-centered">
        <h1 class="title is-spaced">Отзывы</h1>

        <div class="columns">
          <div class="column">
            <p>ОсОО уже на протяжении длительного времени осуществляет перевозки согласно наших заявок и показывет хорошую организацию работы, четкое выполнение гарантийных обязательств и умение оперативно решать поставленные задачи. За время исполнения транспортно-экспедиторского договора, сотрудники ОсОО «Сонора» продемонстрировали высокий уровень провессионализма, коммуникабельность, ответственность и готовность к сотрудничеству. Мы можем рекомендовать ОсОО «Сонора», как надёжного партнёра, предоставляющего своим клиентам дополнительную возможность для развития бизнеса.</p>
          </div>
          <div class="column">
          <p>Транспортная компания является нашим постоянным партнером в области логистических услуг. За время длительного сотрудничества ОсОО «Сонора» подтвердило свой высокий профессиональный подход в организации международных грузовых перевозок, компетентность и оперативность в решении поставленных задач. Все перевозки выполняются в строго оговоренные сроки и с надлежащим качеством. Каждый проект опирается на эффективную схему взаимодействия сотрудников компании и клиента. Эта компания заслужила авторитет организации, которой можно доверить решение самых сложных вопросов. Мы удовлетворены деятельностью ОсОО «Сонора» и рекомендуем эту компанию как профессионального и надежного партнера.</p>
          </div>
          <div class="column">
          <p>ОсОО  является нашим постоянным партнером в области грузоперевозок. За время сотрудничества эта компания показала свою способность с полной ответственностью подходить к поставленным задачам, выполнять работы качественно и в срок. Отличительной чертой работы ОсОО «Сонора» является высокий профессионализм, организованность сотрудников компании и внимательное отношение к клиенту. Рекомендуем ОсОО «Сонора» как надежного и стабильного делового партнера.</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>

  export default {
    name: 'team',
    components: {
    },
    data () {
      return {
        persons: [
          {
            id: 'mmorainville',
            name: 'Mathieu Morainville',
            avatar: 'https://avatars1.githubusercontent.com/u/1155743?v=4&s=460',
            image: '/images/team/superman.png',
            description: '<em>Vueman</em>',
            skills: ['Vue.js', 'JavaScript', 'Design', 'Node.js'],
            link: 'https://github.com/mmorainville'
          },
          {
            id: 'sylver-john',
            name: 'Sylver-John Imhoff',
            avatar: 'https://avatars1.githubusercontent.com/u/6161547?v=4&s=460',
            image: '/images/team/batman.jpg',
            description: '<em>Golang lover</em>',
            skills: ['Golang', 'Vue.js', 'JavaScript'],
            link: 'https://github.com/sylver-john'
          },
          {
            id: 'Outpox',
            name: 'Guillaume Migeon',
            avatar: 'https://avatars2.githubusercontent.com/u/3439246?v=4&s=460',
            image: '/images/team/flash.jpg',
            description: '<em>Extension maker</em>',
            skills: ['Vue.js', 'JavaScript', 'Node.js'],
            link: 'https://github.com/Outpox'
          }
        ]
      }
    },
    mounted () {
      this.persons.sort(() => { return 0.5 - Math.random() })
    }
  }
</script>
