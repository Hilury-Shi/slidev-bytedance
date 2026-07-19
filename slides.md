---
theme: ./theme
layout: cover
highlighter: shiki
lineNumbers: false
themeConfig:
  primary: '#325AB4'
transition: slide-left
title: 从各自为战到参谋部
---

# 从各自为战到参谋部

我们为什么要做这个 Agent，以及它接下来要长成什么样

技术团队 · 内部分享

2026.07

<!--
讲者备注：
- 这是一份面向各部门负责人的分享，不是纯技术分享。
- 主线：公司现在像"没有参谋部的军队"，我们要做的 Agent 就是那个"参谋部"。
- 全程用一个场景串起来：部门 A 和部门 B 协同失败。
-->

---
layout: center
---

<div class="text-left max-w-4xl mx-auto">

# 今天想讲清楚 7 个问题

<div class="mt-6 space-y-3 text-xl leading-relaxed">

<div><span class="text-primary font-bold text-2xl mr-3">1</span> 跨部门协同，到底付出了多大的代价？</div>
<div><span class="text-primary font-bold text-2xl mr-3">2</span> 为什么大家都很努力，却总在<b>各自为战</b>？</div>
<div><span class="text-primary font-bold text-2xl mr-3">3</span> 军队的<b>参谋部</b>，给了我们什么启发？</div>
<div><span class="text-primary font-bold text-2xl mr-3">4</span> 技术侧，其实撞上了<b>同一堵墙</b>？</div>
<div><span class="text-primary font-bold text-2xl mr-3">5</span> 这件事我们<b>已经做了什么</b>？</div>
<div><span class="text-primary font-bold text-2xl mr-3">6</span> 下一步的<b>三件事</b>是什么？</div>
<div><span class="text-primary font-bold text-2xl mr-3">7</span> 如果它长大了，<b>能走多远</b>？</div>

</div>
</div>

---
layout: section
---

# 01 / 协同的代价有多大？

先说说那个我们都遇到过的场景

---

# 一个我们都眼熟的场景

<div class="grid grid-cols-2 gap-8 mt-8">

<div class="border border-gray-300 rounded-lg p-5">
<h3 class="text-primary">部门 A</h3>
<ul class="mt-3 space-y-2">
<li>接到需求，闷头开工</li>
<li>按<b>自己的理解</b>定方案</li>
<li>做到一半，默认 B 会配合</li>
</ul>
</div>

<div class="border border-gray-300 rounded-lg p-5">
<h3 class="text-primary">部门 B</h3>
<ul class="mt-3 space-y-2">
<li>同一时间，也在闷头开工</li>
<li>按<b>另一套理解</b>定方案</li>
<li>并不知道 A 已经依赖了自己</li>
</ul>
</div>

</div>

<div class="mt-8 text-center text-xl">
两条线各自跑得飞快 —— 直到<span class="text-primary font-bold">要对接的那一刻</span>，才发现对不上。
</div>

<!--
讲者备注：这里不点名，用"部门 A / B"泛指。让每个负责人都能对号入座。
-->

---
layout: two-cols
---

# 然后呢？

对不上之后，通常是这样收场：

<v-clicks>

- 临时拉一个<b>协调会</b>
- 各自解释"我当时以为……"
- 谁改动小，谁就"迁就"一下
- 排期顺延，交付延后
- 下次需求，<b>循环再来一遍</b>

</v-clicks>

::right::

<div class="pl-6 mt-16">

<div class="border-l-4 border-primary pl-4 py-2 mb-4">
<div class="text-sm opacity-60">典型一次返工</div>
<div class="text-3xl font-bold text-primary">【填真实数字】</div>
<div class="text-sm opacity-60">例如：延期 2 周 / 开了 5 次协调会</div>
</div>

<div class="border-l-4 border-primary pl-4 py-2">
<div class="text-sm opacity-60">近半年类似情况</div>
<div class="text-3xl font-bold text-primary">【填真实次数】</div>
<div class="text-sm opacity-60">例如：X 个项目受影响</div>
</div>

</div>

<!--
讲者备注：括号里的数字，分享前用真实（可匿名化）案例替换。
一个真实数字，比十句"沟通不畅"更有说服力。
-->

---
layout: statement
---

# 问题不在"谁不努力"

