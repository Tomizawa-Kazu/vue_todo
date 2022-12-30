# Vue Docker環境

### コマンド
- コンテナの起動
  - ```docker-compose up -d```

- コンテナに入る方法
  1. ```docker-compose exec app /bin/bash```　もしくは
  2. ```docker containew exec -it vue-project bash```

- Vueをつくるコマンド
  - ```vue create .```

- Vue実行方法
  1. コンテナに入っている場合、```yarn serve```
  2. コンテナに入っていない場合、```docker-compose exec app yarn serve```

### Todoイメージ
![Todo](/img/image01.png) 

### 参考記事
- [yarn ](https://zenn.dev/chida/articles/8f16e42364398c)

### Project setup
```
yarn install
```

### Compiles and hot-reloads for development
```
yarn serve
```

### Compiles and minifies for production
```
yarn build
```

### Lints and fixes files
```
yarn lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
