# 导演风格数据库（Director Style Database）

> 原子库 · 共 40 位（国际26 + 华语14）｜ 用于"一键套用某导演的视觉与叙事风格"。
> 供模块4调用：把 `模仿提示词` 拼进生图/生视频提示词，即可逼近该导演质感。

## 字段格式
导演名(英文) / 代表作 / 视觉签名(镜头·构图·运镜) / 用光与色彩 / 叙事与母题 / 模仿提示词关键词 / 适配题材

---

## 一、国际导演（1–26）

**1. 克里斯托弗·诺兰 Christopher Nolan**
- 代表作：盗梦空间、星际穿越、敦刻尔克、奥本海默
- 视觉签名：IMAX大画幅实拍、宏大实景、交叉剪辑、旋转/失重镜头
- 用光与色彩：冷峻自然光、低饱和钢蓝灰
- 叙事与母题：非线性时间、嵌套结构、时间/记忆/执念
- 模仿提示词：`IMAX large format, epic practical scale, cold desaturated palette, intricate cross-cutting, grand realism`
- 适配题材：科幻、悬疑、战争、烧脑

**2. 丹尼斯·维伦纽瓦 Denis Villeneuve**
- 代表作：沙丘、银翼杀手2049、降临、边境杀手
- 视觉签名：极简宏大构图、巨物渺小人、缓慢推进、对称留白
- 用光与色彩：大色块单色雾霾（橙雾/冷蓝）、剪影
- 叙事与母题：沉浸压抑、宿命、人与未知
- 模仿提示词：`monolithic minimalist scale, tiny human in vast space, monochrome haze, brutalist, atmospheric fog, slow ominous`
- 适配题材：科幻、史诗、悬疑

**3. 斯坦利·库布里克 Stanley Kubrick**
- 代表作：2001太空漫游、闪灵、发条橙
- 视觉签名：·完美单点对称、超广角、库布里克凝视、轨道长推
- 用光与色彩：高对比、实用光源、冷暖极端
- 叙事与母题：冷峻疏离、人性异化、秩序与疯狂
- 模仿提示词：`one-point perspective symmetry, Kubrick stare, wide angle, clinical precision, unsettling order`
- 适配题材：科幻、恐怖、心理

**4. 阿尔弗雷德·希区柯克 Alfred Hitchcock**
- 代表作：惊魂记、迷魂记、后窗、群鸟
- 视觉签名：移焦变焦(眩晕)、主观窥视镜头、楼梯俯拍
- 用光与色彩：黑色电影阴影、高反差
- 叙事与母题：悬念(炸弹理论)、窥视、罪与恐惧
- 模仿提示词：`dolly zoom vertigo, voyeuristic POV, suspenseful shadows, noir high contrast`
- 适配题材：悬疑、惊悚、犯罪

**5. 昆汀·塔伦蒂诺 Quentin Tarantino**
- 代表作：低俗小说、杀死比尔、无耻混蛋
- 视觉签名：脚部特写、后备箱视角、超长对话、墨西哥对峙
- 用光与色彩：复古胶片暖调、饱和血红
- 叙事与母题：章节体非线性、暴力美学、致敬B级片
- 模仿提示词：`trunk shot, foot close-up, retro film grain, stylized violence, snappy dialogue framing`
- 适配题材：犯罪、动作、黑色幽默

**6. 韦斯·安德森 Wes Anderson**
- 代表作：布达佩斯大饭店、月升王国
- 视觉签名：·绝对对称中心构图、90°快速摇/平移、平面化舞台感、俯拍道具
- 用光与色彩：·高饱和糖果色、粉黄撞色、复古配色板
- 叙事与母题：童话感、章节卡片、怀旧、忧伤喜剧
- 模仿提示词：`Wes Anderson style, perfectly symmetrical centered, pastel candy palette, flat tableau, whimsical, dollhouse`
- 适配题材：喜剧、文艺、童话

**7. 大卫·芬奇 David Fincher**
- 代表作：搏击俱乐部、七宗罪、消失的爱人、社交网络
- 视觉签名：精密构图、冷静缓推、数字化顺滑运镜、暗部细节
- 用光与色彩：·墨绿/暗黄低调、阴郁、极低饱和
- 叙事与母题：冷峻悬疑、人性阴暗、控制与崩坏
- 模仿提示词：`Fincher style, dark muted green-yellow palette, meticulous framing, low-key cold, clinical precision`
- 适配题材：犯罪、惊悚、心理

