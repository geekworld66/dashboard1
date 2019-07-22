<script>
    Vue.component('basic-div', {
      props: ['title', 'count'],
      template: '<div class="div-wrapper">' +
          '<span>{{ title }}</span>' +
          '<span>{{ count }}</span>' +
          '</div>'
    })

    new Vue({
      el: '#app'
    })
</script>

<style lang="scss">
    .div-wrapper{
        width: 10%;
        height: 40px;
        background-color: #00FF00;
        margin: 0px auto;
    }
    .navigation {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }

    h1, h2 {
        font-weight: normal;
    }

    ul {
        list-style-type: none;
        padding: 0;
    }

    li {
        display: inline-block;
        margin: 0 10px;
    }

    a {
        color: #42b983;
    }
</style>
