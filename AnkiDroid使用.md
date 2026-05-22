
## 安装

- 更新软件源，安装必要依赖

  ```bash
  sudo apt update
  sudo apt install libxcb-xinerama0 libxcb-cursor0 libnss3 libxcb-icccm4 libxcb-keysyms1 zstd
  ```
- 软件下载，下载[地址](https://apps.ankiweb.net)

- 解压安装

  ```bash
  tar xaf Downloads/anki-launcher-25.09-linux.tar.zst
  cd Downloads/anki-launcher-25.09-linux/; bash install.sh
  ```

- 启动  

  ```bash
  anki
  ```

  启动后会提示更新.

## 使用




## 附录

### 参考资料

- [Anki app](https://apps.ankiweb.net/)
- [Anki web](https://ankiweb.net/decks)
- [Anki github](https://github.com/ankitects/anki)


### AI

#### 介绍

› https://ankiweb.net/decks

  介绍一下这个工具的主要概念

• 如果你指的是 https://ankiweb.net/decks 这个页面，它本质上是 AnkiWeb 的“共享牌组”入口：用来搜索、下载别人公开分享的 Anki 牌组，然后导入到 Anki 里学习。Anki
  本身是一个基于“间隔重复”的记忆工具。

  核心概念

  - Anki：一款闪卡记忆软件。你看到问题、回忆答案、点“显示答案”，然后根据自己记得好不好选择反馈，Anki 会决定下次什么时候再让你复习这张卡。
  - AnkiWeb：Anki 的在线服务，主要用于账号同步、备份、跨设备同步，以及浏览/分享公开牌组。
  - Shared Decks / 共享牌组：别人做好的牌组集合，比如语言词汇、医学知识、考试题库、国家首都等。你可以从 AnkiWeb 下载后导入 Anki。
  - Deck / 牌组：一组卡片的容器。比如“英语单词”“日语 N2”“医学解剖”。牌组可以有子牌组，例如 Chinese::Hanzi 表示 “Chinese” 下的 “Hanzi” 子牌组。
  - Card / 卡片：真正被复习的单位，通常是一问一答。比如正面是“oxygen 的化学符号？”，背面是 “O”。
  - Note / 笔记：生成卡片的原始数据。一条笔记可以生成一张或多张卡片。例如一条“bonjour = hello”的笔记，可以生成“法语 → 英语”和“英语 → 法语”两张卡。
  - Field / 字段：笔记里的数据格子。比如语言学习中可以有 French、English、Page、Audio 等字段。
  - Note Type / 笔记类型：定义一类笔记有哪些字段、会生成什么卡片。常见类型包括 Basic、Basic and reversed、Cloze、Image Occlusion。
  - Card Template / 卡片模板：决定字段如何显示在卡片正面和背面。比如 {{French}} 会被替换成笔记里 French 字段的实际内容。
  - Review / 复习调度：Anki 根据你的反馈安排复习间隔。卡片状态大致包括新卡、学习中、复习中、重新学习等。

  共享牌组怎么用

  通常流程是：

  1. 在 Anki 桌面版、AnkiMobile 或 AnkiDroid 中打开共享牌组列表，或访问 AnkiWeb 共享牌组页面。
  2. 选择分类或搜索关键词。
  3. 打开感兴趣的牌组页面。
  4. 下载 .apkg 牌组包。
  5. 用 Anki 导入。
  6. 开始学习，并通过同步把它上传到你的 AnkiWeb 账号。

  注意：官方手册说明，不能直接把共享牌组“添加到 AnkiWeb 账号”里；需要先导入到桌面版、AnkiMobile 或 AnkiDroid，再同步到 AnkiWeb。

  使用时的几个重点

  - 共享牌组适合快速开始，但不一定适合深度学习复杂主题。
  - 对复杂学科，最好把共享牌组当作补充材料，而不是替代教材、课程或自己的理解。
  - 自己制作牌组通常学习效果更好，因为制作过程会迫使你判断什么是重点。
  - 如果下载别人的牌组，最好检查内容质量、更新时间、评分、评论和版权情况。
  - 重新导入更新版共享牌组时，通常不会自动像云文档那样实时更新，需要你手动重新下载/导入。

  参考资料：

  - Anki 官方手册：Getting Started / Key Concepts / Shared Decks：https://docs.ankiweb.net/getting-started.html (https://docs.ankiweb.net/getting-started.html)
  - AnkiMobile 手册：Shared Decks：https://docs.ankimobile.net/shared-decks.html (https://docs.ankimobile.net/shared-decks.html)
  - Anki 手册：Sharing Decks Publicly / Privately：https://docs.ankiweb.net/contrib.html (https://docs.ankiweb.net/contrib.html)

#### 安装

› ubuntu 如何安装桌面版

• 可以，Ubuntu 上建议安装 Anki 官方桌面版，不太建议直接用 Ubuntu 软件源里的旧版 anki，因为可能版本落后或同步/插件兼容有问题。

  推荐安装方式：官方包

  先安装依赖：

  sudo apt update
  sudo apt install libxcb-xinerama0 libxcb-cursor0 libnss3 libxcb-icccm4 libxcb-keysyms1 zstd

  然后去官方下载页面：

  https://apps.ankiweb.net

  下载 Linux 版本，文件名大概类似：

  anki-launcher-2xxx-linux.tar.zst

  假设你下载到了 ~/Downloads，执行：

  cd ~
  tar xaf Downloads/anki-launcher-*-linux.tar.zst
  cd anki-launcher-*-linux
  sudo ./install.sh

  安装完成后，可以在终端启动：

  anki

  也可以在 Ubuntu 应用菜单里搜索 Anki 打开。

  如果 tar 解压失败

  有些系统需要这样解压：

  tar xaf Downloads/anki-launcher-*-linux.tar.zst --use-compress-program=unzstd

  或者确认安装了：

  sudo apt install zstd

  升级 Anki

  以后升级也很简单：

  1. 重新从 https://apps.ankiweb.net 下载新版 Linux 包；
  2. 解压；
  3. 再运行：

  sudo ./install.sh

  你的牌组和学习进度不会因为重新安装而丢失，用户数据通常保存在用户目录里。

  卸载旧版

  如果你之前用 apt 安装过 Anki，建议先卸载：

  sudo apt remove anki

  然后再安装官方版。

  官方说明参考：
  https://docs.ankiweb.net/platform/linux/installing.html (https://docs.ankiweb.net/platform/linux/installing.html)

#### 生成牌组

  从零制作一个牌组再导出

  基本流程是：

  创建牌组 → 添加笔记/卡片 → 检查内容 → 导出为 .apkg

  例如做一个英语单词牌组：

  1. 点击 Anki 主界面的 创建牌组。
  2. 输入牌组名，比如：

  English Vocabulary

  3. 点击 添加。
  4. 选择笔记类型，比如：

  Basic

  5. 选择目标牌组：

  English Vocabulary

  6. 填写正面和背面：

  Front: apple
  Back: 苹果；苹果公司

  7. 点击 添加。
  8. 添加多张卡之后，用 文件 → 导出 导出为 .apkg。

  批量制作：用 CSV / TSV 导入

  如果你已经有表格数据，比如：

  apple,苹果
  banana,香蕉
  orange,橙子

  可以保存成 .csv 或 .txt，然后：

  1. Anki 中点击：

  文件 → 导入

  2. 选择 CSV / TXT 文件。
  3. 设置字段分隔符，例如逗号、Tab。
  4. 设置每一列对应到哪个字段，例如：
      - 第一列 → Front
      - 第二列 → Back
  5. 导入后检查卡片。
  6. 再通过 文件 → 导出 导出为 .apkg。

  更推荐用 Tab 分隔，避免英文释义里的逗号导致错列，例如：

  apple 苹果
  banana        香蕉
  orange        橙子

  用 Python 自动生成 .apkg

  如果你想程序化生成牌组，可以用 Python 库 genanki。

  安装：

  pip install genanki

  示例：

  import genanki

  model = genanki.Model(
      1607392319,
      'Simple Model',
      fields=[
          {'name': 'Question'},
          {'name': 'Answer'},
      ],
      templates=[
          {
              'name': 'Card 1',
              'qfmt': '{{Question}}',
              'afmt': '{{FrontSide}}<hr id="answer">{{Answer}}',
          },
      ],
  )

  deck = genanki.Deck(
      2059400110,
      'My First Deck'
  )

  note = genanki.Note(
      model=model,
      fields=['apple', '苹果']
  )

  deck.add_note(note)

  genanki.Package(deck).write_to_file('my_deck.apkg')

  运行后会生成：

  my_deck.apkg

  然后可以在 Anki 中导入它。

  什么时候用哪种方式

  - 少量卡片：直接在 Anki 里添加，然后导出。
  - 已经有表格/词表：CSV / TSV 导入，再导出。
  - 想自动生成大量卡片：用 Python genanki。
  - 想带图片/音频：Anki 手动制作或 genanki 添加媒体文件。

  简单总结：

  手动制作牌组 → 文件 → 导出 → Anki 牌组包 (*.apkg)

  或者：

  数据表 / Python 脚本 → 生成卡片 → 导出 .apkg

#### 卡片类型

› 这个牌组，只能是 正面、反面么？


• 不是，Anki 的牌组不只能是“正面/反面”。

  “正面/反面”只是最基础的卡片形式。Anki 真正的核心是：

  笔记 Note → 字段 Fields → 卡片模板 Card Templates → 生成卡片 Cards

  也就是说，一条资料可以有很多字段，也可以生成多张不同形式的卡片。

  1. 最基础：正面 / 反面

  默认的 Basic 类型就是：

  Front: apple
  Back: 苹果

  生成一张卡：

  正面：apple
  反面：苹果

  2. 可以有多个字段

  比如你学英语单词，可以设计成：

  单词：apple
  音标：/ˈæpəl/
  释义：苹果
  例句：I eat an apple every day.
  发音：音频文件
  图片：苹果图片
  备注：常见水果名词

  这些都可以是字段。

  然后卡片正面可以显示：

  {{单词}}
  {{音标}}

  背面显示：

  {{释义}}
  {{例句}}
  {{发音}}
  {{图片}}
  {{备注}}

  所以不是只能两个字段。

  3. 一条笔记可以生成多张卡

  比如一条笔记：

  English: apple
  Chinese: 苹果
  Example: I ate an apple.

  可以生成两张卡：

  第一张：

  正面：apple
  背面：苹果

  第二张：

  正面：苹果
  背面：apple

  这就是双向卡片。

  还可以生成：

  正面：I ate an ____.
  背面：apple

  也就是说，一条数据可以从多个角度考你。

  4. 常见笔记类型

  Anki 自带几种常见类型：

  - Basic：基础问答，一张正面、一张反面。
  - Basic and reversed card：基础 + 反向卡，比如英文到中文、中文到英文。
  - Basic optional reversed card：可选反向卡。
  - Cloze：填空题，比如“巴黎是法国的首都”变成“巴黎是 {{c1::法国}} 的首都”。
  - Image Occlusion：图片遮挡题，常用于医学、地图、结构图学习。

  5. 例子：医学卡片

  一条笔记可以这样：

  名称：心脏
  位置：胸腔中部偏左
  功能：泵血
  图片：heart.png
  临床意义：心衰、心律失常等

  可以生成卡片：

  卡片 1：这个器官叫什么？
  卡片 2：心脏的位置在哪里？
  卡片 3：心脏的主要功能是什么？
  卡片 4：看图识别结构

  6. 例子：编程知识卡片

  字段：

  概念：闭包
  定义：函数捕获其外部作用域变量的能力
  语言：JavaScript / Python
  示例代码：...
  易错点：变量绑定时机

  卡片可以是：

  正面：什么是闭包？
  背面：定义 + 示例

  正面：下面代码输出什么？
  背面：解释原因

  正面：闭包常见用途？
  背面：状态封装、回调、装饰器等

  一句话总结

  Anki 不是简单的“正面/反面卡片工具”，而是：

  多字段笔记 + 卡片模板 + 间隔重复系统

  你可以做：

  - 问答题
  - 双向翻译
  - 填空题
  - 图片遮挡题
  - 听音辨义
  - 看图识别
  - 多字段知识卡
  - 一条笔记生成多张卡片

  所以 .apkg 牌组可以非常复杂，不只是正面和反面。


