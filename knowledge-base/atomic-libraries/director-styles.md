# 导演风格数据库（Director Style Database）

> 原子库 · 共 70 位（国际46 + 华语14 + 新增AI/技术型·亚洲·纪录/实验10）｜ 用于"一键套用某导演的视觉与叙事风格"。
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

## 三、国际导演（续）（41–55）

41. 赛尔乔·莱昂内 Sergio Leone｜黄金三镖客/西部往事/美国往事｜⭐极端大特写(眼睛)与大远景反差·缓慢仪式化对峙·长焦压缩·决斗三角剪辑｜烈日黄沙·暖褐砂砾·硬光｜西部史诗/暴力宿命/时间记忆｜`spaghetti western, extreme eye close-up vs vast wide, slow standoff, sun-baked telephoto`｜西部/史诗/犯罪
42. 安德烈·塔可夫斯基 Andrei Tarkovsky｜潜行者/镜子/乡愁｜⭐极慢长镜·水与火等自然元素·缓移凝视·梦境质感｜自然柔光·褪色棕调·水汽湿润｜信仰/记忆/时间/精神追寻｜`Tarkovsky slow long take, water and nature elements, dreamlike, sepia muted, spiritual`｜文艺/哲思/诗电影
43. 英格玛·伯格曼 Ingmar Bergman｜第七封印/野草莓/假面｜⭐面部大特写·双人脸部叠合·极简舞台·静默凝视｜黑白高反差·冷峻北欧光｜信仰怀疑/死亡/孤独/心理剖析｜`Bergman intense face close-ups, stark black-and-white, minimalist, psychological silence`｜文艺/心理/哲思
44. 费德里科·费里尼 Federico Fellini｜八部半/大路/甜蜜生活｜⭐马戏团式狂欢调度·梦境游行·夸张群像·流动长镜｜黑白或浓艳·梦幻马戏感｜梦与现实/记忆狂欢/创作焦虑｜`Felliniesque carnival, dreamlike parade, grotesque ensemble, flowing surreal`｜文艺/超现实/喜剧
45. 让-吕克·戈达尔 Jean-Luc Godard｜精疲力尽/狂人皮埃罗｜⭐跳切首创·打破第四面墙·手持街拍·间离｜自然光·三原色块(红蓝白)｜法国新浪潮/解构/政治爱情｜`French New Wave, jump cuts, breaking 4th wall, handheld street, primary color blocks`｜文艺/实验/爱情
46. 佩德罗·阿莫多瓦 Pedro Almodóvar｜对她说/痛苦与荣耀/关于我母亲｜浓烈情节剧调度·质感特写·女性视角构图｜⭐高饱和红绿撞色·浓艳暖调｜欲望/女性/身份/情节剧｜`Almodóvar saturated red and green, melodrama, bold color blocking, sensual`｜情节剧/文艺/情感
47. 尼古拉斯·温丁·雷弗恩 Refn｜亡命驾驶/霓虹恶魔｜极简静止构图·缓慢凝滞·暴力骤起·风格化｜⭐霓虹粉蓝紫·高对比暗调·荧光｜暴力美学/孤独/时尚冷感｜`Refn neon pink-blue, slow static minimalism, sudden violence, hyper-stylized`｜犯罪/惊悚/风格化
48. 埃德加·赖特 Edgar Wright｜极盗车神/热血警探/僵尸肖恩｜⭐快速剪辑·音效同步剪辑·急推急甩·卡点视觉笑点｜明亮高饱和·活泼｜类型戏仿/喜剧节奏/视听同步｜`Edgar Wright rapid cuts, sound-synced editing, whip pans, kinetic comedic timing`｜喜剧/动作/类型
49. 约戈斯·兰斯莫斯 Yorgos Lanthimos｜龙虾/宠儿/可怜的东西｜⭐超广角/鱼眼变形·对称·冷漠平移·诡异构图｜冷峻自然光或浓艳·疏离｜荒诞寓言/权力/人性怪诞｜`Lanthimos wide-angle fisheye distortion, deadpan symmetry, absurd unsettling`｜荒诞/黑色/文艺
50. 阿里·艾斯特 Ari Aster｜遗传厄运/仲夏夜惊魂｜⭐缓慢推进·模型屋俯视·白昼恐怖·对称仪式｜明亮白昼反差恐怖·诡异暖阳｜创伤/家庭崩坏/邪典仪式｜`Ari Aster slow dread, dollhouse overhead shot, daylight horror, symmetrical ritual`｜恐怖/心理/邪典
51. 扎克·施奈德 Zack Snyder｜300勇士/守望者/正义联盟｜⭐升格变速(speed ramp)·高对比剪影·慢动作暴力·史诗定格｜⭐青橙高对比·去饱和金属·阴郁｜神话史诗/超级英雄/暴力美学｜`Zack Snyder speed-ramp slow-mo, teal-orange high contrast, epic silhouettes, desaturated`｜超英/史诗/动作
52. 迈克尔·贝 Michael Bay｜变形金刚/绝地战警/勇闯夺命岛｜⭐英雄低角度环绕(Bayhem)·爆炸·快剪·动态甩镜｜⭐金橙黄昏·镜头光晕·高反差｜爆炸奇观/军事/商业大片｜`Bayhem low-angle hero orbit, explosions, lens flares, golden-hour, frenetic`｜动作/商业/军事
53. 盖·里奇 Guy Ritchie｜两杆大烟枪/偷拐抢骗/绅士｜⭐快速蒙太奇·定格旁白·变速·多线交织犯罪｜饱和伦敦质感·明快｜英式黑帮/多线巧合/痞帅幽默｜`Guy Ritchie fast montage, freeze-frame narration, speed ramps, slick crime caper`｜犯罪/黑色幽默/动作
54. 斯派克·李 Spike Lee｜为所应为/黑色党徒/迷镇凶案｜⭐双人推车浮镜(double dolly)·直视镜头·跳接·政治插入｜饱和浓烈·街区暖调｜种族/社会正义/都市经验｜`Spike Lee double-dolly floating shot, direct address, bold saturated, urban`｜社会/剧情/政治
55. 滨口龙介 Ryusuke Hamaguchi｜驾驶我的车/夜以继日/偶然与想象｜固定中景长对话·车内戏·留白·自然表演｜自然柔光·写实低调｜对话沟通/记忆/偶然与命运｜`Hamaguchi long static dialogue shots, in-car scenes, naturalistic, quiet realism`｜文艺/剧情/情感

