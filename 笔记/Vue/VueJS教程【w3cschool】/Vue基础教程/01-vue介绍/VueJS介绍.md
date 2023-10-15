在html中引入Vue.js
    <script src="https://cdn.jsdeliver.net/npm/vue@2/dist/vue.js"></script>

声明式渲染
    <div id="app">
        {{message}}
    </div>
    var app = new Vue({
        el: '#app',
        data: {
            message: 'hello vue!'
        }
    })