<div class="text-2xl mt-4 opacity-80">大家都很拼，代价却依然发生</div>

---
layout: section
---

# 02 / 为什么总是各自为战？

---
layout: quote
---

# "几乎所有大公司，CEO 都是光杆司令"

—— 雷军，谈组织与参谋部

---

# 这不是态度问题，是结构问题

<div class="mt-6 space-y-5 text-xl">

<div class="flex items-start gap-4">
<div class="text-primary font-bold">缺口 1</div>
<div>没有一个地方，能让 A 和 B <b>同时看到全局战场</b> —— 各自只看到自己那一块。</div>
</div>

<div class="flex items-start gap-4">
<div class="text-primary font-bold">缺口 2</div>
<div>信息靠<b>临时开会</b>传递 —— 慢、易失真、开完就散、无沉淀。</div>
</div>

<div class="flex items-start gap-4">
<div class="text-primary font-bold">缺口 3</div>
<div>依赖关系<b>没人统一盯</b> —— 出了问题才发现，只能事后补救。</div>
</div>

</div>

<div class="mt-8 text-center text-xl">
军队几万人也会遇到这个问题。他们的解法，叫<span class="text-primary font-bold">参谋部</span>。
</div>

---
layout: section
---

# 03 / 参谋部给了我们什么启发？

---

# 参谋部到底是干什么的

<div class="mt-4 text-lg opacity-70">它不是"幕僚"，而是司令部里最核心的指挥机构</div>

<div class="grid grid-cols-2 gap-5 mt-8">

<div class="border border-gray-300 rounded-lg p-5">
<h4 class="text-primary">① 搜集情况</h4>
<div class="mt-2 opacity-80">摸清敌我双方的真实状态，而不是靠猜</div>
</div>

<div class="border border-gray-300 rounded-lg p-5">
<h4 class="text-primary">② 拟定计划</h4>
<div class="mt-2 opacity-80">把指挥员的意图，变成可执行的作战方案</div>
</div>

<div class="border border-gray-300 rounded-lg p-5">
<h4 class="text-primary">③ 传达命令</h4>
<div class="mt-2 opacity-80">统一下达，并<b>督促执行、检查落实</b></div>
</div>

<div class="border border-gray-300 rounded-lg p-5">
<h4 class="text-primary">④ 协调保障</h4>
<div class="mt-2 opacity-80">横向拉通各兵种，让大家<b>朝一个方向使劲</b></div>
</div>

</div>

<div class="mt-6 text-center text-lg">
一句话：<span class="text-primary font-bold">让指挥员不再是"光杆司令"，让全军看到同一张地图。</span>
</div>

---

# 把参谋部，翻译成我们的语言

<div class="grid grid-cols-2 gap-x-6 gap-y-3 mt-8">
  <div class="text-center text-sm opacity-60 font-bold">军队 · 参谋部</div>
  <div class="text-center text-sm text-primary font-bold">公司 · Agent 参谋部</div>

  <div class="border border-gray-300 rounded-lg p-3 text-center">搜集情况</div>
  <div class="border border-primary rounded-lg p-3 text-center text-primary">知识库检索 · 统一数据事实</div>

  <div class="border border-gray-300 rounded-lg p-3 text-center">拟定作战计划</div>
  <div class="border border-primary rounded-lg p-3 text-center text-primary">工具化查询 · 直接给建议</div>

  <div class="border border-gray-300 rounded-lg p-3 text-center">传令 / 督办</div>
  <div class="border border-primary rounded-lg p-3 text-center text-primary">跨部门可见 · 状态透明</div>

  <div class="border border-gray-300 rounded-lg p-3 text-center">协调各兵种</div>
  <div class="border border-primary rounded-lg p-3 text-center text-primary">权限围栏 · 各就各位</div>
</div>

<div class="mt-6 text-center text-xl">
我们要做的 Agent，本质就是给公司装一个<span class="text-primary font-bold">"参谋部"</span>。
</div>

---
layout: section
---

# 04 / 技术侧，撞上了同一堵墙

---
layout: two-cols
---

# 今天的"参谋"，是工程师

只要涉及跨部门的数据和分析：

<v-clicks>

