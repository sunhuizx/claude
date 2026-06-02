# 导演风格数据库（Director Style Database）

> 原子库 · 共 40 位（国际26 + 华语14）｜ 用于"一键套用某导演的视觉与叙事风格"。
> 供模块4调用：把 `模仿提示词` 拼进生图/生视频提示词，即可逼近该导演质感。

## 字段格式
导演名(英文) / 代表作 / 视觉签名(镜头·构图·运镜) / 用光与色彩 / 叙事与母题 / 模仿提示词关键词 / 适配题材

---

## 一、国际导演（1–26）

1. 克里斯托弗·诺兰 Christopher Nolan｜盗梦/星际/敦刻尔克/奥本海默｜IMAX大画幅实拍·宏大实景·交叉剪辑·旋转失重｜冷峻自然光·低饱和钢蓝灰｜非线性时间/嵌套/时间记忆执念｜`IMAX large format, epic practical scale, cold desaturated, intricate cross-cutting`｜科幻/悬疑/战争/烧脑
2. 丹尼斯·维伦纽瓦 Denis Villeneuve｜沙丘/银翼2049/降临｜极简宏大·巨物渺小人·缓慢推进·对称留白｜大色块单色雾霾·剪影｜沉浸压抑/宿命/人与未知｜`monolithic minimalist scale, tiny human, monochrome haze, brutalist, atmospheric fog`｜科幻/史诗/悬疑
3. 斯坦利·库布里克 Stanley Kubrick｜2001/闪灵/发条橙｜⭐完美单点对称·超广角·库布里克凝视·轨道长推｜高对比·实用光源·冷暖极端｜冷峻疏离/异化/秩序与疯狂｜`one-point symmetry, Kubrick stare, wide angle, clinical, unsettling order`｜科幻/恐怖/心理
4. 阿尔弗雷德·希区柯克 Hitchcock｜惊魂记/迷魂记/后窗｜移焦变焦·主观窥视·楼梯俯拍｜黑色电影阴影·高反差｜悬念(炸弹理论)/窥视/罪与恐惧｜`dolly zoom vertigo, voyeuristic POV, suspenseful shadows, noir`｜悬疑/惊悚/犯罪
5. 昆汀·塔伦蒂诺 Tarantino｜低俗小说/杀死比尔/无耻混蛋｜脚部特写·后备箱视角·超长对话·墨西哥对峙｜复古胶片暖调·饱和血红｜章节非线性/暴力美学/致敬B级片｜`trunk shot, foot close-up, retro film grain, stylized violence`｜犯罪/动作/黑色幽默
6. 韦斯·安德森 Wes Anderson｜布达佩斯大饭店/月升王国｜⭐绝对对称中心·90°快速摇/平移·平面舞台·俯拍道具｜⭐高饱和糖果色·粉黄撞色｜童话/章节卡片/怀旧忧伤喜剧｜`Wes Anderson style, symmetrical centered, pastel candy palette, flat tableau, whimsical`｜喜剧/文艺/童话
7. 大卫·芬奇 David Fincher｜搏击俱乐部/七宗罪/消失的爱人/社交网络｜精密构图·冷静缓推·数字顺滑运镜·暗部细节｜⭐墨绿暗黄低调·阴郁·极低饱和｜冷峻悬疑/人性阴暗/控制崩坏｜`Fincher dark muted green-yellow, meticulous framing, low-key cold, clinical`｜犯罪/惊悚/心理
8. 史蒂文·斯皮尔伯格 Spielberg｜E.T./辛德勒名单/侏罗纪｜斯式凝视(仰望惊叹)·流畅长镜·光束逆光｜温暖怀旧·神圣逆光·希望暖调｜童真奇观/家庭/人性救赎｜`Spielberg face of wonder, warm backlit glow, awe, sweeping camera`｜冒险/家庭/史诗
9. 马丁·斯科塞斯 Scorsese｜好家伙/出租车司机/愤怒的公牛｜长跟一镜到底·定格旁白·快速变焦·暴力特写｜饱和红·都市霓虹·年代质感｜黑帮浮沉/罪与赎/男性暴力｜`Scorsese long tracking oner, freeze-frame voiceover, saturated reds, gritty urban`｜黑帮/犯罪/传记
10. 雷德利·斯科特 Ridley Scott｜银翼杀手/异形/角斗士｜烟雾光束·纵深布景·宏大场面·风扇光影｜体积光烟雾·冷蓝工业·史诗暖金｜反乌托邦/生存/文明野蛮｜`atmospheric haze, volumetric light beams, layered design, epic`｜科幻/史诗/惊悚
11. 詹姆斯·卡梅隆 Cameron｜阿凡达/泰坦尼克/终结者2｜顶级特效奇观·大场面调度·动态运动｜生物荧光·科技冷调·宏大鲜艳｜技术奇观/人与自然机器/灾难爱情｜`Cameron spectacle, bioluminescent, cutting-edge VFX, grand dynamic action`｜科幻/动作/灾难
12. 蒂姆·波顿 Tim Burton｜剪刀手/僵尸新娘/大鱼｜哥特怪诞·扭曲尖锐造型·夸张角色｜⭐高对比黑白+诡异紫绿·苍白人物｜怪人局外人/黑色童话/孤独温情｜`Tim Burton gothic, whimsical macabre, twisted spiky, pale, dark fairytale`｜奇幻/哥特/动画
13. 吉尔莫·德尔·托罗 del Toro｜潘神迷宫/水形物语｜精致怪物·童话与残酷并置·实体特效质感｜⭐青绿+暖琥珀对撞·暗调奇幻｜怪物即美/童话寓言/边缘者｜`del Toro dark fairytale, teal and amber, ornate creature design, gothic`｜奇幻/恐怖/寓言
14. 阿方索·卡隆 Cuarón｜地心引力/罗马/人类之子｜⭐超长一镜到底·沉浸跟拍·自然手持｜自然光写实·罗马黑白·柔和｜沉浸临场/记忆/人性微光｜`immersive long take, continuous oner, naturalistic light, handheld`｜剧情/科幻/文艺
15. 伊纳里图 Iñárritu｜荒野猎人/鸟人｜伪一镜到底·贴脸跟拍·自然光实拍｜全自然光·冷峻原始｜生存挣扎/命运交织/人性极境｜`seamless long take, intimate handheld follow, natural light only, raw`｜剧情/生存/心理
16. 达伦·阿伦诺夫斯基 Aronofsky｜黑天鹅/梦之安魂曲｜贴身SnorriCam·快速蒙太奇·镜像｜黑白对立·压抑冷调｜执念癫狂/自毁/身心崩坏｜`body-mounted SnorriCam, rapid montage, claustrophobic, descent into madness`｜心理/惊悚
17. 科恩兄弟 Coen Brothers｜老无所依/冰血暴｜精确构图·广角变形·黑色幽默调度｜地域质感·冷峻昏黄｜荒诞命运/黑色幽默/宿命无常｜`Coen brothers, precise wide-angle, deadpan dark comedy, bleak Americana`｜犯罪/黑色幽默
18. 大卫·林奇 David Lynch｜穆赫兰道/蓝丝绒/双峰｜超现实梦境·诡异慢节奏·红帘幕意象｜浓重阴影·诡异红蓝·迷离｜潜意识/双重身份/表象下恐怖｜`Lynchian surreal, dreamlike unsettling, deep shadows, red curtains, eerie`｜超现实/惊悚/悬疑
19. 泰伦斯·马力克 Malick｜生命之树/细细的红线｜⭐黄金时刻自然光·广角仰拍自然·流动手持·低位仰望｜魔幻时刻金光·自然柔美｜意识流/低语旁白/人与自然神性｜`golden hour natural light, wide low looking up, flowing handheld, poetic nature`｜文艺/哲思/史诗
20. 保罗·托马斯·安德森 PTA｜血色将至/不羁夜/魅影缝匠｜流畅长跟·缓推·复古胶片·人物中心｜年代暖调·自然布光·胶片颗粒｜野心与孤独/美式人物史诗｜`fluid tracking, slow push-in, vintage film stock, character-driven, period`｜剧情/传记/年代
21. 朴赞郁 Park Chan-wook｜老男孩/小姐/分手的决心｜⭐华丽运镜·不可能机位·对称暴力美学·空间穿越运镜｜浓郁高饱和·典雅冷艳｜复仇/禁忌情欲/命运反转｜`ornate camera moves, impossible angles, lush saturated, stylized symmetry`｜复仇/悬疑/情色惊悚
22. 奉俊昊 Bong Joon-ho｜寄生虫/母亲/雪国列车｜垂直空间隐喻·精准构图·横移调度｜写实质感·阶级冷暖对比｜阶级/黑色幽默+悲剧/社会寓言｜`vertical class metaphor, precise framing, lateral tracking, social realism`｜剧情/社会/惊悚
23. 黑泽明 Kurosawa｜七武士/罗生门/乱｜⭐多机位·长焦压缩·运动群像·天候(风雨)调度｜黑白高反差·自然天光·大胆色块｜武士道/人性多面/史诗群戏｜`telephoto compression, dynamic weather, epic ensemble in motion, bold`｜古装/史诗/武士
24. 是枝裕和 Kore-eda｜小偷家族/步履不停｜固定中景·平视·生活流长镜·餐桌戏｜自然柔光·温润日常·低饱和暖｜家庭/日常细节/温情与残酷｜`still medium shots, eye-level, natural soft light, quiet domestic realism`｜家庭/文艺/剧情
25. 宫崎骏 Miyazaki｜千与千寻/龙猫/哈尔｜手绘2D·丰富自然细节·飞行场面·留白｜明丽自然·温暖治愈·丰盈天空云朵｜自然与文明/成长/反战/少女主角｜`Studio Ghibli hand-drawn 2D, lush nature, soft warm palette, painterly sky`｜动画/奇幻/成长
26. 今敏 Satoshi Kon｜未麻的部屋/红辣椒/千年女优｜⭐现实幻想无缝匹配剪辑·跳跃转场·心理蒙太奇｜鲜明·虚实交错｜梦与现实边界/身份/潜意识｜`seamless reality-fantasy match cuts, jump transitions, psychological montage`｜动画/心理/悬疑

