# zhuoxingzhang.github.io

我的个人学术主页，线上地址 <https://zhuoxingzhang.github.io>。

这是一个普通的 Jekyll 站点，GitHub Pages 每次收到推送都会自动重新构建，
本地不需要安装任何东西。**日常维护只要改 `_data/` 里的三个 YAML 文件**，
推送后大约一分钟就会上线。

---

## 目录

1. [最简单的更新方法：直接在 GitHub 网页上改](#1-最简单的更新方法直接在-github-网页上改)
2. [常见任务速查](#2-常见任务速查)
3. [各部分内容怎么改](#3-各部分内容怎么改)
4. [改外观：颜色、字体、小标题](#4-改外观颜色字体小标题)
5. [进阶：加板块、加图标、加会议颜色、换网站图标](#5-进阶加板块加图标加会议颜色换网站图标)
6. [发布之后怎么确认上线了](#6-发布之后怎么确认上线了)
7. [YAML 易错点](#7-yaml-易错点)
8. [出问题了怎么办](#8-出问题了怎么办)
9. [本地预览（可选）](#9-本地预览可选)
10. [文件结构](#10-文件结构)
11. [几条不要动的规矩](#11-几条不要动的规矩)

---

## 1. 最简单的更新方法：直接在 GitHub 网页上改

不用开电脑上的任何工具，浏览器就够了：

1. 打开仓库 <https://github.com/zhuoxingzhang/zhuoxingzhang.github.io>。
2. 点进要改的文件，比如 `_data/publications.yml`。
3. 点右上角的铅笔图标（Edit this file）。
4. 改完点绿色的 **Commit changes**，再确认一次。
5. 等一分钟左右，刷新主页就能看到。

在自己电脑上改也一样：改文件，然后 `git add`、`git commit`、`git push`。

> 每次改完，最好用**手机**打开主页看一眼。这个页面在手机上排版最紧，
> 问题一般先在手机上暴露。

---

## 2. 常见任务速查

| 我想要……                         | 改哪个文件                  | 看第几节 |
| -------------------------------- | --------------------------- | -------- |
| 加一篇论文                        | `_data/publications.yml`    | 3.5      |
| 发一条新闻                        | `_data/news.yml`            | 3.4      |
| 改自我介绍（About）               | `_data/profile.yml`         | 3.2      |
| 改研究方向（Research）            | `_data/profile.yml`         | 3.3      |
| 改名字、职位、单位、一句话简介      | `_data/profile.yml`         | 3.1      |
| 加/删页头的链接按钮（Scholar 等）  | `_data/profile.yml`         | 3.1      |
| 换邮箱                            | `_data/profile.yml`         | 3.6      |
| 换头像                            | `images/` + `profile.yml`   | 3.7      |
| 挂 CV                             | `assets/` + `profile.yml`   | 3.7      |
| 改明信片上那段话                   | `index.html`                | 3.6      |
| 改板块旁边的小字（"say hello" 等） | `index.html`                | 4.3      |
| 改颜色                            | `assets/css/site.css` 顶部  | 4.1      |
| 改搜索引擎看到的网站描述            | `_config.yml`               | —        |

---

## 3. 各部分内容怎么改

### 3.1 页头（深蓝色夜空那块）

全部在 `_data/profile.yml`：

| 字段           | 显示在哪                              | 留空或删掉会怎样       |
| -------------- | ------------------------------------- | ---------------------- |
| `name`         | 大标题，也是导航栏左边的名字            | 必填                   |
| `pronouns`     | 名字旁边的绿色小标签（he/him）           | 标签消失               |
| `title`        | 名字下面第一行（PhD Candidate …）       | —                      |
| `department`   | 第二行，学院名                          | 只显示学校             |
| `affiliation`  | 第二行，学校名                          | —                      |
| `location`     | 带定位图标的那一行，也用在明信片地址里   | 那一行消失             |
| `greeting`     | 头像旁边的对话气泡                      | 气泡消失               |
| `tagline`      | 黄色的一句话简介                        | 那一行消失             |
| `photo`        | 头像贴纸                                | 显示名字首字母         |
| `links`        | 一排彩色按钮                            | —                      |
| `cv`           | 按钮最后多一个 CV                       | 不显示 CV 按钮         |

**链接按钮**的写法：

```yaml
links:
  - name: Google Scholar
    url: https://scholar.google.com/citations?user=...
  - name: GitHub
    url: https://github.com/zhuoxingzhang
```

按钮颜色按顺序自动轮换：黄、粉、蓝、绿、紫、蜜桃色。调换顺序，颜色也跟着变。

### 3.2 About

`profile.yml` 里的 `about`，**一个 `-` 就是一段**：

```yaml
about:
  - >-
    第一段英文……可以随便换行，
    渲染时会连成一段。
  - >-
    第二段……
```

段落里可以写 HTML，比如 `<a href="https://...">链接</a>`、`<em>斜体</em>`。

### 3.3 Research

所有研究方向都在**一张卡片**里，一个方向一句话，前面用小图标当项目符号。
对应 `profile.yml` 里的 `interests`，一个 `-` 就是一条：

```yaml
interests:
  - icon: key                          # 这一条前面的小图标
    text: >-
      <strong>Mixed covers</strong> that let the keys a database already
      enforces do most of the integrity work.
```

- 用 `<strong>…</strong>` 括起来的词会加粗，下面还会画一道和图标同色的荧光笔。
  每条最好只标一个关键词，扫一眼就知道是哪个方向。
- `icon` 可选 `database`、`key`、`search`、`log`，另外还有 `mail`、`pin`、`sparkle`、`moon`。
  不写会显示一颗星星（sparkle）；名字拼错的话，图标框里是空的。
- 图标颜色按顺序轮换：黄、粉、蓝、绿。
- 懒得配图标的话，也可以直接写一句话：`- Some new direction.`，前面自动用星星。
- 句子尽量短，电脑上一行、手机上三四行最合适。详细的介绍放在 About 里。
- 句子里如果有不想被拆开的词（比如 `TPC-H` 不希望断成 `TPC-` 和 `H`），
  这样写：`<span class="nb">TPC-H</span>`。

### 3.4 News

`_data/news.yml`，**写在最上面的就是最新的**，页面按文件里的顺序显示：

```yaml
- date: 2026-10
  text: >-
    <em>论文标题</em> has been accepted to <strong>VLDB 2027</strong>.
```

- `date` 是自由文本，`2026`、`2026-10`、`Oct 2026` 都可以。
- `text` 里可以用 HTML：`<em>`（斜体）、`<strong>`（加粗）、`<a href="...">`（链接）。
- 页面只直接显示**前 5 条**，更早的自动收进一个 "Earlier news" 折叠按钮。
- 把整个文件清空，News 板块和导航栏里的 News 会一起消失。

### 3.5 论文

`_data/publications.yml`。复制一段已有的，改成新论文就行：

```yaml
- title: The Title of the Paper
  authors: Yanni Tang, Zhuoxing Zhang, Sebastian Link
  venue: SIGMOD
  venue_full: Proceedings of the ACM on Management of Data
  year: 2027
  type: conference
  award: Best Paper
  links:
    - {name: DOI, url: "https://doi.org/10.1145/xxxxxxx"}
    - {name: PDF, url: "/assets/papers/my-paper.pdf"}
    - {name: Code, url: "https://github.com/zhuoxingzhang/xxx"}
```

| 字段          | 说明                                                                  |
| ------------- | --------------------------------------------------------------------- |
| `title`       | 必填                                                                   |
| `authors`     | 必填，逗号分隔。自己的名字会**自动加粗并画上荧光笔**                     |
| `venue`       | 必填，显示成彩色印章。**用简短的一个词**，比如 `SIGMOD`、`VLDBJ`         |
| `venue_full`  | 可选，鼠标悬停在印章上时显示的全称                                      |
| `year`        | 必填，按年份分组，新的在上面                                            |
| `type`        | `journal` 或 `conference`，目前页面上不显示，留着备用                    |
| `award`       | 可选，显示成黄色标签；没有就整行删掉                                    |
| `links`       | 可选，每个链接一个圆角按钮，`name` 随便起（DOI、PDF、arXiv、Slides…）     |

补充说明：

- 文件里论文的先后**不影响年份顺序**，页面会自动按年份从新到旧排。同一年里的几篇按文件里的先后显示。
- 标题旁的论文总数（"10 papers so far"）是自动统计的。
- 自动加粗靠的是 `_config.yml` 里的 `author_name: Zhuoxing Zhang`，作者列表里的写法必须和它一模一样。
- 想放 PDF 就把文件放进 `assets/papers/`（没有这个文件夹就新建），链接写 `/assets/papers/文件名.pdf`。

**印章颜色**已经配好的会议/期刊：SIGMOD 粉、VLDB 蓝、VLDBJ 紫、TKDE 黄、EAAI 绿、ADC 蜜桃色、PRICAI 橙。
新的会议默认是蓝色，想换颜色见 5.3。

### 3.6 Contact 明信片

- **邮箱**：改 `profile.yml` 里的 `email`，写正常地址就行。
  页面上会自动做防爬虫处理：网页源码里存的是倒过来的地址，浏览器打开后再还原。
  **不要**在别的地方手写邮箱地址，不然防爬虫就白做了。
- **地址那三行**：来自 `profile.yml` 的 `department`、`affiliation`、`location`。
- **"Hello there!" 和下面那段话**：在 `index.html` 里找 `postcard-body`。
  那段话里有很多 `&shy;`，这是"软连字符"，告诉浏览器"这个单词可以在这里断开并加连字符"，
  不需要断的时候看不见。明信片是整页最窄的一栏，靠它们才能两端对齐不留大空隙。
  改文字时，长单词最好也照样加上，例如 `col&shy;lab&shy;o&shy;ra&shy;tion`。
- **落款**（— Zhuoxing）会自动取 `name` 的第一个词。

### 3.7 头像和 CV

- **换头像**：把新图片（最好是正方形）放进 `images/`，然后改
  `profile.yml`：`photo: "/images/新文件名.jpg"`。
  写 `photo: ""` 会改成显示名字首字母。
- **挂 CV**：把 PDF 存成 `assets/cv.pdf`，然后改
  `profile.yml`：`cv: "/assets/cv.pdf"`。链接按钮最后会多出一个 CV。

---

## 4. 改外观：颜色、字体、小标题

所有样式都在 **`assets/css/site.css`** 这一个文件里。

### 4.1 颜色

文件最上面的 `:root { … }` 是全站的颜色"变量"，改这里全站一起变：

| 变量                                     | 管什么                               |
| ---------------------------------------- | ------------------------------------ |
| `--paper`                                | 页面底色（米黄色）                    |
| `--card`                                 | 卡片底色                             |
| `--text` / `--text-soft`                 | 正文颜色 / 次要文字颜色               |
| `--line` / `--shadow`                    | 所有描边 / 所有硬阴影                 |
| `--link`                                 | 链接颜色                             |
| `--night-top` / `--night`                | 页头和页脚的夜空渐变                  |
| `--yellow` `--pink` `--sky` `--mint` `--lilac` `--peach` | 那几种马卡龙色贴纸 |

紧接着的 `@media (prefers-color-scheme: dark) { :root { … } }` 是**暗色模式**的版本。
手机或电脑切到深色模式时会用这一组。改了浅色，记得看看暗色要不要一起改。

每个板块标题贴纸的颜色在这几行（搜 `.sec--about`）：

```css
.sec--about    { --c: var(--sky); }
.sec--research { --c: var(--yellow); }
.sec--news     { --c: var(--pink); }
.sec--papers   { --c: var(--mint); }
.sec--contact  { --c: var(--lilac); }
```

### 4.2 字体

标题用 **Fredoka**（圆润的那个），正文用 **Nunito**，都从 jsDelivr 加载。
这里特意没用 Google Fonts，因为国内访问不了。
加载字体的两行在 `_layouts/default.html`，字体名在 `site.css` 的 `--font-display` / `--font-body`。
如果 CDN 偶尔访问不到，页面会自动退回系统字体，不影响阅读。

### 4.3 板块旁边的小字、导航栏文字

- "nice to meet you"、"what keeps me busy"、"fresh off the press"、"say hello"：
  在 `index.html` 里搜 `sec-sub`。
- 导航栏里的文字在 `_includes/hero.html`。导航栏写的是 **Papers**，不是 Publications，
  这样 375px 宽的手机能一行放下全部五项。改长了手机上就得左右滑动。

---

## 5. 进阶：加板块、加图标、加会议颜色、换网站图标

### 5.1 加一个新板块（比如 Teaching）

1. `index.html`，照着已有的板块加一段：

   ```html
   <section id="teaching" class="sec sec--teaching">
     <div class="sec-head">
       <h2 class="sec-tag">Teaching</h2>
       <p class="sec-sub">in the classroom</p>
     </div>
     <div class="prose">
       <p>……</p>
     </div>
   </section>
   ```

2. `_includes/hero.html` 的导航列表里加一项：`<li><a href="#teaching">Teaching</a></li>`。
3. `site.css` 里给它一个颜色：`.sec--teaching { --c: var(--peach); }`。

注意：导航栏在手机上已经放满了，加第六项之后手机上需要左右滑动。滑动能正常用，当前板块也会自动滑到可见位置。

### 5.2 加一个新图标

图标都画在 `_includes/icon.html` 里，每个是一段 SVG。照着已有的格式加一个 `{%- when "名字" -%}` 分支：

- 画布用 `viewBox="0 0 48 48"`，线条用 `stroke="currentColor"`。
- 主体形状加 `class="i-a"`（会填成奶油白），点缀部分加 `class="i-b"`（会填成卡片颜色的深色版）。

加好以后，`profile.yml` 里写 `icon: 名字` 就能用。

### 5.3 给新会议配印章颜色

在 `site.css` 里搜 `.venue--sigmod`，照样加一行，名字是 `venue` 字段的**小写**：

```css
.venue--icde { --c: var(--peach); }
```

### 5.4 换网站图标（浏览器标签上的小月亮）

浏览器实际用的是 `images/favicon.svg`。旁边的 `favicon.ico` 和几个 PNG 是给老浏览器和手机桌面用的备份。
换图标时这些最好一起换：用任意"SVG 转 PNG/ICO"的工具，从新的 SVG 导出 16/32/48（ico）、32、180、192、512 这几个尺寸，文件名保持不变。

---

## 6. 发布之后怎么确认上线了

1. 推送后打开仓库的 **Actions** 标签页，会看到一条 **pages build and deployment**。
   - 黄色圆圈：正在构建，通常不到一分钟。
   - 绿色对勾：已经上线。
   - 红色叉：构建失败，**线上还是旧版本**，网站本身不会坏。点进去看报错，十有八九是 YAML 格式错了（见第 7 节）。
2. 上线了但页面看起来没变：GitHub Pages 会让浏览器缓存最多 10 分钟。
   电脑上按 `Ctrl + F5` 强制刷新；手机上可以等几分钟，或在地址后面加 `?1` 再打开。
3. 页脚的年份 "© 2026" 在每次构建时自动更新，新年第一次推送后就会变。

---

## 7. YAML 易错点

`_data/` 里的文件都是 YAML 格式，它对格式很挑剔：

- **缩进只能用空格，不能用 Tab**。同一层的内容要对齐。
- 长文字用 `>-`，下一行开始缩进着写。这样可以随便换行，里面的引号、冒号、`#` 都不用管：
  ```yaml
  detail: >-
    这里随便写 "引号"、冒号: 和 # 井号都没问题。
  ```
- 短文字里如果有 `: `（冒号加空格）或以特殊符号开头，就用双引号括起来：
  ```yaml
  greeting: "Hi, I'm Zhuoxing!"
  tagline: "Databases: my first love"
  ```
- 以 `#` 开头的行是注释，不会显示。
- 拿不准的时候，把内容粘到 <https://www.yamllint.com> 检查一下。

---

## 8. 出问题了怎么办

| 现象                                     | 多半是因为                          | 怎么办                                              |
| ---------------------------------------- | ----------------------------------- | --------------------------------------------------- |
| Actions 里是红叉                          | YAML 格式错误                        | 点进去看是哪个文件哪一行，对照第 7 节修改             |
| 推送了但网页没变                           | 浏览器缓存 / 还在构建                 | 看 Actions 是否绿了，然后强制刷新                     |
| 页面突然没有样式，变成白底黑字的普通网页      | CSS 文件被改名了                      | 见第 11 节第一条                                     |
| 某篇论文里我的名字没加粗                    | 作者列表里名字写法不一致               | 必须和 `_config.yml` 的 `author_name` 完全相同        |
| 新会议的印章是蓝色                          | 还没给它配颜色                        | 见 5.3                                              |
| 某段文字在手机上两端对齐后空隙很大            | 那一行的长单词挤不进去                 | 改一下措辞，或者在长单词里加 `&shy;`（见 3.6）         |
| 改坏了想回到之前的版本                      | —                                   | 在 GitHub 上打开文件点 **History**，找到之前的版本复制回来；或者用 `git revert` |

---

## 9. 本地预览（可选）

不预览也完全可以。如果想推送前先在自己电脑上看效果，需要先装 Ruby，然后在项目目录运行：

```bash
bundle install
```

```bash
bundle exec jekyll serve
```

打开 <http://localhost:4000>。改 `_data/` 和页面文件会自动刷新；改 `_config.yml` 需要停掉重新运行。

---

## 10. 文件结构

```
_config.yml             站点设置：标题、SEO 描述、自动加粗的名字
_data/profile.yml       个人信息、About、Research 卡片、链接、邮箱
_data/news.yml          新闻（清空则 News 板块自动隐藏）
_data/publications.yml  论文
index.html              页面主体：各板块的结构、明信片文字、小标题
_layouts/default.html   页面外壳：字体加载、页脚、几段小脚本
_includes/hero.html     夜空页头 + 导航栏
_includes/icon.html     手绘小图标（研究卡片、月亮、邮票……）
_includes/email.html    防爬虫的邮箱链接
assets/css/site.css     全部样式，颜色变量在最上面
assets/css/style.scss   占位文件，不要删（见第 11 节）
images/                 头像、网站图标
_portfolio/             暂时没用：2025 年南岛自驾相册，没有挂到主页上（图片在 images/nz/）
Gemfile                 只给本地预览用，GitHub 不看它
```

---

## 11. 几条不要动的规矩

1. **样式文件必须叫 `site.css`，不能改名成 `style.css`，`assets/css/style.scss` 也不要删。**
   `_config.yml` 没有指定主题，GitHub Pages 就会默认套一个叫 jekyll-theme-primer 的主题。
   这个主题自带的样式正好会生成 `style.css`，会把我们的样式悄悄盖掉。
   `style.scss` 是用来挡住它的。
2. **不要在页面其他地方手写邮箱**，统一由 `profile.yml` 的 `email` 生成（见 3.6）。
3. **`_config.yml` 里的 `lang: en` 不要删**。浏览器要靠它知道是英文，才会给单词自动断词，两端对齐才不会出现大空隙。
4. **正文的两端对齐是刻意的**。别给正文加 `text-wrap: pretty`，实测反而会让空隙变大。

---

用到的开源资源：字体 [Fredoka](https://fonts.google.com/specimen/Fredoka) 和
[Nunito](https://fonts.google.com/specimen/Nunito)（SIL Open Font License），
通过 [jsDelivr](https://www.jsdelivr.com) 上的 [Fontsource](https://fontsource.org) 加载。