**8. 史蒂文·斯皮尔伯格 Steven Spielberg**
- 代表作：E.T.、辛德勒的名单、侏罗纪公园
- 视觉签名：斯皮尔伯格凝视(仰望惊叹)、流畅长镜调度、光束逆光
- 用光与色彩：温暖怀旧、神圣逆光、希望暖调
- 叙事与母题：童真与奇观、家庭、人性救赎
- 模仿提示词：`Spielberg face of wonder, warm backlit glow, sense of awe, sweeping camera, sentimental`
- 适配题材：冒险、家庭、史诗

**9. 马丁·斯科塞斯 Martin Scorsese**
- 代表作：好家伙、出租车司机、愤怒的公牛
- 视觉签名：长跟拍一镜到底、定格旁白、快速变焦、暴力特写
- 用光与色彩：饱和红、都市夜霓虹、年代质感
- 叙事与母题：黑帮浮沉、罪与赎、男性暴力
- 模仿提示词：`Scorsese long tracking oner, freeze-frame voiceover, saturated reds, gritty urban night`
- 适配题材：黑帮、犯罪、传记

**10. 雷德利·斯科特 Ridley Scott**
- 代表作：银翼杀手、异形、角斗士
- 视觉签名：烟雾光束、纵深布景、宏大场面、风扇光影
- 用光与色彩：体积光烟雾、冷蓝工业、史诗暖金
- 叙事与母题：反乌托邦、生存、文明与野蛮
- 模仿提示词：`Ridley Scott atmospheric haze, volumetric light beams, layered production design, epic scale`
- 适配题材：科幻、史诗、惊悚

**11. 詹姆斯·卡梅隆 James Cameron**
- 代表作：阿凡达、泰坦尼克号、终结者2
- 视觉签名：顶级特效奇观、大场面调度、动态运动镜头
- 用光与色彩：阿凡达生物荧光、科技冷调、宏大鲜艳
- 叙事与母题：技术奇观、人与自然/机器、灾难爱情
- 模仿提示词：`Cameron spectacle, bioluminescent, cutting-edge VFX, grand dynamic action, immersive scale`
- 适配题材：科幻、动作、灾难

**12. 蒂姆·波顿 Tim Burton**
- 代表作：剪刀手爱德华、僵尸新娘、大鱼
- 视觉签名：哥特怪诞、扭曲尖锐造型、夸张角色设计
- 用光与色彩：·高对比黑白+诡异紫绿、苍白人物
- 叙事与母题：怪人/局外人、黑色童话、孤独温情
- 模仿提示词：`Tim Burton gothic, whimsical macabre, twisted spiky shapes, pale characters, dark fairytale`
- 适配题材：奇幻、哥特、动画

**13. 吉尔莫·德尔·托罗 Guillermo del Toro**
- 代表作：潘神的迷宫、水形物语、地狱男爵
- 视觉签名：精致怪物设计、童话与残酷并置、实体特效质感
- 用光与色彩：·标志性青绿+暖琥珀对撞、暗调奇幻
- 叙事与母题：怪物即美、童话寓言、边缘者
- 模仿提示词：`del Toro dark fairytale, teal and amber, ornate creature design, gothic fantasy, tactile`
- 适配题材：奇幻、恐怖、寓言

**14. 阿方索·卡隆 Alfonso Cuarón**
- 代表作：地心引力、罗马、人类之子
- 视觉签名：·超长一镜到底、沉浸跟拍、自然手持
- 用光与色彩：自然光写实、罗马黑白、柔和
- 叙事与母题：沉浸临场、记忆、人性微光
- 模仿提示词：`Cuarón immersive long take, continuous oner, naturalistic light, handheld realism`
- 适配题材：剧情、科幻、文艺

**15. 亚利桑德罗·伊纳里图 Iñárritu**
- 代表作：荒野猎人、鸟人、爱情是狗娘
- 视觉签名：伪一镜到底、贴脸跟拍、自然光实拍
- 用光与色彩：荒野猎人全自然光、冷峻原始
- 叙事与母题：生存挣扎、命运交织、人性极境
- 模仿提示词：`Iñárritu seamless long take, intimate handheld follow, natural light only, raw survival`
- 适配题材：剧情、生存、心理

