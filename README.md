# xunfei-tts

## 介绍
`vue-xunfei-tts` 是一个适用于 **Vue 3** 的 **讯飞 TTS（语音合成）** 解决方案，基于 `Vite` 进行构建。

## 安装依赖
```sh
npm install
```

## 启动开发环境
```sh
npm run dev
```

## 生产环境构建
```sh
npm run build
```

## 代码格式检查
```sh
npm run lint
```

## 讯飞 TTS 使用方法
1. 在 **`src/utils/onlineTTS.js`** 位置，配置 **讯飞 API 相关的三个 Key**。** 三个相关key需要登录讯飞官方平台获取 **
2. 需要使用的三个 Key 说明：
   - `APPID`：应用 ID
   - `APIKey`：API 密钥
   - `APISecret`：API 密钥（加密用）

3. 示例代码：
```js
const APPID = 'xxx'
const API_SECRET = 'xxx'
const API_KEY = 'xxx'
```

## 参考文档
- [讯飞官方文档](https://www.xfyun.cn/doc/)

