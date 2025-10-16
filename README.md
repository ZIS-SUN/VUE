# Vue 快速入门指南

## 快速开始

### 方式1：直接打开HTML文件
直接在浏览器中打开 `index.html` 即可看到效果！

### 方式2：使用本地服务器（推荐）
```bash
# 使用Python启动服务器
python3 -m http.server 8080

# 或使用Node.js的http-server
npx http-server
```

然后访问 http://localhost:8080

## Vue核心概念讲解

### 1. 数据绑定 (v-model)
```javascript
<input v-model="name">
```
双向数据绑定：输入框的值和数据自动同步

### 2. 事件处理 (@click)
```javascript
<button @click="increment">增加</button>
```
`@click` 是 `v-on:click` 的简写

### 3. 列表渲染 (v-for)
```javascript
<li v-for="(todo, index) in todos" :key="index">
  {{ todo }}
</li>
```
循环渲染数组中的每一项

### 4. 条件渲染 (v-if)
```javascript
<p v-if="showMessage">显示内容</p>
```
根据条件决定是否渲染元素

### 5. 插值表达式 {{ }}
```javascript
<p>Hello, {{ name }}!</p>
```
在模板中显示数据

## 创建正式Vue项目

### 使用 create-vue（Vue官方脚手架）

```bash
# 1. 创建项目
npm create vue@latest

# 项目配置选项：
# ✔ Project name: my-vue-app
# ✔ Add TypeScript? No
# ✔ Add JSX Support? No
# ✔ Add Vue Router? Yes
# ✔ Add Pinia? Yes
# ✔ Add Vitest? No
# ✔ Add ESLint? Yes

# 2. 进入项目
cd my-vue-app

# 3. 安装依赖
npm install

# 4. 启动开发服务器
npm run dev
```

### 项目结构
```
my-vue-app/
├── public/          # 静态资源
├── src/
│   ├── assets/      # 资源文件（图片、样式等）
│   ├── components/  # 组件
│   ├── views/       # 页面
│   ├── router/      # 路由配置
│   ├── stores/      # 状态管理
│   ├── App.vue      # 根组件
│   └── main.js      # 入口文件
├── index.html
└── package.json
```

## Vue单文件组件 (.vue)

```vue
<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <button @click="count++">计数: {{ count }}</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      msg: 'Hello Vue!',
      count: 0
    }
  }
}
</script>

<style scoped>
h1 {
  color: #42b983;
}
</style>
```

## 常用Vue指令

| 指令 | 说明 | 示例 |
|------|------|------|
| `v-model` | 双向数据绑定 | `<input v-model="text">` |
| `v-bind` | 属性绑定（简写 `:`） | `:src="imageUrl"` |
| `v-on` | 事件绑定（简写 `@`） | `@click="handler"` |
| `v-if` | 条件渲染 | `v-if="isShow"` |
| `v-show` | 条件显示（CSS） | `v-show="isVisible"` |
| `v-for` | 列表渲染 | `v-for="item in items"` |

## 学习路线建议

1. **基础阶段**（1-2周）
   - HTML/CSS/JavaScript基础
   - Vue基本语法和指令
   - 组件的概念

2. **进阶阶段**（2-3周）
   - 组件通信（props、emit）
   - 生命周期钩子
   - 计算属性和侦听器
   - Vue Router（路由）

3. **实战阶段**（持续）
   - Pinia/Vuex（状态管理）
   - HTTP请求（axios）
   - 实际项目开发

## 推荐资源

- 官方文档：https://cn.vuejs.org/
- Vue教程：https://cn.vuejs.org/tutorial/
- Vue Playground：https://play.vuejs.org/

## 下一步

1. 打开 index.html 查看示例效果
2. 尝试修改代码，观察变化
3. 创建自己的第一个Vue项目
4. 学习Vue Router和Pinia

祝你学习愉快！
