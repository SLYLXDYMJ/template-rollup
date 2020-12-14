## Rollup 类库脚手架

### 克隆本项目
```
git clone https://github.com/q-jason/template-rollup.git
```

### 使用指南
1. 根据需要修改 rollup.config.js 预设配置
2. 根据需要修改 package.json (name、version、main、module)
2. src/index.js 作为入口实现类库
3. 在 docs 目录实现预览（文档）页面（文档简单的话建议直接用 README.md）
4. 在根目录 npm run build 打包类库
5. 若需要文档则，配置好 travis-ci
6. 提交 git
7. 提交 npm

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
```

### travis-ci
> 该项目预览采用 travis-ci 自动打包部署 docs <br/>
> 根目录预设配置文件 .travis.yml <br/>
> 流程如下（PS: 从 hexo 文档中抄过来的....）：

1. 新建一个 repository。如果你希望你的站点能通过 <你的 GitHub 用户名>.github.io 域名访问，你的 repository 应该直接命名为 <你的 GitHub 用户名>.github.io。
2. 将你的 Hexo 站点文件夹推送到 repository 中。默认情况下不应该 public 目录将不会被推送到 repository 中，你应该检查 .gitignore 文件中是否包含 public 一行，如果没有请加上。
3. 将 [Travis CI](https://github.com/marketplace/travis-ci) 添加到你的 GitHub 账户中。
4. 前往 GitHub 的 [Applications settings](https://github.com/settings/installations)，配置 Travis CI 权限，使其能够访问你的 repository。
5. 你应该会被重定向到 Travis CI 的页面。如果没有，请 [手动前往](https://travis-ci.com/)。
6. 在浏览器新建一个标签页，前往 GitHub [新建 Personal Access Token](https://github.com/settings/tokens)，只勾选 repo 的权限并生成一个新的 Token。Token 生成后请复制并保存好。
7. 回到 Travis CI，前往你的 repository 的设置页面，在 Environment Variables 下新建一个环境变量，Name 为 GH_TOKEN，Value 为刚才你在 GitHub 生成的 Token。确保 DISPLAY VALUE IN BUILD LOG 保持 不被勾选 避免你的 Token 泄漏。点击 Add 保存。
8. 在你的 Hexo 站点文件夹中新建一个 .travis.yml 文件：

备注：
- https://travis-ci.com 是能看到 git 提交和构件失败原因的