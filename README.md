## Rollup 类库脚手架

### 克隆本项目
```
git clone https://github.com/q-jason/template-rollup.git
```

### 使用指南
1. 根据需要修改 rollup.config.js 预设配置
2. 根据需要修改 package.json (name、version、main、module)
3. src/index.js 作为入口实现类库
4. 在 docs_src 目录实现预览（文档）页面
5. 文档简单的话建议直接用 README.md 来写
6. 分别打包类库和文档
7. 提交 git，同时将 docs 目录设置 github page
8. 提交 npm

PS: rollup.config.js
```javascript
// 1. 修改类库名称
const NAME = '_'

// 2. 修改 output
output: [ /* ... */ ]
```

### 命令行
1. 类库开发环境
```bash
npm run dev
```

2. 类库打包
```bash
npm run build
```

3. docs 开发环境
```bash
cd docs
npm run dev
npm run build
```