- 要一份数据 → <b>提需求给技术</b>
- 技术<b>手动写查询</b>、从库里抠数据
- 再<b>专门写一个前端页面</b>展示
- 想换个维度看 → <b>再排一次期</b>
- 高峰期，大家<b>排队等技术</b>

</v-clicks>

::right::

<div class="pl-6 mt-14">

<div class="border border-gray-300 rounded-lg p-6 text-center">
<div class="text-lg opacity-70">所有分析需求</div>
<div class="text-5xl my-4">⬇</div>
<div class="text-2xl font-bold text-primary">技术团队</div>
<div class="text-5xl my-4">⬇</div>
<div class="text-lg opacity-70">各部门</div>
<div class="mt-4 text-primary font-bold">单点瓶颈</div>
</div>

</div>

---
layout: statement
---

# 同一个问题，换了个位置

<div class="text-2xl mt-4 opacity-80">业务侧缺参谋部，技术侧成了那个"光杆参谋"</div>

---
layout: section
---

# 补充 / 先统一几个词

进入正题前，用一个生活场景讲明白 4 个关键词

---

# 一个场景，一层层加能力

<div class="mt-4 text-lg opacity-70">"帮我安排周末去杭州玩" —— AI 是怎么从聊天变成能干活的</div>

<div class="mt-6 space-y-3 text-lg">

<div class="flex gap-4"><div class="text-primary font-bold w-40 flex-shrink-0">大模型 LLM</div><div>你问一句，它答一句 —— 但答得浅</div></div>
<div class="flex gap-4"><div class="text-primary font-bold w-40 flex-shrink-0">提示词 / 上下文</div><div>把话说清楚、把前文一起带上，答得更准</div></div>
<div class="flex gap-4"><div class="text-primary font-bold w-40 flex-shrink-0">记忆 Memory</div><div>对话太长会忘，于是压缩成"记忆"留住重点</div></div>
<div class="flex gap-4"><div class="text-primary font-bold w-40 flex-shrink-0">检索 RAG</div><div>读你的私有资料再回答，不靠瞎编</div></div>
<div class="flex gap-4"><div class="text-primary font-bold w-40 flex-shrink-0">工具调用</div><div>不只是"告诉你怎么做"，而是真的去查、去做</div></div>

</div>

<div class="mt-6 text-center text-lg opacity-80">
每一个词，都是<b>上一步遇到了问题</b>才冒出来的解法。
</div>

---

# 后面要反复用到的 4 个词

<div class="grid grid-cols-2 gap-5 mt-8">

<div class="border border-gray-300 rounded-lg p-5">
<h3 class="text-primary">Agent（智能体）</h3>
<div class="mt-2 opacity-80">接到目标，自己规划、自己调工具、自己记录 —— 一个能<b>独立干活</b>的系统</div>
</div>

<div class="border border-gray-300 rounded-lg p-5">
<h3 class="text-primary">MCP（统一工具接口）</h3>
<div class="mt-2 opacity-80">让所有工具遵循<b>同一种接法</b>，接一次，处处能用，不必逐个改代码</div>
</div>

<div class="border border-gray-300 rounded-lg p-5">
<h3 class="text-primary">Skill（技能）</h3>
<div class="mt-2 opacity-80">把规则和经验写成<b>可复用</b>的文件，而不是每次现场口述</div>
</div>

<div class="border border-gray-300 rounded-lg p-5">
<h3 class="text-primary">Harness（约束/围栏）</h3>
<div class="mt-2 opacity-80">给 Agent <b>划边界、定红线、自动验收</b>，让它在可控范围内爆发生产力</div>
</div>

</div>

<div class="mt-6 text-center text-lg">
接下来说的"已经做了什么"和"下一步三件事"，其实就是这 <span class="text-primary font-bold">4 个词</span>。
</div>

---
layout: section
---

# 05 / 我们已经做了什么？

它不是概念，是已经在跑的系统

---

# 我们的 Agent，就是那个定义的落地

<div class="mt-4 text-lg opacity-70">"接到目标 → 自己规划 → 自己调工具 → 自己记录结果"</div>

