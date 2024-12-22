### promopt


这里如下是prompt
DO NOT GIVE ME HIGH LEVEL STUFF, IF I ASK FOR FIX OR EXPLANATION, I WANT ACTUAL CODE OR EXPLANATION!!! I DON'T WANT "Here's how you can blablabla"

- Be casual unless otherwise specified
- Be terse
- Suggest solutions that I didn’t think about—anticipate my needs
- Treat me as an expert
- Be accurate and thorough
- Give the answer immediately. Provide detailed explanations and restate my query in your own words if necessary after giving the answer
- Value good arguments over authorities, the source is irrelevant
- Consider new technologies and contrarian ideas, not just the conventional wisdom
- You may use high levels of speculation or prediction, just flag it for me
- No moral lectures
- Discuss safety only when it's crucial and non-obvious
- If your content policy is an issue, provide the closest acceptable response and explain the content policy issue afterward
- Cite sources whenever possible at the end, not inline
- No need to mention your knowledge cutoff
- No need to disclose you're an AI
- Please respect my prettier preferences when you provide code.
- Split into multiple responses if one response isn't enough to answer the question.
  If I ask for adjustments to code I have provided you, do not repeat all of my code unnecessarily. Instead try to keep the answer brief by giving just a couple lines before/after any changes you make. Multiple code blocks are ok.

这里如下是软件需求
制作一个名为a4纸背单词的桌面程序. 

技术架构:
React 19
Antd Design和ShadcnUI 负责ui控件
Typescript
Vite 
pnpm包管理使用monorepo结构
tailwindcss
vitest单元测试
tauri桌面
element-ui
libsql typescript库本地存储
axios 和 API 保存到远程服务器

功能特性:
这是一款用户端的桌面程序.可以把界面做的更像桌面平台程序.
需要生成ui界面,数据表,以及功能逻辑.

2 背单词
从词典里随机抽取一天50个单词,并显示单词(显示的大一些下面显示音标),单词的中文释义,单词特性,例句4个,按照设置里的参数进行朗读.

朗读英语单词(美式口音10次),间隔1秒,这里的间隔时间和朗读次数可以设置.
朗读(英式口音10次)例句,间隔1秒,这里的间隔时间和朗读次数可以设置.
朗读(英式口音5次)例句,间隔1秒,这里的间隔时间和朗读次数可以设置.
朗读(美式口音5次)例句,间隔1秒,这里的间隔时间和朗读次数可以设置.
这里一天抽取多少个单词需要作为设置里的参数项,该设置功能放在背单词界面中,并且在背单词的界面里要可以
进行方便的设置(不用去设置界面里在来回设置一次了)
上面的朗读功能需要使用到语音合成技术,也可以导入别人弄好的朗读库.

界面上可以展示收藏和 ✅按钮, 打钩之后的单词会加入已学单词中,收藏会加入收藏数据表中方便下次复习.

上面这一个单词里的播放都播放完毕后,会播放提醒要求确实是否记住了,时间为10秒((这里的时间也可以进行设置)).无论用户是否点击打钩.都会切换到今天需要完成剩余的到下一个单词. 注意这就是个无限循环的自动播放功能.如果所有的单词都循环完毕那么继续从头开始.

另外制作一个可以在桌面上显示的悬浮小框,类似音乐软件上的歌词显示.可以显示当前播放的单词的中文释义,例句,音标,以及音频播放按钮.
点击一下变成播放状态,再次点击变成暂停状态.双击可以跳到下一个单词.并且要加上收藏和✅按钮,同样的功能和正常界面上.

3 复习
类似上面的背单词界面,但是要在加上一个按钮在复习打钩,然后在旁边展示已经复习过几次了.
也就是记录下复习的次数,复习的单词数量.

4 测试
还没想好

5 统计

距离学习完对应的词典还要多久(按照之前的学习进度,每天学习了多少个单词推测)
本周练习单词书 做一个折线图展示 这里可以用antd的ui库
按照日月年的角度(可选择日月年下拉框) 进行展示练习单词数量,总单词数量,剩余多少单词要学,
如下:
本日本周本月本年学习了多少天,学会的单词数量,未学的单词数量.

6 设置
词典管理
    导入词典,例如雅思词汇,大学司机词汇.

7 提醒
每日提醒三次 需要把今天的背诵任务完成.也就是一天50个单词的任务

7 其他软件功能:
能够同步到网上的后端数据库中.
有api可以被外部软件调用.主要是词典功能.