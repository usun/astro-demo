# Astro Starter Kit: Minimal

```sh
npm create astro@latest -- --template minimal
```

> 🧑‍🚀 **Seasoned astronaut?** Delete this file. Have fun!

## 🚀 Project Structure

Inside of your Astro project, you'll see the following folders and files:

```text
/
├── public/
├── src/
│   └── pages/
│       └── index.astro
└── package.json
```

Astro looks for `.astro` or `.md` files in the `src/pages/` directory. Each page is exposed as a route based on its file name.

There's nothing special about `src/components/`, but that's where we like to put any Astro/React/Vue/Svelte/Preact components.

Any static assets, like images, can be placed in the `public/` directory.

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help` | Get help using the Astro CLI                     |

## 👀 Want to learn more?

Feel free to check [our documentation](https://docs.astro.build) or jump into our [Discord server](https://astro.build/chat).

## usun 总结
- 使用idea，编写astro项目，需要安装astro插件，帮助快速编写：高亮、提示、代码补充等。
- astro类似写html:使用相对路径访问页面和mardown文件。
- pages目录下面如果有index.astro文件，访问目录默认会访问index.astro。如：http://localhost:4321/tags/
- 编写 Astro 模板非常像编写 HTML，但你可以在其中加入 JavaScript 表达式。
  - frontmatter中的代码栅栏之间，可以添加JavaScript，在页面可以直接引用。类似：{pageTitle}
  - 在你的 Astro 脚本中使用 JavaScript 或 TypeScript 表达式定义变量。
  - 你可以在你的 .astro 文件的任何部分使用所有现代的 JavaScript 逻辑运算符、表达式和函数。但是，大括号仅在 HTML 模板主体中是必要的。 
  - Astro 的模板语法类似于 JSX 语法。如果你想知道如何在你的 HTML 中使用你的脚本，那么搜索一下 JSX 中是如何做到的，这可能是一个很好的出发点！
  - 可以在代码围栏中定义变量，然后在样式标签中将其用作 CSS 变量使用。
  - 全局样式：将下面的 import 语句添加到 about.astro 文件的 frontmatter 中.
- 添加和使用组件，astro组件是可以重复使用的代码片段。如：src/components/Navigation.astro
  - 在组件脚本的顶部，也就是代码块内添加一个导入语句。
  - 用导航组件替换现有的代码。
- 布局："<slot />"
  - 让布局负责渲染任何共同的 HTML,在页面定义其他html内容。
  - 使用布局，可以在 Markdown内容或布局中包含元素。
- astro api
  - import.meta.glob() 从项目中访问文件中的数据
  - getStaticPaths() 批量创建多个页面（路由）
  - Astro 的 RSS 包来创建一个 RSS 订阅