<div class="mt-6 flex flex-col items-center gap-1">
  <div class="border border-gray-300 rounded-lg px-6 py-1.5">用户提问</div>
  <div class="text-xl text-primary leading-none">↓</div>
  <div class="border-2 border-primary rounded-lg px-8 py-1.5 text-primary font-bold">对话引擎（调度中枢）</div>
  <div class="text-xl text-primary leading-none">↓</div>
  <div class="grid grid-cols-4 gap-3 w-full text-center text-sm">
    <div class="border border-gray-300 rounded-lg p-2">工具箱<br/>专业/学校/志愿/分数线</div>
    <div class="border border-gray-300 rounded-lg p-2">结构化追问<br/>缺信息就反问</div>
    <div class="border border-gray-300 rounded-lg p-2">长对话记忆<br/>自动压缩</div>
    <div class="border border-gray-300 rounded-lg p-2">额度<br/>预扣 / 退还</div>
  </div>
  <div class="text-xl text-primary leading-none">↓</div>
  <div class="border border-gray-300 rounded-lg px-6 py-1.5">带依据的回答</div>
</div>

<div class="mt-4 text-center text-lg">
面向 C 端的"<span class="text-primary font-bold">潇湘单招 AI 老师</span>"，即将在线上服务真实用户。
</div>

---

# 三件事，各解决一个真实问题

<div class="mt-6 space-y-4">

<div class="border-l-4 border-primary pl-4 py-1">
<h3 class="text-primary">① 不瞎猜：缺信息，先反问</h3>
<div class="mt-1 opacity-80">没说清省份/分数，它不硬答，而是<b>带选项反问</b>，答完从断点继续。</div>
</div>

<div class="border-l-4 border-primary pl-4 py-1">
<h3 class="text-primary">② 不断片：长对话自动"记笔记"</h3>
<div class="mt-1 opacity-80">聊得再久也不失忆，旧对话在后台<b>悄悄压缩成记忆</b>，用户无感。</div>
</div>

<div class="border-l-4 border-primary pl-4 py-1">
<h3 class="text-primary">③ 不打架：同时两个请求也不乱</h3>
<div class="mt-1 opacity-80">连点、并发、抢额度，都能<b>有序处理</b>，不超扣、不串台。</div>
</div>

</div>

<div class="mt-5 text-center opacity-70">下面各举一个例子 ——只讲"它到底怎么做到的"。</div>

---

# 「不瞎猜」：缺信息先反问，而不是乱答

<div class="grid grid-cols-2 gap-8 mt-4">

<div>
<div class="text-sm opacity-60 mb-3">常见做法：不懂也硬答</div>
<div class="space-y-2.5">
<div class="flex gap-2 items-end justify-end"><div class="bubble-user rounded-2xl rounded-br-md px-3 py-2 text-sm shadow-sm">计算机专业哪个学校好？</div><div class="avatar-user w-6 h-6 rounded-full text-white text-xs flex items-center justify-center flex-shrink-0">你</div></div>
<div class="flex gap-2 items-end"><div class="avatar-user w-6 h-6 rounded-full text-white text-xs flex items-center justify-center flex-shrink-0">AI</div><div class="bubble-user rounded-2xl rounded-bl-md px-3 py-2 text-sm shadow-sm">一般来说 XX 职院还不错……</div></div>
<div class="text-xs opacity-50 pl-8">不问科类 / 估分就硬答 → 答了等于没答</div>
</div>
</div>

<div>
<div class="text-sm text-primary font-bold mb-3">我们的做法：先问清，再作答</div>
<div class="space-y-2.5">
<div class="flex gap-2 items-end justify-end"><div class="bubble-user rounded-2xl rounded-br-md px-3 py-2 text-sm shadow-sm">计算机专业哪个学校好？</div><div class="avatar-user w-6 h-6 rounded-full text-white text-xs flex items-center justify-center flex-shrink-0">你</div></div>
<div class="flex gap-2 items-end"><div class="avatar-ai w-6 h-6 rounded-full text-white text-xs flex items-center justify-center flex-shrink-0">AI</div><div class="bubble-ai rounded-2xl rounded-bl-md px-3 py-2 text-sm shadow-sm">想帮你选准，先确认：普高类还是中职对口？单招估分多少？想留哪个市？</div></div>
<div class="flex gap-2 items-end justify-end"><div class="bubble-user rounded-2xl rounded-br-md px-3 py-2 text-sm shadow-sm">普高类，估分 420，想留长沙</div><div class="avatar-user w-6 h-6 rounded-full text-white text-xs flex items-center justify-center flex-shrink-0">你</div></div>
<div class="flex gap-2 items-end"><div class="avatar-ai w-6 h-6 rounded-full text-white text-xs flex items-center justify-center flex-shrink-0">AI</div><div class="bubble-ai rounded-2xl rounded-bl-md px-3 py-2 text-sm shadow-sm">好，普高类 420、长沙，我按这个来筛……</div></div>
</div>
</div>