**16. 达伦·阿伦诺夫斯基 Darren Aronofsky**
- 代表作：黑天鹅、梦之安魂曲、摔角王
- 视觉签名：贴身跟拍(SnorriCam)、快速剪辑蒙太奇(hip-hop montage)、镜像
- 用光与色彩：黑天鹅黑白对立、压抑冷调
- 叙事与母题：执念癫狂、自毁、身心崩坏
- 模仿提示词：`Aronofsky body-mounted SnorriCam, rapid hip-hop montage, claustrophobic, descent into madness`
- 适配题材：心理、惊悚、剧情

**17. 科恩兄弟 Coen Brothers**
- 代表作：老无所依、冰血暴、谋杀绿脚趾
- 视觉签名：精确构图、广角变形、黑色幽默调度
- 用光与色彩：地域质感、冷峻或昏黄
- 叙事与母题：荒诞命运、黑色幽默、宿命无常
- 模仿提示词：`Coen brothers, precise wide-angle framing, deadpan dark comedy, bleak Americana`
- 适配题材：犯罪、黑色幽默、剧情

**18. 大卫·林奇 David Lynch**
- 代表作：穆赫兰道、蓝丝绒、双峰
- 视觉签名：超现实梦境、诡异慢节奏、红帘幕意象
- 用光与色彩：浓重阴影、诡异红蓝、迷离
- 叙事与母题：潜意识、双重身份、表象下的恐怖
- 模仿提示词：`Lynchian surreal, dreamlike unsettling, deep shadows, red curtains, eerie ambiguity`
- 适配题材：超现实、惊悚、悬疑

**19. 泰伦斯·马力克 Terrence Malick**
- 代表作：生命之树、细细的红线、天堂之日
- 视觉签名：·黄金时刻自然光、广角仰拍自然、流动手持、低位仰望
- 用光与色彩：魔幻时刻金光、自然柔美
- 叙事与母题：意识流、低语旁白、人与自然/神性
- 模仿提示词：`Malick golden hour natural light, wide-angle low looking up, flowing handheld, poetic nature, whispered voiceover`
- 适配题材：文艺、哲思、史诗

**20. 保罗·托马斯·安德森 PTA**
- 代表作：血色将至、不羁夜、魅影缝匠
- 视觉签名：流畅长跟、缓推、复古胶片、人物中心
- 用光与色彩：年代暖调、自然布光、胶片颗粒
- 叙事与母题：野心与孤独、美式人物史诗
- 模仿提示词：`PTA fluid tracking, slow push-in, vintage film stock, character-driven, period warmth`
- 适配题材：剧情、传记、年代

**21. 朴赞郁 Park Chan-wook**
- 代表作：老男孩、小姐、分手的决心
- 视觉签名：·华丽运镜、不可能机位、对称暴力美学、空间穿越运镜
- 用光与色彩：浓郁高饱和、典雅冷艳
- 叙事与母题：复仇、禁忌情欲、命运反转
- 模仿提示词：`Park Chan-wook ornate camera moves, impossible angles, lush saturated color, stylized symmetry`
- 适配题材：复仇、悬疑、情色惊悚

**22. 奉俊昊 Bong Joon-ho**
- 代表作：寄生虫、母亲、雪国列车
- 视觉签名：垂直空间隐喻、精准构图、横移调度
- 用光与色彩：写实质感、阶级冷暖对比
- 叙事与母题：阶级、黑色幽默+悲剧、社会寓言
- 模仿提示词：`Bong Joon-ho vertical class metaphor, precise framing, lateral tracking, social realism with dark satire`
- 适配题材：剧情、社会、惊悚

**23. 黑泽明 Akira Kurosawa**
- 代表作：七武士、罗生门、乱
- 视觉签名：·多机位、长焦压缩、运动中群像、天候(风雨)调度
- 用光与色彩：黑白高反差、自然天光、大胆色块(乱)
- 叙事与母题：武士道、人性多面、史诗群戏
- 模仿提示词：`Kurosawa telephoto compression, dynamic weather, epic ensemble in motion, bold elemental`
- 适配题材：古装、史诗、武士

**24. 是枝裕和 Hirokazu Kore-eda**
- 代表作：小偷家族、步履不停、无人知晓
- 视觉签名：固定中景、平视、生活流长镜、餐桌戏
- 用光与色彩：自然柔光、温润日常、低饱和暖
- 叙事与母题：家庭、日常细节、温情与残酷
- 模仿提示词：`Kore-eda still medium shots, eye-level, natural soft light, quiet domestic realism, slice of life`
- 适配题材：家庭、文艺、剧情

