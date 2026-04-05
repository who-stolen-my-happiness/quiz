大气物理学刷题 Demo（修正版）

文件说明
1. 直接双击 index.html，即可在电脑浏览器里使用。
2. quiz_data.js 是题库数据文件。
3. images 文件夹里是部分图形题/原题页截图，index.html 会自动调用，所以不要单独删掉这个文件夹。

这次修改了什么
1. 重新整理了 290 道选择题的数据，修复了大量题干、选项、答案错位问题。
2. 提交后直接判分，不再弹出二次确认。
3. 增加了“上一题”按钮，可以回退。
4. 支持多选题（例如第 173 题）。
5. 对部分图形题增加了“查看该题所在页原图”。
6. 修正了一个明显的题答案不匹配问题：第 127 题在原答案页与题面不一致，已按题面可见选项修正为 C。

如何上传到 GitHub 并部署
方法一：最简单，使用 GitHub Pages

一、准备
1. 注册并登录 GitHub。
2. 在电脑安装 Git（可选，但推荐）。
3. 把当前整个 atmos_quiz_demo_fixed 文件夹保留完整。

二、创建仓库
1. 打开 GitHub 首页。
2. 点击右上角 New repository。
3. 仓库名建议填：atmos-quiz-demo
4. 选择 Public。
5. 点击 Create repository。

三、上传文件
方法 A：网页直接上传
1. 进入你刚创建的仓库。
2. 点击 Add file -> Upload files。
3. 把以下内容一起拖进去：
   - index.html
   - quiz_data.js
   - images 文件夹里的全部图片
4. 点击 Commit changes。

方法 B：用 Git 命令上传
在本地项目文件夹打开终端，依次执行：

git init
git branch -M main
git add .
git commit -m "init atmos quiz demo"
git remote add origin 你的仓库地址
git push -u origin main

例如仓库地址通常像：
https://github.com/你的用户名/atmos-quiz-demo.git

四、开启 GitHub Pages
1. 打开仓库页面。
2. 点击 Settings。
3. 左侧找到 Pages。
4. 在 Build and deployment 里：
   - Source 选择 Deploy from a branch
   - Branch 选择 main
   - Folder 选择 /root
5. 点击 Save。

五、获取网页链接
等几十秒到几分钟后，GitHub 会生成一个访问地址，通常格式是：
https://你的用户名.github.io/atmos-quiz-demo/

之后你就可以在电脑、手机、iPad 浏览器里直接打开。

使用时注意
1. images 文件夹必须和 index.html 放在同一级目录下。
2. 如果你以后修改题库，只要重新上传 index.html、quiz_data.js 和 images 文件夹即可。
3. 浏览器会缓存旧版本，如果更新后没变化，强制刷新即可：
   - Windows: Ctrl + F5
   - Mac: Command + Shift + R

如果你想继续升级，可以再做这些功能
1. 收藏题目
2. 章节筛选
3. 计时模式
4. 自动统计每类题正确率
5. 导出错题本