</div>

<div class="mt-5 text-center">
关键：反问时它会<b>暂停</b>当前任务，等你回答后<span class="text-primary font-bold">从断点继续</span>，而不是从头再问一遍。
</div>

---

# 「不断片」：上下文怎么被"无感压缩"

<div class="grid grid-cols-2 gap-8 mt-4">

<div>
<div class="text-sm opacity-60 mb-3">用户看到的：一段顺畅的对话</div>
<div class="space-y-2.5">
<div class="flex gap-2 items-end justify-end"><div class="bubble-user rounded-2xl rounded-br-md px-3 py-2 text-sm shadow-sm">我中职对口，护理类，估分 410</div><div class="avatar-user w-6 h-6 rounded-full text-white text-xs flex items-center justify-center flex-shrink-0">你</div></div>
<div class="flex gap-2 items-end"><div class="avatar-ai w-6 h-6 rounded-full text-white text-xs flex items-center justify-center flex-shrink-0">AI</div><div class="bubble-ai rounded-2xl rounded-bl-md px-3 py-2 text-sm shadow-sm">410 分护理类，我们看看……</div></div>
<div class="text-center text-xs opacity-40">…往后又聊了几十轮：专业、院校、往年录取线…</div>
<div class="flex gap-2 items-end justify-end"><div class="bubble-user rounded-2xl rounded-br-md px-3 py-2 text-sm shadow-sm">那我这分，助产专业稳吗？</div><div class="avatar-user w-6 h-6 rounded-full text-white text-xs flex items-center justify-center flex-shrink-0">你</div></div>
<div class="flex gap-2 items-end"><div class="avatar-ai w-6 h-6 rounded-full text-white text-xs flex items-center justify-center flex-shrink-0">AI</div><div class="bubble-ai rounded-2xl rounded-bl-md px-3 py-2 text-sm shadow-sm">按你 410、护理对口来看……<span class="opacity-60">（依然记得）</span></div></div>
</div>
</div>

<div>
<div class="text-sm opacity-60 mb-3">系统在背后悄悄做的</div>
<div class="space-y-2.5 text-sm">
<div>① 对话变长，最早的"410 / 护理对口"眼看要被挤出模型的记忆窗口</div>
<div class="memo-card rounded-xl p-3">
<div class="text-primary font-bold text-xs mb-1">自动生成的"记忆卡片"</div>
中职对口 · 护理类 · 估分 410<br/>关注：护理 / 助产　意向：长沙、株洲<br/>已排除：省外院校
</div>
<div>② 把这张卡片，随新问题一起发给模型</div>
<div>③ 用户全程无感 —— 不卡、不重复问、不失忆</div>
</div>
</div>

</div>

<div class="mt-5 text-center">
像给 AI 配了个<span class="text-primary font-bold">随时记笔记的秘书</span>：旧对话浓缩成要点，新对话照常继续。
</div>

---

# 「不打架」：同时来两个请求，也不会乱

<div class="text-sm opacity-70 mt-2">比如：网络一卡连点两次"发送"；或额度只剩 1 次，两个请求几乎同时到</div>

<div class="grid grid-cols-2 gap-6 mt-5">

<div class="card-danger rounded-xl p-5">
<h3 class="text-gray-600">如果不管</h3>
<ul class="mt-3 space-y-2 text-sm">
<li>两个请求都读到"还剩 1 次" → 都放行 → <b>白扣 / 超用</b></li>
<li>两条回复同时写进一个对话 → <b>互相截断、内容错乱</b></li>
</ul>
</div>