**25. 宫崎骏 Hayao Miyazaki**
- 代表作：千与千寻、龙猫、哈尔的移动城堡
- 视觉签名：手绘2D、丰富自然细节、飞行场面、留白(间)
- 用光与色彩：明丽自然、温暖治愈、丰盈天空云朵
- 叙事与母题：自然与文明、成长、反战、少女主角
- 模仿提示词：`Studio Ghibli hand-drawn 2D, lush nature detail, soft warm palette, whimsical, painterly sky`
- 适配题材：动画、奇幻、成长

**26. 今敏 Satoshi Kon**
- 代表作：未麻的部屋、红辣椒、千年女优
- 视觉签名：·现实与幻想无缝匹配剪辑、跳跃转场、心理蒙太奇
- 用光与色彩：鲜明、虚实交错
- 叙事与母题：梦与现实边界、身份、潜意识
- 模仿提示词：`Satoshi Kon seamless reality-fantasy match cuts, jump transitions, psychological montage, anime`
- 适配题材：动画、心理、悬疑

---

## 二、华语导演（27–40）

**27. 张艺谋 Zhang Yimou**
- 代表作：红高粱、英雄、大红灯笼高高挂、影
- 视觉签名：·极致色彩美学、大色块对称、人海方阵、对称构图
- 用光与色彩：·高饱和红/金，或《影》水墨黑白灰
- 叙事与母题：民族寓言、命运、视觉仪式感
- 模仿提示词：`Zhang Yimou bold color symbolism, massive symmetrical formations, saturated red and gold, or ink-wash monochrome`
- 适配题材：古装、史诗、武侠、文艺

**28. 陈凯歌 Chen Kaige**
- 代表作：霸王别姬、黄土地、妖猫传
- 视觉签名：古典厚重构图、戏曲意象、华丽场面
- 用光与色彩：浓郁古典、舞台暖光、绚烂
- 叙事与母题：历史洪流中的个体、命运悲剧、文化
- 模仿提示词：`Chen Kaige operatic grandeur, classical composition, rich theatrical color, historical epic`
- 适配题材：古装、历史、文艺

**29. 王家卫 Wong Kar-wai**
- 代表作：花样年华、重庆森林、春光乍泄、堕落天使
- 视觉签名：·抽帧慢门拖影、广角变形、手持贴身、镜面框架
- 用光与色彩：·霓虹浓郁、暖黄绿调、高饱和暧昧
- 叙事与母题：错过的爱、孤独、时间与记忆、都市疏离
- 模仿提示词：`Wong Kar-wai step-printing motion blur, neon saturated色, intimate handheld, melancholic urban, framed reflections`
- 适配题材：爱情、文艺、都市

**30. 姜文 Jiang Wen**
- 代表作：阳光灿烂的日子、让子弹飞、鬼子来了
- 视觉签名：浓烈运动镜头、荷尔蒙张力、明亮高反差
- 用光与色彩：阳光炽烈金黄、浓墨重彩
- 叙事与母题：荒诞寓言、权力欲望、男性激情、隐喻
- 模仿提示词：`Jiang Wen vivid kinetic energy, blazing golden sunlight, high-contrast, allegorical bravado`
- 适配题材：剧情、黑色幽默、历史

**31. 毕赣 Bi Gan**
- 代表作：路边野餐、地球最后的夜晚
- 视觉签名：·超长一镜到底(3D长镜)、梦境漫游、潮湿空间
- 用光与色彩：幽暗潮湿、霓虹冷调、迷离绿蓝
- 叙事与母题：记忆与梦、时间循环、诗意乡愁
- 模仿提示词：`Bi Gan dreamlike long take, damp neon-lit, poetic wandering, hypnotic, misty melancholy`
- 适配题材：文艺、梦境、悬疑

**32. 贾樟柯 Jia Zhangke**
- 代表作：三峡好人、山河故人、站台
- 视觉签名：固定长镜、纪实远中景、非职业演员、真实环境
- 用光与色彩：自然光、褪色写实、灰蓝市井
- 叙事与母题：时代变迁、小人物、城乡、记忆
- 模仿提示词：`Jia Zhangke documentary realism, static long takes, faded naturalistic color, ordinary people, changing China`
- 适配题材：现实、文艺、剧情

**33. 侯孝贤 Hou Hsiao-hsien**
- 代表作：悲情城市、刺客聂隐娘、童年往事
- 视觉签名：·极远固定长镜、空镜、克制不动声色、自然光
- 用光与色彩：自然典雅、东方留白、柔和
- 叙事与母题：历史与个人、时间流逝、东方美学
- 模仿提示词：`Hou Hsiao-hsien distant static long take, restrained observation, natural light, oriental negative space`
- 适配题材：文艺、历史、古装