## 二、华语导演（27–40）

27. 张艺谋 Zhang Yimou｜红高粱/英雄/大红灯笼/影｜⭐极致色彩美学·大色块对称·人海方阵｜⭐高饱和红金或《影》水墨黑白灰｜民族寓言/命运/视觉仪式感｜`bold color symbolism, massive symmetrical formations, saturated red and gold, or ink-wash`｜古装/史诗/武侠/文艺
28. 陈凯歌 Chen Kaige｜霸王别姬/黄土地/妖猫传｜古典厚重构图·戏曲意象·华丽场面｜浓郁古典·舞台暖光·绚烂｜历史洪流中个体/命运悲剧/文化｜`operatic grandeur, classical composition, rich theatrical color, historical epic`｜古装/历史/文艺
29. 王家卫 Wong Kar-wai｜花样年华/重庆森林/春光乍泄｜⭐抽帧慢门拖影·广角变形·手持贴身·镜面框架｜⭐霓虹浓郁·暖黄绿调·高饱和暧昧｜错过的爱/孤独/时间记忆/都市疏离｜`step-printing motion blur, neon saturated, intimate handheld, melancholic urban`｜爱情/文艺/都市
30. 姜文 Jiang Wen｜阳光灿烂的日子/让子弹飞｜浓烈运动镜头·荷尔蒙张力·明亮高反差｜阳光炽烈金黄·浓墨重彩｜荒诞寓言/权力欲望/男性激情/隐喻｜`vivid kinetic energy, blazing golden sunlight, high-contrast, allegorical bravado`｜剧情/黑色幽默/历史
31. 毕赣 Bi Gan｜路边野餐/地球最后的夜晚｜⭐超长一镜到底(3D长镜)·梦境漫游·潮湿空间｜幽暗潮湿·霓虹冷调·迷离绿蓝｜记忆与梦/时间循环/诗意乡愁｜`dreamlike long take, damp neon-lit, poetic wandering, hypnotic, misty`｜文艺/梦境/悬疑
32. 贾樟柯 Jia Zhangke｜三峡好人/山河故人/站台｜固定长镜·纪实远中景·非职业演员·真实环境｜自然光·褪色写实·灰蓝市井｜时代变迁/小人物/城乡/记忆｜`documentary realism, static long takes, faded color, ordinary people`｜现实/文艺/剧情
33. 侯孝贤 Hou Hsiao-hsien｜悲情城市/刺客聂隐娘｜⭐极远固定长镜·空镜·克制·自然光｜自然典雅·东方留白·柔和｜历史与个人/时间流逝/东方美学｜`distant static long take, restrained observation, natural light, oriental negative space`｜文艺/历史/古装
34. 李安 Ang Lee｜卧虎藏龙/断背山/少年派/色戒｜细腻流畅·情感克制构图·东西方融合｜典雅自然·随题材变｜隐忍情感/文化身份/欲望压抑｜`elegant restraint, emotionally precise framing, refined natural light`｜文艺/武侠/情感
35. 徐克 Tsui Hark｜黄飞鸿/倩女幽魂/狄仁杰｜凌厉快剪·飞天遁地武打·特效奇观·动态运镜｜绚丽奇幻·浓墨重彩｜武侠新浪潮/家国/奇幻江湖｜`wuxia spectacle, fast kinetic editing, gravity-defying martial arts, fantastical`｜武侠/奇幻/古装动作
36. 杜琪峰 Johnnie To｜枪火/放逐/黑社会｜⭐静止站位调度(枪战如棋局)·冷峻构图·霓虹夜｜港式冷蓝夜·低调硬光·霓虹｜宿命/江湖义气/黑帮博弈｜`static gunfight standoff, geometric staging, cold neon Hong Kong night, noir`｜警匪/黑帮/犯罪
37. 吴宇森 John Woo｜英雄本色/喋血双雄/变脸｜⭐双枪·白鸽·慢动作枪战·墨西哥对峙｜教堂逆光·浪漫暖调·暴力诗意｜兄弟情义/忠义/暴力浪漫主义｜`heroic bloodshed, dual pistols, white doves, slow-mo gunfight, backlit`｜动作/枪战/英雄片
38. 周星驰 Stephen Chow｜功夫/少林足球/喜剧之王｜夸张漫画式·无厘头·夸张特效·速度感｜明亮鲜艳·漫画感｜小人物逆袭/无厘头喜剧/悲喜交织｜`slapstick exaggeration, cartoonish timing, vivid, mo lei tau absurd comedy`｜喜剧/动作喜剧
39. 宁浩 Ning Hao｜疯狂的石头/无人区｜多线索交叉·快节奏黑色幽默·手持｜市井写实·粗粝｜荒诞巧合/小人物群像/黑色幽默｜`multi-thread crime caper, fast dark comedy, gritty, interlocking coincidence`｜黑色幽默/犯罪/喜剧
40. 陈思诚 Chen Sicheng｜唐人街探案/消失的她｜商业类型化·悬疑反转·异域奇观·明快剪辑｜高饱和异域风情·明亮商业感｜本格推理+喜剧/强情节反转/商业类型｜`commercial mystery, exotic vivid spectacle, twist-driven, slick editing`｜悬疑/喜剧/商业类型

## 使用提示
- 风格选用速记：极致色彩→张艺谋/王家卫；对称强迫美→库布里克/韦斯·安德森；冷峻阴郁→芬奇/杜琪峰；自然诗意→马力克/侯孝贤；梦境超现实→林奇/毕赣/今敏；暴力浪漫→吴宇森/朴赞郁；史诗宏大→维伦纽瓦/诺兰。
- 组合调用：导演风格 = 该导演常用「灯光+构图+运镜+色彩」组合，可与对应原子库交叉引用。
- 生图/生视频：把 `模仿提示词` 直接拼入，再叠加题材场景描述即可。
- 共40位：国际26 + 华语14。
