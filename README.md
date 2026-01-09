# Ai4City 新网站 v1.02.0104 版本使用手册  
## 维护方法
1. **代码编辑**：使用任何文本编辑器（如VSCode、Sublime Text等）打开并编辑`index.html`文件。
2. **样式调整**：目前网站使用不标准的Tailwind CSS框架，样式配置存放在html文件中，集中在"**// 3. UI 组件，页面样式**"这个部分，几乎不用动。
3. **内容更新**：网站内容主要存储在`index.html`文件中的"**// 1. 数据层**"部分。可以直接在该文件中修改和添加新闻、研究方向、团队成员等内容。
   - **大标题上的seminar及其详情页面内容**：在`ARTICLE_CONTENT`数组中添加或修改研讨会第一条“seminar”，这个id是专用于大标题上面的seminar及其详情页面的。
   - **新闻**：在`NEWS_ITEMS`数组中添加新闻条目，直接引用`ARTICLE_CONTENT`里面的对象名称（如'seminar'、'Zhouseminar'等）。
   - **研究方向**：在`RESEARCH_AREAS`数组中更新研究方向信息，不过这里几乎不用改。
   - **团队成员**：在`TEAM_MEMBERS`数组中管理PI和学生的信息。在人员去留的时候增添新的数组就行了，其它几乎不用改.
4. **图片和资源管理**：所有静态资源（如图片、图标等）存放在`image/`文件夹中。根据需要添加、删除或替换这些资源。
5. **本地预览**：可以使用本地服务器（如Live Server插件）在浏览器中预览网站效果，确保所有修改正确显示。

## 主要样式代码位置
- `index.html`: 该文件包含了网站的整体结构和内容。主要部分包括：
  - 头部导航栏：包含网站Logo和导航链接。（const Navbar = ... ...）
  - 首页：展示实验室简介、最新新闻、研究方向、团队成员等内容。（const HomePage = ... ...）
  - 新闻页面：动态生成新闻列表和详情页。包含在首页中。（{/* 这是新的News的容器，下滑表单 */}） 
  - 研究页面，出版物页面，资源页面：（const ListPage = ({ title, description, items, type = "default" })... ...）
  - 团队页面：展示团队成员信息，包括PI和学生。 （const TeamPage = ()... ...）
  - 页脚：包含版权信息和社交媒体链接。 （const Footer = ... ...）

## 文件结构  
### 1.资源
- `version.md`: 版本记录文件。
- `README.md`: 本文件，网站使用手册。
- `3drebuild.mp4`: 首页的演示视频。
- `tailwind.config.js`: Tailwind CSS 配置文件。
- `index.html`: 网站主HTML文件，包含网站的整体结构和内容。
- `geindex.html`：gemini生成的网站样式，个人觉得比较美观
- `image/`: 存放静态资源文件，如图片、图标等。以下分门别类存放：
  - `frontPage/`: 首页相关图片。
  - `news/`: 新闻相关图片。
  - `team/`: 团队成员照片。
  - `research/`: 研究相关图片。
  - `publications/`: 出版物相关图片。
  - `resources/`: 资源相关图片。
  - `seminar/`: 研讨会相关图片。