## 四、日本动画导演（56–60）

56. 新海诚 Makoto Shinkai｜你的名字/天气之子/秒速五厘米｜⭐极致光影天空·镜头光晕·唯美空镜·细腻自然作画｜⭐绚丽高饱和·逆光光斑·瑰丽天空云彩｜距离与思念/青春/灾难与羁绊｜`Makoto Shinkai luminous skies, lens flares, hyper-detailed nature, radiant saturated, 2D anime`｜动画/青春/爱情
57. 细田守 Mamoru Hosoda｜夏日大作战/狼的孩子/怪物之子｜清爽日常融奇幻·明快构图·家庭温情·虚拟空间设计｜明亮清新·夏日蓝绿·通透｜家庭羁绊/虚拟与现实/成长｜`Hosoda clean bright daylight, summer blue-green, family warmth, crisp, 2D anime`｜动画/家庭/奇幻
58. 押井守 Mamoru Oshii｜攻壳机动队/天使之卵｜⭐哲思慢节奏·城市空镜蒙太奇·赛博沉思·水与雨意象｜暗调冷峻·赛博绿青·雨湿反光｜人与机器/存在/意识哲学｜`Oshii philosophical slow pace, cyberpunk cityscape montage, rain, contemplative, 2D anime`｜动画/科幻/哲思
59. 庵野秀明 Hideaki Anno｜新世纪福音战士/真实之影｜⭐密集文字定格·凌厉快切·实景质感·意识流留白长镜｜高对比·神学符号·冷暖极端｜心理创伤/孤独/末世/意识剖析｜`Anno rapid text-card cuts, freeze frames, psychological montage, apocalyptic, 2D anime`｜动画/科幻/心理
60. 汤浅政明 Masaaki Yuasa｜恶魔人crybaby/乒乓/春宵苦短｜⭐夸张变形流动作画·超现实·扭曲透视·实验色彩｜大胆撞色·迷幻高饱和·扭曲｜情欲与暴力/生命力/超现实表现｜`Yuasa fluid distorted animation, surreal warped perspective, psychedelic bold color, 2D anime`｜动画/实验/超现实

## 五、AI/技术型·亚洲拓展·纪录片/实验（61–70）