<div class="card-safe rounded-xl p-5">
<h3 class="text-primary">我们的做法：临界区</h3>
<ul class="mt-3 space-y-2 text-sm">
<li>把"扣额度、写回复"这些关键动作，圈成一次只放一个人进的<b>"窄门"</b></li>
<li>谁先进谁执行，另一个排队或被挡下（"正在生成中 / 额度不足"）</li>
<li>动作<b>要么整段成功，要么整段回退</b>，不留半成品</li>
</ul>
</div>

</div>

<div class="mt-5 text-center">
高峰期再热闹，也<span class="text-primary font-bold">不会乱套</span>。
</div>

---
layout: fact
---

# 即将上线

<div>不是概念演示，是每天在跑的<span class="text-primary">生产系统</span></div>

---
layout: section
---

# 06 / 下一步 · 三件事

从"C 端 AI 老师"，走向"公司参谋部"

---

# 下一步①：权限与围栏

<div class="mt-2 text-lg opacity-70">这就是前面说的 <b>Harness</b> —— 给 Agent 划边界、定红线</div>

<div class="grid grid-cols-2 gap-8 mt-8">

<div>
<h3 class="text-primary">现状</h3>
<ul class="mt-3 space-y-2">
<li>权限只到<b>"用户"</b>这一层</li>
<li>能不能看某块数据，还没有部门/角色维度</li>
</ul>
<div class="mt-4 opacity-70 text-sm">已有雏形：额度"预扣退还"就是一种围栏 —— 用完即止、超支即拦。</div>
</div>

<div>
<h3 class="text-primary">要补的能力</h3>
<ul class="mt-3 space-y-2">
<li>权限扩展到<b>部门 / 角色</b>维度</li>
<li>公共数据人人可查，<b>敏感数据按岗位隔离</b></li>
<li>关键动作有红线，越界自动拦</li>
</ul>
</div>

</div>

<div class="mt-6 text-center text-lg">
让 Agent 强大，<span class="text-primary font-bold">但始终在可控范围内</span>。
</div>

---

# 下一步②：公共工具 + 核心人员 MCP

<div class="mt-2 text-lg opacity-70">这就是前面说的 <b>MCP</b> —— 统一接口，按人开放</div>

<div class="grid grid-cols-2 gap-8 mt-8">

<div class="border border-gray-300 rounded-lg p-5">
<h3 class="text-primary">公共 Tools</h3>
<div class="mt-2 text-sm opacity-60">人人可用</div>
<ul class="mt-3 space-y-2">
<li>常用查询、通用统计</li>
<li>标准化、无敏感数据</li>
<li>降低"什么都问技术"的日常负担</li>
</ul>
</div>

<div class="border border-gray-300 rounded-lg p-5">
<h3 class="text-primary">核心人员 MCP</h3>
<div class="mt-2 text-sm opacity-60">更高权限</div>
<ul class="mt-3 space-y-2">
<li>跨部门数据、<b>多维度图表按需生成</b></li>
<li>负责人自己就能拉数、看趋势</li>
<li><b>不再排队等技术出报表</b></li>
</ul>
</div>

</div>

<div class="mt-6 text-center text-lg">
把技术从"单点参谋"里<span class="text-primary font-bold">解放出来</span>。
</div>

---

# 下一步③：知识库打通 + 多租户

<div class="mt-2 text-lg opacity-70">这就是 <b>Skill 的组织化</b> —— 把散落的经验，变成可复用的知识资产</div>

<div class="grid grid-cols-2 gap-8 mt-6">

<div>
<h3 class="text-primary">今天的痛</h3>
<ul class="mt-3 space-y-2">
<li>内部 SOP、文档，散在各处</li>
<li>对外的学校/专业/分数线数据，另成一摊</li>
<li>没有<b>统一检索层</b> —— 问一次答一次，答完就忘</li>
</ul>
</div>

<div>
<h3 class="text-primary">已定下的方向</h3>
<ul class="mt-3 space-y-2">
<li><b>已决定接入 Turbopuffer</b>，建统一知识库供 Agent 直接检索</li>
<li>内外部数据<b>按"租户"隔离</b>，互不串门</li>
<li>公共知识共享，私有知识各自可见</li>
</ul>
</div>

</div>

---

# 知识库长什么样：多租户