**34. 李安 Ang Lee**
- 代表作：卧虎藏龙、断背山、少年派、色戒
- 视觉签名：细腻流畅、情感克制构图、东西方融合
- 用光与色彩：典雅自然、随题材变(竹林青绿/西部辽阔)
- 叙事与母题：隐忍情感、文化身份、欲望与压抑
- 模仿提示词：`Ang Lee elegant restraint, emotionally precise framing, refined natural light, East-meets-West`
- 适配题材：文艺、武侠、情感、剧情

**35. 徐克 Tsui Hark**
- 代表作：黄飞鸿、倩女幽魂、狄仁杰
- 视觉签名：凌厉快剪、飞天遁地武打、特效奇观、动态运镜
- 用光与色彩：绚丽奇幻、浓墨重彩
- 叙事与母题：武侠新浪潮、家国、奇幻江湖
- 模仿提示词：`Tsui Hark wuxia spectacle, fast kinetic editing, gravity-defying martial arts, fantastical`
- 适配题材：武侠、奇幻、古装动作

**36. 杜琪峰 Johnnie To**
- 代表作：枪火、放逐、PTU、黑社会
- 视觉签名：·静止站位调度(枪战如棋局)、冷峻构图、霓虹夜
- 用光与色彩：港式冷蓝夜、低调硬光、霓虹
- 叙事与母题：宿命、江湖义气、黑帮博弈
- 模仿提示词：`Johnnie To static gunfight standoff, geometric staging, cold neon Hong Kong night, low-key noir`
- 适配题材：警匪、黑帮、犯罪

**37. 吴宇森 John Woo**
- 代表作：英雄本色、喋血双雄、变脸
- 视觉签名：·双枪、白鸽、慢动作枪战、墨西哥对峙
- 用光与色彩：教堂逆光、浪漫暖调、暴力诗意
- 叙事与母题：兄弟情义、忠义、暴力浪漫主义
- 模仿提示词：`John Woo heroic bloodshed, dual pistols, white doves, slow-motion gunfight, Mexican standoff, backlit`
- 适配题材：动作、枪战、英雄片

**38. 周星驰 Stephen Chow**
- 代表作：功夫、少林足球、喜剧之王
- 视觉签名：夸张漫画式、无厘头、夸张特效、速度感
- 用光与色彩：明亮鲜艳、漫画感
- 叙事与母题：小人物逆袭、无厘头喜剧、悲喜交织
- 模仿提示词：`Stephen Chow slapstick exaggeration, cartoonish comic timing, vivid, mo lei tau absurd comedy`
- 适配题材：喜剧、动作喜剧

**39. 宁浩 Ning Hao**
- 代表作：疯狂的石头、无人区、疯狂的外星人
- 视觉签名：多线索交叉、快节奏黑色幽默、手持
- 用光与色彩：市井写实、粗粝
- 叙事与母题：荒诞巧合、小人物群像、黑色幽默
- 模仿提示词：`Ning Hao multi-thread crime caper, fast dark comedy, gritty realism, interlocking coincidence`
- 适配题材：黑色幽默、犯罪、喜剧

**40. 陈思诚 Chen Sicheng**
- 代表作：唐人街探案系列、消失的她
- 视觉签名：商业类型化、悬疑反转、异域奇观、明快剪辑
- 用光与色彩：高饱和异域风情、明亮商业感
- 叙事与母题：本格推理+喜剧、强情节反转、商业类型
- 模仿提示词：`Chen Sicheng commercial mystery, exotic vivid spectacle, twist-driven plotting, slick editing`
- 适配题材：悬疑、喜剧、商业类型

---

## 使用提示
- **风格选用速记**：极致色彩→张艺谋/王家卫；对称强迫美→库布里克/韦斯·安德森；冷峻阴郁→芬奇/杜琪峰；自然诗意→马力克/侯孝贤；梦境超现实→林奇/毕赣/今敏；暴力浪漫→吴宇森/朴赞郁；史诗宏大→维伦纽瓦/诺兰。
- **组合调用**：导演风格 = 该导演常用的「灯光+构图+运镜+色彩」组合，可与对应原子库交叉引用，让镜头方案整体统一。
- **生图/生视频**：把 `模仿提示词` 直接拼入，再叠加题材与场景描述即可。
- 共 **40 位**：国际26 + 华语14。
