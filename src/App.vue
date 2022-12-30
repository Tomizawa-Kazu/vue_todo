<template>
  <div id="app">
    <h1>My Todo App</h1>
    <div>
      <label for="title">タイトル：</label>
      <input type="text" v-model="title" placeholder="タイトル">
    </div>
    <div>
      <label for="body">内容：</label>
      <textarea v-model="body" placeholder="内容"></textarea>
    </div>
    <div>
      <input type="submit" value="追加" @click="addList">
    </div>
    <ul v-for="(list, i) in lists" v-bind:key="i">
      <li>id: {{ i }}, title: {{ list.title }} <button @click="deleteList(i)">削除</button></li>
    </ul>
    <pre>
      {{ $data }}
    </pre>
  </div>
</template>

<script>
export default {
  data: () => ({
    lists: [
      { title: '外へ行く', body: 'クレープ食べる' },
      { title: '買い物に行く', body: '夕ご飯' }
    ],
    title: '',
    body: ''
  }),
  methods: {
    // リストの追加
    addList: function () {
      if (this.title === '' || this.body === '') return
      this.lists.push({ title: this.title, body: this.body })
      this.title = ''
      this.body = ''
    },

    // リストの削除
    deleteList: function (i) {
      this.lists.splice(i, 1)
    }
  }
};
</script>