<div class="mt-6 flex flex-col items-center gap-1">
  <div class="border border-gray-300 rounded-lg px-6 py-1.5">Agent 参谋部</div>
  <div class="text-xl text-primary leading-none">↓</div>
  <div class="border-2 border-primary rounded-lg px-8 py-1.5 text-primary font-bold">统一知识库 · Turbopuffer</div>
  <div class="text-xl text-primary leading-none">↓</div>
  <div class="grid grid-cols-4 gap-3 w-full text-center text-sm">
    <div class="border border-gray-300 rounded-lg p-2">租户 · 内部<br/>SOP / 文档 / 数据</div>
    <div class="border border-gray-300 rounded-lg p-2">租户 · 本校对外<br/>专业 / 分数线</div>
    <div class="border border-gray-300 rounded-lg p-2">租户 · 其他学校<br/>数据隔离</div>
    <div class="border border-gray-300 rounded-lg p-2">公共知识<br/>共享层</div>
  </div>
</div>

<div class="grid grid-cols-3 gap-4 mt-5 text-sm text-center">
<div class="border border-gray-300 rounded p-3"><b class="text-primary">对象存储原生</b><br/>便宜、可扩展</div>
<div class="border border-gray-300 rounded p-3"><b class="text-primary">向量 + 全文检索</b><br/>问得准、找得到</div>
<div class="border border-gray-300 rounded p-3"><b class="text-primary">多租户 + 分支</b><br/>天然隔离、可克隆</div>
</div>

<div class="mt-4 text-center text-sm opacity-60">
选型已定：<b class="text-primary">已决定接入 Turbopuffer</b> 作为统一检索层（turbopuffer.com/docs）
</div>

---
layout: section
---

# 07 / 如果它长大了？

---
layout: two-cols
---

# 每一次技术浪潮，都会重塑形态

<div class="mt-4 space-y-3">

<div class="flex gap-3"><div class="text-primary font-bold w-16">4G</div><div>图文 → <b>短视频</b>，长出了抖音</div></div>
<div class="flex gap-3"><div class="text-primary font-bold w-16">推荐</div><div>人找信息 → <b>信息找人</b></div></div>
<div class="flex gap-3"><div class="text-primary font-bold w-16">AI</div><div>人找数据 → <b>数据主动来找人</b></div></div>

</div>

<div class="mt-6 opacity-70 text-sm">
教育/备考信息服务，正在迎来自己的"形态切换"。
</div>

::right::

<div class="pl-6 mt-14">
<div class="border-l-4 border-primary pl-4 py-2">
<div class="text-lg">当内部参谋部足够好用</div>
<div class="mt-3 text-xl font-bold text-primary">它也可能对外开放</div>
<div class="mt-3 opacity-70">给其他学校、机构使用 —— 多租户能力，本就是为这一步预留的。</div>
</div>
</div>

<!--
讲者备注：这一页克制，一笔带过。内部为主，不展开市场规模/商业模式。
但要点到：多租户 = 对外开放的技术前提，我们现在就在为它打地基。
-->

---
layout: statement
---

# 各自为战，还是协同作战？

<div class="text-2xl mt-4 opacity-80">当每个部门都有"参谋部式"的支持，答案会不一样</div>

---
layout: section
---

# 08 / 讨论 · 需要大家拍板

---

# 今天希望达成的几件事

<div class="mt-8 space-y-5 text-xl">

<div class="flex items-start gap-4">
<span class="text-primary font-bold text-2xl">1</span>
<div><b>试点</b>：选 1-2 个协同最痛的部门，先跑起来</div>
</div>

<div class="flex items-start gap-4">
<span class="text-primary font-bold text-2xl">2</span>
<div><b>数据</b>：哪些数据可以进公共知识库，哪些要按角色隔离 —— 需要各部门圈定范围</div>
</div>

<div class="flex items-start gap-4">
<span class="text-primary font-bold text-2xl">3</span>
<div><b>排期</b>：权限围栏 / 公共工具 / 知识库，三件事的优先级和节奏</div>
</div>

</div>

<div class="mt-10 text-center text-2xl text-primary font-bold">
让我们从"闭门造车"，走向"看同一张地图"
</div>

<!--
讲者备注：以行动项收尾。把"分享"变成"决策会"。
-->

---
layout: center
class: text-center
---

# 谢谢

欢迎拍砖 · 期待一起把这件事做成

<div class="mt-4 opacity-60 text-sm">技术团队 · 2026.07</div>