61. 加雷斯·爱德华兹 Gareth Edwards｜AI创世者/哥斯拉/侠盗一号｜⭐巨物渺小人类·低角度仰拍巨像·真实感VFX合成·克制叙描｜自然光·低饱和冷灰·大气迷雾｜科技伦理/人性与巨物/希望微光｜`Gareth Edwards giant beings, tiny human scale, low-angle awe, realistic VFX, atmospheric haze`｜科幻/灾难/巨物
62. 亚历克斯·加兰 Alex Garland｜机械姬/湮灭/美国内战｜冷峻人机对话·镜像反射·极简封闭空间·缓推凝视｜极简白/冷蓝·实验室冷光·自然与合成对撞｜AI意识/身份/自毁/人造与自然｜`Alex Garland clinical AI, mirror reflections, minimalist sci-fi, cold sterile, existential`｜科幻/心理惊悚/哲思
63. 李沧东 Lee Chang-dong｜燃烧/诗/密阳｜自然主义手持·长镜跟随·空镜留白·平实克制｜自然光·低饱和现实·韩国郊野质感｜阶层/愤怒/存在空虚/社会边缘人｜`Lee Chang-dong naturalistic handheld, long takes, muted realism, slow-burn social, poetic restraint`｜剧情/社会/文艺
64. 阿彼察邦·韦拉斯哈古 Apichatpong Weerasethakul｜能召回前世的布米叔叔/记忆/热带疾病｜⭐极慢长镜·丛林自然·超现实与日常并置·静默凝视｜自然光·热带绿色潮湿·朦胧迷离｜灵性/记忆/自然·人性边界｜`Apichatpong slow cinema, tropical jungle, surreal everyday, spiritual, meditative stillness`｜文艺/实验/超现实
65. 阿斯哈·法哈蒂 Asghar Farhadi｜一次别离/推销员/关于伊丽｜⭐道德困境·室内对峙调度·群像式对话·手持跟拍走动｜自然光·写实室内暖调·伊朗日常｜道德灰色/家庭裂痕/谎言与尊严｜`Asghar Farhadi moral dilemma, handheld indoor tracking, ensemble dialogue, social realism`｜剧情/家庭/社会
66. 陈英雄 Tran Anh Hung｜青木瓜之味/三轮车夫/挪威的森林｜慢镜头感官美学·微观特写(食物/触觉)·静谧构图·色彩丰盈｜浓郁东南亚暖调·青绿金黄饱和·热带湿润｜感官记忆/日常生活/人与环境诗意｜`Tran Anh Hung slow-mo sensory, micro close-ups food texture, lush saturated tropical, poetic stillness`｜文艺/感官/东方生活
67. 沃纳·赫尔佐格 Werner Herzog｜陆上行舟/灰熊人/阿基尔·上帝的愤怒｜⭐史诗疯狂·极端实景·不可控自然·人物直视镜头独白｜自然光·原始丛林河流·厚重原始｜人类野心与自然/疯狂边缘/文明与原始｜`Werner Herzog epic madness, extreme real locations, untamed nature, hypnotic monologue, raw`｜纪录片/冒险/剧情
68. 阿涅斯·瓦尔达 Agnès Varda｜拾穗者/五至七时的克莱奥/天涯沦落女｜手持摄像机·街拍/主观介入·拼贴/装置感·自反式旁白｜自然光·明快鲜亮·法式日常色彩｜女性视角/时间/边缘者/生命与死亡｜`Agnès Varda handheld documentary, subjective intervention, collage, feminist, playful warmth`｜纪录片/女性/文艺
69. 弗雷德里克·怀斯曼 Frederick Wiseman｜社会福利/国家美术馆/伯克利｜⭐纯观察式·无旁白无采访·机构空间长镜·剪辑为叙｜自然光·真实环境·不修饰｜制度与人性/权力/群体行为/秩序｜`Frederick Wiseman fly-on-the-wall, no narration, institutional observation, verite long takes`｜纪录片/社会观察
70. 迈克尔·哈内克 Michael Haneke｜爱/白丝带/隐藏摄影机｜⭐固定长镜·冷静行刑式构图·暴力发生在画外·拒绝配乐操纵｜自然冷峻·北欧式低饱和·灰暗｜暴力与媒介/中产暗面/原罪/叙事伦理｜`Michael Haneke static long take, violence off-screen, clinical cold, no manipulative score, unsettling`｜心理/社会/惊悚

## 使用提示
- 风格选用速记：极致色彩→张艺谋/王家卫/阿莫多瓦；对称强迫美→库布里克/韦斯·安德森/兰斯莫斯；冷峻阴郁→芬奇/杜琪峰；自然诗意→马力克/侯孝贤/塔可夫斯基；梦境超现实→林奇/毕赣/今敏/费里尼；暴力浪漫→吴宇森/朴赞郁；霓虹暴力美学→雷弗恩；史诗宏大→维伦纽瓦/诺兰；西部仪式→莱昂内；升格史诗→施奈德；爆炸商业→迈克尔·贝；快剪戏仿→埃德加·赖特/盖·里奇；白昼恐怖→阿里·艾斯特；动画光影天空→新海诚；动画哲思→押井守/庵野秀明。
- 组合调用：导演风格 = 该导演常用「灯光+构图+运镜+色彩」组合，可与对应原子库交叉引用。
- 生图/生视频：把 `模仿提示词` 直接拼入，再叠加题材场景描述即可；动画导演务必前置 `2D anime style`。
- 共70位：国际46（含日本动画5）+ 华语14 + AI/技术型·亚洲·纪录/实验10。
