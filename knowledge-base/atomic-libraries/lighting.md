# 灯光数据库（Lighting Database）

> 原子库 · 共 44 条 ｜ 灯光决定情绪基调，是「同样的画面、不同的灵魂」的关键。
> 本库供模块4（提示词生成器）调用，`视觉关键词` 字段可直接复制进生图/生视频提示词。

## 字段格式
```
布光名称 / 灯位(主·辅·轮廓·背景) / 光质(硬·柔) / 光比 /
色温色调 / 情绪效果 / 适用场景题材 / 经典案例 / 视觉关键词 / 配套构图
```

## 💡 基础概念速查
- **光质：** 硬光=阴影边缘锐利、对比强（裸灯/正午阳光）；柔光=阴影柔和过渡（柔光箱/阴天）。
- **光比：** 主光与暗部的亮度比。低光比=平、明亮；高光比=反差大、戏剧。
- **色温：** 暖（约2700–3500K，橙黄）/ 中性（约5000–5600K，日光）/ 冷（约6500K+，蓝）。
- **三大功能光：** 主光(Key)定明暗与方向；辅光(Fill)补暗部降反差；轮廓光(Back/Rim)勾边分离背景。

---

# 一、经典人像 / 影棚布光（1–12）

## 1. 三点布光（Three-Point Lighting）
- **灯位：** 主光45°侧前方、辅光对侧稍低补暗、轮廓光主体后方勾边
- **光质：** 可硬可柔（通常柔主光）
- **光比：** 中（可调）
- **色温色调：** 中性，按场景调
- **情绪效果：** 标准、立体、干净、可信
- **适用场景题材：** 访谈、对话、通用人物——一切的默认起点
- **经典案例：** 几乎所有标准影视对话镜头
- **视觉关键词：** three-point lighting, key fill and rim light, balanced studio portrait, dimensional
- **配套构图：** 中景/近景，主体居三分线

## 2. 伦勃朗光（Rembrandt Lighting）
- **灯位：** 主光高位45°侧光，暗侧脸颊形成倒三角光斑
- **光质：** 偏硬至中
- **光比：** 较高
- **色温色调：** 暖或中性
- **情绪效果：** 戏剧、深沉、古典、有故事感
- **适用场景题材：** 人物肖像、文艺、历史、深度访谈
- **经典案例：** 古典油画式人物特写
- **视觉关键词：** Rembrandt lighting, triangle of light on cheek, dramatic side key, painterly portrait
- **配套构图：** 近景/特写，暗侧留空

## 3. 蝴蝶光 / 派拉蒙光（Butterfly / Paramount）
- **灯位：** 主光置于相机正上方、朝下打，鼻下形成蝴蝶状对称阴影
- **光质：** 柔
- **光比：** 低至中
- **色温色调：** 中性偏暖
- **情绪效果：** 魅惑、华丽、精致、复古明星感
- **适用场景题材：** 时尚、美妆、女性肖像、老好莱坞风
- **经典案例：** 黄金时代好莱坞明星定妆照
- **视觉关键词：** butterfly lighting, paramount glamour light, symmetrical under-nose shadow, beauty light
- **配套构图：** 正面特写，对称构图

## 4. 环形光（Loop Lighting）
- **灯位：** 主光稍高、偏侧30–45°，鼻侧投下小环形阴影
- **光质：** 柔
- **光比：** 低至中
- **色温色调：** 中性
- **情绪效果：** 自然、亲和、立体而不夸张
- **适用场景题材：** 最通用的人像光，访谈、日常、商业
- **经典案例：** 大量人物宣传照
- **视觉关键词：** loop lighting, small nose shadow, natural flattering portrait
- **配套构图：** 近景，平视

## 5. 分割光（Split Lighting）
- **灯位：** 主光90°正侧，半脸亮半脸暗
- **光质：** 偏硬
- **光比：** 高
- **色温色调：** 中性或冷
- **情绪效果：** 强戏剧、冲突、双面性、神秘
- **适用场景题材：** 悬疑、反派、内心挣扎、双重人格
- **经典案例：** 反派登场的半明半暗脸
- **视觉关键词：** split lighting, half face in shadow, hard side light, dramatic duality
- **配套构图：** 特写，明暗各占一半

## 6. 宽光（Broad Lighting）
- **灯位：** 照亮朝向相机的较宽一侧脸
- **光质：** 柔
- **光比：** 低
- **色温色调：** 中性
- **情绪效果：** 开朗、显脸宽、健康
- **适用场景题材：** 高调人像、需要显饱满/亲和的角色
- **经典案例：** 喜剧/广告人物
- **视觉关键词：** broad lighting, wider side of face lit, open friendly look
- **配套构图：** 近景，略侧脸

## 7. 窄光 / 短光（Short Lighting）
- **灯位：** 照亮背离相机的较窄一侧脸，宽侧入暗
- **光质：** 中
- **光比：** 中至高
- **色温色调：** 中性
- **情绪效果：** 显瘦、立体、戏剧、精致
- **适用场景题材：** 大多数电影人像、塑造轮廓
- **经典案例：** 电影级人物近景
- **视觉关键词：** short lighting, far side of face lit, slimming dimensional portrait
- **配套构图：** 近景/特写，侧脸

## 8. 顶光（Top Lighting）
- **灯位：** 光从正上方垂直向下
- **光质：** 硬
- **光比：** 高（眼窝、鼻下深阴影）
- **色温色调：** 中性或冷
- **情绪效果：** 压迫、孤立、审视、神性或恐怖
- **适用场景题材：** 审讯、孤独、宗教神性、惊悚
- **经典案例：** 审讯室头顶吊灯
- **视觉关键词：** top lighting, overhead light, deep eye sockets shadow, oppressive
- **配套构图：** 俯拍或平视，主体居中孤立

## 9. 底光 / 脚光（Under Lighting）
- **灯位：** 光从下方向上打（反自然方向）
- **光质：** 硬
- **光比：** 高
- **色温色调：** 冷或诡异绿/橙（火）
- **情绪效果：** 诡异、恐怖、邪恶、不安
- **适用场景题材：** 鬼怪、恐怖、营火讲鬼故事、反派变身
- **经典案例：** 手电筒打脸讲鬼故事
- **视觉关键词：** under lighting, uplight from below, eerie horror face, ghoulish
- **配套构图：** 特写，仰角

## 10. 轮廓光 / 逆光（Rim / Back Lighting）
- **灯位：** 光在主体后方，勾出边缘亮线，与背景分离
- **光质：** 硬（勾边）
- **光比：** 视主体正面补光而定
- **色温色调：** 任意，常用冷边缘
- **情绪效果：** 氛围、神圣、神秘、立体分离
- **适用场景题材：** 出场、回忆、神性、烟雾环境
- **经典案例：** 烟雾中逆光登场的人影
- **视觉关键词：** rim light, backlight halo, edge separation light, glowing outline
- **配套构图：** 中景，主体前留暗

## 11. 高调（High-Key）
- **灯位：** 多柔光均匀铺满，辅光强、阴影极少
- **光质：** 柔
- **光比：** 极低
- **色温色调：** 中性偏亮
- **情绪效果：** 轻松、明亮、纯净、梦幻、乐观
- **适用场景题材：** 喜剧、广告、MV、爱情、梦境、医疗科技
- **经典案例：** 明亮纯白的广告画面
- **视觉关键词：** high-key lighting, bright low-contrast, minimal shadows, airy clean
- **配套构图：** 留白多，背景明亮

## 12. 低调（Low-Key）
- **灯位：** 主光为主、辅光极弱或无，大面积暗
- **光质：** 硬
- **光比：** 极高
- **色温色调：** 中性或冷
- **情绪效果：** 压抑、神秘、危险、孤独、紧张
- **适用场景题材：** 黑色电影、悬疑、惊悚、犯罪、深夜
- **经典案例：** 黑色电影侦探独坐暗室
- **视觉关键词：** low-key lighting, deep shadows, high contrast, single source, moody dark
- **配套构图：** 大面积阴影，主体局部受光

---

# 二、自然光与时间光（13–20）

## 13. 黄金时刻（Golden Hour）
- **灯位：** 日出后/日落前的低角度自然侧逆光
- **光质：** 柔暖
- **光比：** 中（长柔影）
- **色温色调：** 暖金橙
- **情绪效果：** 浪漫、温暖、怀旧、希望、史诗
- **适用场景题材：** 爱情、回忆、结局、公路、青春
- **经典案例：** 夕阳下的拥抱/奔跑
- **视觉关键词：** golden hour, warm low sun, long soft shadows, sunset glow, magic hour
- **配套构图：** 逆光剪影或暖边缘光

## 14. 蓝调时刻（Blue Hour）
- **灯位：** 日落后天空均匀冷调散射光
- **光质：** 柔
- **光比：** 低
- **色温色调：** 深蓝冷调
- **情绪效果：** 忧郁、宁静、孤独、过渡感
- **适用场景题材：** 离别、深夜来临、城市黄昏、文艺
- **经典案例：** 暮色城市天际线
- **视觉关键词：** blue hour, twilight, deep blue ambient, dusk, melancholic calm
- **配套构图：** 配实用暖光点缀冷调

## 15. 正午硬光（Harsh Midday Sun）
- **灯位：** 头顶强直射阳光
- **光质：** 极硬
- **光比：** 高（短硬阴影）
- **色温色调：** 中性偏冷白
- **情绪效果：** 残酷、燥热、暴露、纪实、紧张
- **适用场景题材：** 西部、战争、纪录片、荒漠、对峙
- **经典案例：** 正午荒漠对决
- **视觉关键词：** harsh midday sun, hard overhead light, deep short shadows, blown highlights, arid
- **配套构图：** 高反差，强烈明暗

## 16. 阴天柔光（Overcast Soft Light）
- **灯位：** 云层全向散射，无明显方向
- **光质：** 极柔
- **光比：** 极低
- **色温色调：** 中性偏冷
- **情绪效果：** 平静、写实、阴郁、压抑、文艺
- **适用场景题材：** 文艺片、阴郁剧情、写实、北欧风
- **经典案例：** 阴天里的日常生活流
- **视觉关键词：** overcast soft light, diffused even lighting, no harsh shadows, muted grey sky
- **配套构图：** 低饱和，均匀曝光

## 17. 月光（Moonlight）
- **灯位：** 高位冷蓝低照度模拟月光，常带轮廓
- **光质：** 柔至中
- **光比：** 高（暗背景）
- **色温色调：** 冷蓝
- **情绪效果：** 神秘、浪漫、孤寂、危险、梦幻
- **适用场景题材：** 夜戏、爱情夜、恐怖、潜行
- **经典案例：** 月夜窗边的剪影
- **视觉关键词：** moonlight, cool blue night, soft moon glow, silvery rim, nocturnal
- **配套构图：** 低调，蓝调暗场

## 18. 窗光（Window Light）
- **灯位：** 侧向大面积柔光（来自窗户），自然渐变
- **光质：** 柔
- **光比：** 中
- **色温色调：** 日光或暖（晨/暮）
- **情绪效果：** 生活感、亲密、宁静、真实
- **适用场景题材：** 室内剧、家庭、亲密对话、文艺
- **经典案例：** 窗边阅读/对坐的柔光
- **视觉关键词：** soft window light, directional natural light, gentle falloff, intimate interior
- **配套构图：** 侧光，靠窗布置主体

## 19. 丁达尔 / 上帝之光（God Rays / Volumetric Beams）
- **灯位：** 强光穿过雾/尘/缝隙，形成可见光束
- **光质：** 硬束
- **光比：** 高
- **色温色调：** 暖（阳光）或冷（窗）
- **情绪效果：** 神圣、希望、震撼、超脱、救赎
- **适用场景题材：** 教堂、森林晨雾、神迹、转折高光
- **经典案例：** 教堂彩窗射入的光柱
- **视觉关键词：** god rays, volumetric light beams, sunbeams through fog, crepuscular rays, divine light
- **配套构图：** 逆光，光束斜贯画面

## 20. 逆光剪影（Silhouette Backlight）
- **灯位：** 强背光，主体正面不补光
- **光质：** 任意（强背光）
- **光比：** 极高（主体全黑）
- **色温色调：** 视背景而定
- **情绪效果：** 神秘、悬念、艺术、隐藏身份、情绪化
- **适用场景题材：** 神秘登场、隐藏反派、艺术抒情、谢幕
- **经典案例：** 门口逆光的黑影身形
- **视觉关键词：** silhouette, strong backlight, subject in shadow, dramatic outline, mysterious figure
- **配套构图：** 主体纯黑，背景亮

---

# 三、氛围与风格化光（21–29）

## 21. 霓虹光（Neon Lighting）
- **灯位：** 画面内多彩人造光源（招牌/灯带），多向混色
- **光质：** 中至柔
- **光比：** 中（彩色高光）
- **色温色调：** 高饱和粉/青/紫/品红混色
- **情绪效果：** 迷离、暧昧、都市、潮酷、堕落
- **适用场景题材：** 赛博朋克、都市夜、夜店、犯罪、MV
- **经典案例：** 雨夜霓虹街头
- **视觉关键词：** neon lighting, pink and cyan glow, wet street reflections, cyberpunk city night
- **配套构图：** 暗场+彩色光斑，潮湿反光

## 22. 烛光 / 火光（Candle / Firelight）
- **灯位：** 低位点光源，近距快速衰减、自然摇曳
- **光质：** 柔（近）
- **光比：** 高（边缘速暗）
- **色温色调：** 极暖橙
- **情绪效果：** 亲密、古典、温暖、危险（火）、虔诚
- **适用场景题材：** 古装、烛光晚餐、祈祷、篝火、停电
- **经典案例：** 烛光中的密谈
- **视觉关键词：** candlelight, warm flickering glow, firelight, intimate amber light, soft falloff
- **配套构图：** 近景，光源入画

## 23. 实用光源（Practical Lights）
- **灯位：** 画面内可见的真实灯具（台灯/路灯/招牌/手机）即光源
- **光质：** 视灯具而定
- **光比：** 中至高
- **色温色调：** 混合（暖灯+冷屏等）
- **情绪效果：** 真实、沉浸、有动机、生活质感
- **适用场景题材：** 现实主义、室内、夜景、自然主义
- **经典案例：** 只靠台灯照明的书房夜戏
- **视觉关键词：** practical lights, motivated light sources, lamp in frame, naturalistic mixed lighting
- **配套构图：** 光源入画，明暗自然分布

## 24. 赛博朋克双色光（Teal–Orange / Cyan–Magenta）
- **灯位：** 冷暖两色光从两侧对撞打主体
- **光质：** 中
- **光比：** 中（彩色对比）
- **色温色调：** 一冷一暖强对撞
- **情绪效果：** 风格化、科幻、潮酷、张力、未来
- **适用场景题材：** 科幻、MV、潮流广告、动作大片
- **经典案例：** 双色光勾勒的人物近景
- **视觉关键词：** teal and orange, dual color lighting, cyan magenta rim, stylized sci-fi color contrast
- **配套构图：** 两侧彩色边缘光，暗中调

## 25. 黑色电影百叶窗光（Film Noir Venetian Blinds）
- **灯位：** 硬光透过百叶窗投下平行条状阴影
- **光质：** 硬
- **光比：** 极高
- **色温色调：** 中性偏冷，黑白感
- **情绪效果：** 宿命、囚禁、悬疑、危险、压抑
- **适用场景题材：** 黑色电影、侦探、犯罪、审讯、出轨
- **经典案例：** 侦探办公室的百叶窗条纹
- **视觉关键词：** film noir, venetian blind shadows, hard slatted light, chiaroscuro, dramatic stripes
- **配套构图：** 条纹阴影横切人脸/墙

## 26. 屏幕冷光（Screen / TV Glow）
- **灯位：** 来自屏幕方向的闪烁冷光打脸
- **光质：** 柔
- **光比：** 高（暗环境）
- **色温色调：** 冷蓝，闪动
- **情绪效果：** 孤独、空虚、现代、沉迷、深夜
- **适用场景题材：** 深夜独处、网瘾、监控、现代都市
- **经典案例：** 黑暗中被电视/手机照亮的脸
- **视觉关键词：** screen glow, flickering cool blue light on face, TV light in dark room, lonely modern
- **配套构图：** 暗场，单面冷光

## 27. 警灯红蓝（Police / Emergency Lights）
- **灯位：** 交替红蓝频闪从侧/外打入
- **光质：** 硬，闪动
- **光比：** 高，节律变化
- **色温色调：** 强红与强蓝交替
- **情绪效果：** 紧急、危机、犯罪、不安、混乱
- **适用场景题材：** 案发现场、追捕、事故、犯罪剧
- **经典案例：** 夜间案发现场的红蓝闪烁
- **视觉关键词：** police lights, alternating red and blue flashing, emergency strobe, crime scene
- **配套构图：** 暗夜，红蓝交替扫过

## 28. 体积光 / 雾光（Volumetric / Atmospheric Fog）
- **灯位：** 光在雾气/烟尘中可见，制造层次与纵深
- **光质：** 任意（雾中漫射）
- **光比：** 中至高
- **色温色调：** 任意，常冷
- **情绪效果：** 梦境、悬疑、史诗、神秘、不安
- **适用场景题材：** 恐怖、奇幻、战场、梦境、悬疑
- **经典案例：** 雾中手电光柱的搜索
- **视觉关键词：** volumetric lighting, atmospheric fog, hazy light beams, misty depth, smoky ambiance
- **配套构图：** 前后景分层，光雾纵深

## 29. 明暗对比法（Chiaroscuro）
- **灯位：** 单一硬光源，极端明暗对比（卡拉瓦乔式）
- **光质：** 硬
- **光比：** 极高
- **色温色调：** 暖或中性，油画感
- **情绪效果：** 古典、戏剧、庄重、宗教、油画美
- **适用场景题材：** 历史、宗教、艺术、悲剧、肖像
- **经典案例：** 油画式单光人物
- **视觉关键词：** chiaroscuro, single hard light source, extreme light-dark contrast, baroque painterly
- **配套构图：** 主体受光，余皆没入暗

---

# 四、情绪与功能光（30–36）

## 30. 暖调家庭光（Warm Domestic）
- **灯位：** 多个暖色实用灯均匀柔照
- **光质：** 柔
- **光比：** 低
- **色温色调：** 暖橙黄
- **情绪效果：** 温馨、安全、怀旧、幸福、放松
- **适用场景题材：** 家庭、团聚、节日、童年、治愈
- **经典案例：** 一家人围坐的暖光客厅
- **视觉关键词：** warm domestic lighting, cozy amber glow, homey inviting interior, soft warm tone
- **配套构图：** 暖色满铺，柔和

## 31. 冷调惊悚（Cold Thriller）
- **灯位：** 整体降饱和偏青蓝、硬阴影
- **光质：** 硬
- **光比：** 高
- **色温色调：** 冷青蓝、低饱和
- **情绪效果：** 冷峻、疏离、不安、犯罪、理性冷酷
- **适用场景题材：** 犯罪、悬疑、科技惊悚、太平间、监狱
- **经典案例：** 冷蓝调的犯罪现场
- **视觉关键词：** cold thriller lighting, desaturated teal blue, hard shadows, clinical cold, bleak
- **配套构图：** 冷色调，硬边阴影

## 32. 边缘勾边光（Kicker / Edge Light）
- **灯位：** 后侧45°的边缘光，沿主体轮廓勾亮线
- **光质：** 硬
- **光比：** 视正面补光而定
- **色温色调：** 任意，常与主光异色
- **情绪效果：** 立体、精致、人物突出、电影感
- **适用场景题材：** 人物特写、高级感、海报感镜头
- **经典案例：** 人物轮廓被边缘光勾出
- **视觉关键词：** kicker light, edge rim on subject, hair light, cinematic separation, glowing contour
- **配套构图：** 近景，主体与暗背景分离

## 33. 平光 / 正面光（Flat / Frontal）
- **灯位：** 光与镜头同轴，正面平打
- **光质：** 柔
- **光比：** 极低（几无阴影）
- **色温色调：** 中性
- **情绪效果：** 扁平、客观、纪实、亦可时尚纯净
- **适用场景题材：** 证件式、纪实、新闻、时尚平光美
- **经典案例：** 正面无影的纪实肖像
- **视觉关键词：** flat frontal lighting, on-axis light, shadowless, documentary, even beauty light
- **配套构图：** 正面，对称

## 34. 高反差侧光（High-Contrast Side）
- **灯位：** 强侧光，半脸明半脸入暗
- **光质：** 硬
- **光比：** 高
- **色温色调：** 中性或冷
- **情绪效果：** 硬朗、内心挣扎、男性气质、张力
- **适用场景题材：** 硬汉、独白、抉择、人物深度刻画
- **经典案例：** 半脸入暗的内心独白特写
- **视觉关键词：** high-contrast side light, half-lit face, strong directional key, brooding intensity
- **配套构图：** 特写，明暗对半

## 35. 摇曳火光闪烁（Flickering Light）
- **灯位：** 不稳定闪动暖光（火/故障灯/爆炸余光）
- **光质：** 硬，强弱跳动
- **光比：** 动态变化
- **色温色调：** 暖橙（火）或冷（故障灯）
- **情绪效果：** 不安、危险、恐怖、临场、混乱
- **适用场景题材：** 火灾、恐怖、废墟、停电、战场
- **经典案例：** 火光忽明忽暗映照的脸
- **视觉关键词：** flickering firelight, unstable strobing glow, pulsing warm light, ominous flicker
- **配套构图：** 暗场，光强律动变化

## 36. 发际光 / 顶逆光（Hair Light）
- **灯位：** 高后位专打头发与肩部，勾出轮廓
- **光质：** 中至硬
- **光比：** 局部高光
- **色温色调：** 中性或冷边
- **情绪效果：** 精致、立体、与背景分离、高级
- **适用场景题材：** 人像、时尚、访谈、需突出主体
- **经典案例：** 头发被勾亮的精致近景
- **视觉关键词：** hair light, top-back separation light, glowing hair rim, polished portrait
- **配套构图：** 近景，主体浮出暗背景

---

# 五、特殊与场景光（37–44）

## 37. 舞台演唱会动感光（Concert / Stage Moving Lights）
- **布光位置：** 多向摇头灯、追光、激光、逆向烟雾光束，机位多角度
- **光质：** 高强度硬光束 + 烟雾体积感，动态扫射变换
- **明暗对比：** 极高对比，光束切割黑暗
- **色温色彩：** 高饱和炫彩（红蓝紫绿），随节拍变色
- **塑形效果：** 光束扫射、频闪、追光锁定，能量四射
- **情绪氛围：** 亢奋、狂热、炫目、能量、躁动、盛典
- **适用场景：** 演唱会、夜店、舞台、电音节、颁奖礼、MV
- **经典案例：** 烟雾中激光与摇头灯束随鼓点扫射全场
- **视觉关键词：** concert stage lights, moving head beams, lasers, haze, strobing, vibrant
- **AI提示词：** `concert stage lighting, sweeping moving-head beams and lasers through haze, vibrant strobing colors, energetic`
- **风险提示：** 光束需烟雾才有体积感；频闪注意光敏；忌乱无节拍

## 38. 水面焦散波光（Water Caustics）
- **布光位置：** 光线透过/反射水面，在主体与环境投下流动波纹光
- **光质：** 流动的网状波光（caustics），柔中带闪动
- **明暗对比：** 中等，波光在暗背景上游移
- **色温色彩：** 多偏碧蓝/青绿（泳池/海），或暖金（夕照水面）
- **塑形效果：** 主体表面爬满流动的水纹光斑，梦幻浮动
- **情绪氛围：** 梦幻、宁静、清凉、失重、潜意识、唯美
- **适用场景：** 泳池、水下、海边、浴室、梦境、回忆、水族馆
- **经典案例：** 泳池边人物身上爬满流动的蓝色波纹光
- **视觉关键词：** water caustics, rippling reflected light, pool light patterns, shimmering
- **AI提示词：** `water caustics light, rippling reflections dancing over subject, aqua tones, dreamy shimmering`
- **风险提示：** 波纹需"流动感"，AI 易做成静态；与水体场景配合

## 39. 投影图案光 Gobo（Dappled / Pattern Light）
- **布光位置：** 光源透过镂空物（树叶/栅格/百叶/花窗/水纹片）投出图案
- **光质：** 带图案的斑驳光影（树影/格栅/光斑）
- **明暗对比：** 中高，图案明暗交织
- **色温色彩：** 随场景，常自然光或暖光
- **塑形效果：** 主体与墙面爬满斑驳图案，增层次与氛围
- **情绪氛围：** 斑驳诗意、慵懒、禁锢（栅格）、自然、神秘、复古
- **适用场景：** 树荫下、百叶窗、监狱栅格、教堂花窗、林间、慵懒午后
- **经典案例：** 树影斑驳洒在午睡人物脸上
- **视觉关键词：** gobo pattern light, dappled leaf shadows, window grid shadow, textured light
- **AI提示词：** `dappled gobo lighting, leaf-shadow patterns over subject and wall, textured atmospheric shadows`
- **风险提示：** 与百叶窗光(25)区分在"图案多样"；图案别盖过主体

## 40. 闪电雷暴光（Lightning Flash）
- **布光位置：** 强冷光从窗/外部瞬间爆闪，伴随短暂全亮再回暗
- **光质：** 极强冷硬瞬闪，几帧爆亮
- **明暗对比：** 极端（暗→瞬间惨白→暗）
- **色温色彩：** 惨白冷蓝，幽冷
- **塑形效果：** 瞬间照亮全场/剪影，定格惊悚一刻
- **情绪氛围：** 惊悚、危机、不安、震撼、暴烈、宿命
- **适用场景：** 雷暴夜、恐怖、惊悚、悬疑、戏剧高潮、揭示
- **经典案例：** 闪电瞬间照亮窗边伫立的黑影
- **视觉关键词：** lightning flash, sudden cold strobe through window, stark silhouette, stormy
- **AI提示词：** `lightning flash lighting, sudden stark cold-blue burst through window, dramatic silhouettes, stormy night`
- **风险提示：** 配雷声才成立；闪频注意光敏；爆闪时长把握

## 41. 反弹 / 柔板补光（Bounce / Reflector Fill）
- **布光位置：** 主光经反光板/墙面/地面反弹回填阴影侧
- **光质：** 极柔的二次反射光，无硬影
- **明暗对比：** 低，柔和填充暗部
- **色温色彩：** 随反射面（白板中性/金板暖/银板冷）
- **塑形效果：** 柔化阴影、降低反差、提亮暗部细节，自然通透
- **情绪氛围：** 自然、柔和、真实、舒适、亲和
- **适用场景：** 访谈、人像、自然光补光、纪录片、日常写实、美妆广告
- **经典案例：** 逆光人物面部用反光板补出柔亮
- **视觉关键词：** bounce light, reflector fill, soft shadow fill, natural soft lighting
- **AI提示词：** `soft bounce fill light, reflector filling shadows, low contrast natural flattering light`
- **风险提示：** 这是"技术补光"，重在自然降反差；过度则平淡无立体

## 42. 彩色凝胶氛围光（Color Gel Wash）
- **布光位置：** 加色片的光从侧/背/双向打出，染色环境与主体
- **光质：** 浓郁染色光，可双色对撞
- **明暗对比：** 中高，色彩边界分明
- **色温色彩：** 强烈单色或撞色（品红+青、红+蓝、橙+紫）
- **塑形效果：** 主体被双色光勾勒，半脸异色，时尚张力
- **情绪氛围：** 时尚、迷离、戏剧、张力、潮流、躁动或暧昧
- **适用场景：** MV、时尚大片、夜店、人像、海报、潮流广告
- **经典案例：** 人物左脸品红右脸青蓝的撞色染光
- **视觉关键词：** color gel lighting, dual-color wash, magenta and cyan, bold colored light
- **AI提示词：** `color gel lighting, dual-tone magenta-and-cyan wash, bold stylized colored light, fashion mood`
- **风险提示：** 与霓虹(21)区分在"凝胶染色"；撞色要有设计别脏

## 43. 节日 / 烟花彩光（Festive / Fireworks Light）
- **布光位置：** 烟花/彩灯/灯笼/圣诞灯等点状彩光源散布，主体受其映照
- **光质：** 点状闪烁彩光 + 偶发烟花强闪
- **明暗对比：** 中，暗夜中点点彩光
- **色温色彩：** 多彩暖闪（金红绿）、烟花瞬间染色
- **塑形效果：** 主体被节日彩光映照、烟花照亮仰望的脸
- **情绪氛围：** 欢庆、温暖、浪漫、热闹、希望、团圆
- **适用场景：** 节日、跨年、烟花、婚礼、圣诞、庙会、浪漫告白
- **经典案例：** 烟花绽放映亮两人仰望的脸
- **视觉关键词：** festive lights, fireworks glow, bokeh string lights, colorful celebration
- **AI提示词：** `festive lighting, fireworks illuminating upturned faces, colorful bokeh string lights, warm celebratory`
- **风险提示：** 烟花映照需"明灭变化"；彩灯光斑增氛围

## 44. 探照灯 / 聚光束（Searchlight / Spotlight Beam）
- **布光位置：** 强方向性光束从远处扫射或单束聚打主体
- **光质：** 极强硬光束，体积感强（需烟雾/雾气）
- **明暗对比：** 极高，光束外即黑暗
- **色温色彩：** 冷白/暖金，单束纯净
- **塑形效果：** 单束锁定主体（舞台聚光）或扫射搜寻（探照），强戏剧聚焦
- **情绪氛围：** 聚焦、审视、追捕、孤立、表演、神圣或压迫
- **适用场景：** 越狱搜捕、舞台独唱、审讯、孤独独白、逃亡、聚焦时刻
- **经典案例：** 探照灯光柱在夜空扫射搜寻逃犯
- **视觉关键词：** searchlight beam, single spotlight, volumetric light shaft, isolating spotlight
- **AI提示词：** `searchlight / spotlight beam, strong volumetric light shaft through haze, isolating the subject, dramatic`
- **风险提示：** 光束需烟雾显形；与丁达尔(19)区分在"人造强方向束"

---

---

# 六、科幻与心理光（45–52）

## 45. 全息投影光（Holographic Projection Glow）
- **布光位置：** 全息投影仪或AR界面向主体及环境发射半透明光幕、数据流光点从投影面散射
- **光质：** 半透明叠加光幕，粒子感闪烁，柔中带数码颗粒
- **明暗对比：** 中低对比，光幕与环境共存
- **色温色彩：** 冰蓝/青绿/淡紫/湖蓝半透明色，闪烁粒子白
- **塑形效果：** 主体被半透明数据光幕包裹或穿行其中、光点飘浮于空间
- **情绪氛围：** 未来、科技、超现实、数字化、虚拟与现实交融
- **适用场景：** 科幻、赛博朋克、高科技实验室、虚拟会议、AR增强现实
- **经典案例：** 全息通讯中人物被蓝色半透明光幕笼罩，数据流从指尖流过
- **视觉关键词：** holographic projection, translucent light screen, floating data particles, sci-fi overlay, AR glow
- **AI提示词：** `holographic lighting, translucent data light curtain enveloping subject, floating blue particles, sci-fi augmented reality glow`
- **风险提示：** 半透明光勿遮挡主体五官；数据流粒子过多成噪点

## 46. 能量核心光（Energy Core / Reactor Glow）
- **布光位置：** 核心光源位于主体中央(如胸口/武器/驾驶舱)，向外辐射脉冲光波
- **光质：** 脉冲硬光，以核心为心向四周辐射、强弱交替
- **明暗对比：** 极高(核心爆亮→边缘骤暗)
- **色温色彩：** 橙金/蓝白/紫红/绿核，光线随脉冲变色
- **塑形效果：** 主体被中央能量核心照亮、脉冲光斑从核心向外扩散、设备/环境被光波扫过
- **情绪氛围：** 能量充盈、临界爆发、科技神圣、危机前兆
- **适用场景：** 科幻、机甲、超级英雄、魔幻核心、能源舱启动、自毁倒计时
- **经典案例：** 机甲胸口反应堆脉冲发光，光波一波波扫过驾驶舱
- **视觉关键词：** energy core glow, pulsating reactor light, radial power waves, surging sci-fi power, plasma glow
- **AI提示词：** `pulsating energy core, radial light waves from center, intense reactor glow, surging sci-fi plasma, light rippling outward`
- **风险提示：** 脉冲频率过快引发光敏安全；核心亮度需有呼吸节奏

## 47. 驾驶舱界面光（Cockpit / HUD Interface Glow）
- **布光位置：** 多个显示屏/仪表/HUD从多方向投射冷调界面光在驾驶员脸上及舱内
- **光质：** 多源不规则硬光闪动，随仪表信息变化
- **明暗对比：** 中高，暗舱中多源亮屏
- **色温色彩：** 仪表绿/橙/蓝/红多色，冷调为主
- **塑形效果：** 驾驶者面部被多源仪表光从不同方向照亮、数据在脸庞上流动、舱内设备灯光闪烁
- **情绪氛围：** 紧张、专注、科技感、危机操控、孤寂飞行
- **适用场景：** 科幻、太空、飞行、潜艇、指挥中心、机甲驾驶
- **经典案例：** 太空中飞行员脸庞被绿色HUD和橙色警报灯交替照亮
- **视觉关键词：** cockpit lighting, HUD glow on face, multi-source instrument lights, sci-fi pilot, dashboard glow
- **AI提示词：** `cockpit instrument lighting, HUD green glow on pilot face, flickering multi-colored dashboard lights, immersive sci-fi cockpit`
- **风险提示：** 多源光方向统一(每屏对应一侧)；脸上光彩勿杂色腥

## 48. 生化变异光（Bioluminescent / Mutagenic Glow）
- **布光位置：** 光从生命体内部或表面渗出(血脉/菌丝/腺体)、在身体与环境中蔓延
- **光质：** 生物自发光，柔且不稳定细脉流淌
- **明暗对比：** 中，暗环境自发光
- **色温色彩：** 荧绿/磷光青/紫红/橙黄(菌变)、蓝(深海)、金(神性)
- **塑形效果：** 生物发光线条沿血脉/纹理蔓延、孢子/发光线缕环绕主体、暗处自体发光
- **情绪氛围：** 异变、恐怖、美丽而致命、超自然、神秘生命
- **适用场景：** 科幻变异、生化危机、深海生物、奇幻精灵、毒液/寄生
- **经典案例：** 感染者手臂上绿色荧光血管纹路从指尖向心脏蔓延
- **视觉关键词：** bioluminescent glow, vein glow, mutagenic blue light, fungal spore light, organic self-illumination
- **AI提示词：** `bioluminescent lighting, glowing veins creeping across skin, ethereal green-blue organic glow, supernatural self-illumination`
- **风险提示：** 生物发光流线要有"生长/蔓延"动势，忌静态贴图；颜色别太霓虹失真实

## 49. 时间停滞光（Time-Freeze Desaturation）
- **布光位置：** 光固定在停帧瞬间，环境降饱和度+轻微欠曝，主体局部保留全彩
- **光质：** 静止、凝固、抽去活力的平光
- **明暗对比：** 低，画面整体降压暗
- **色温色彩：** 去饱和度偏灰蓝或灰褐，主体保留原色
- **塑形效果：** 环境色彩褪去如定格、主体在灰色世界中保持色彩、飘浮尘埃凝固
- **情绪氛围：** 暂停、回忆凝固、重大抉择瞬间、濒死体验、超能力
- **适用场景：** 时间操纵、闪回定格、子弹时间、超英能力、临终回光
- **经典案例：** 爆炸碎片凝固在空中，主角从降饱和的定格画面中穿行
- **视觉关键词：** time-freeze lighting, desaturated frozen moment, color isolation on subject, suspended in time, bullet-time stillness
- **AI提示词：** `time-freeze effect, environment desaturated and still, subject keeps full color in gray world, suspended moment, surreal frozen time`
- **风险提示：** 与高调(11)区分在"全场景去色+主体留色"；不要混用降饱和与暖调

## 50. 恐惧扭曲光（Fear Distortion Lighting）
- **布光位置：** 光从非现实方向(如地底/天花板外)强行扭曲打入，光源不明
- **光质：** 极度异化——硬光但来源不明、束色畸变、暗处拉扯如黑洞
- **明暗对比：** 极端并扭曲，亮部过曝边缘渗黑光
- **色温色彩：** 阴冷绿/暗紫/苍白黄/不祥青灰、暗部渗入深红
- **塑形效果：** 环境扭曲如透镜畸变、阴影不按物理拉长、主体被异常光斑凝视、光源从不该有光的位置打出
- **情绪氛围：** 极致恐惧、心理崩塌、超自然邪恶、精神失常、梦魇
- **适用场景：** 心理恐怖、克苏鲁、精神病幻觉、超自然、极端惊悚、地狱景象
- **经典案例：** 走廊灯光在主角身后扭曲拉长、阴影如触手爬向脚边
- **视觉关键词：** fear distortion light, unnatural shadow pulling, impossible light source, lens warp dread, psychological horror glow
- **AI提示词：** `distorted horror lighting, shadows stretching unnaturally, impossible source of sickly green light, warped perspective, unsettling dream-logic glow`
- **风险提示：** 恐怖光在"违反光物理"——但必须有逻辑底线，忌纯抽象噪点

## 51. 迷幻意识流光（Psychedelic Stream of Consciousness）
- **布光位置：** 多色光带/光丝从主体头部/环境中旋转穿梭，如意识可视化
- **光质：** 流体、光丝、拖尾、光斑溶解，离散而流动
- **明暗对比：** 低至中，梦幻溶解感
- **色温色彩：** 超饱和霓虹七彩、高亮品红/紫/金/青绿、颜色在流动中渐变
- **塑形效果：** 光丝如思维从主体头部旋出、颜色随情绪变化流淌、世界溶解为光流
- **情绪氛围：** 迷幻、意识开悟、药物影响、精神共鸣、超验体验
- **适用场景：** 致幻、冥想、脑机接口、潜意识旅程、艺术实验片
- **经典案例：** 主角闭目后彩色光丝从太阳穴喷出，织成流动的记忆画面
- **视觉关键词：** psychedelic light trails, consciousness stream glow, rainbow fluid light, melting color, drug-trip visual
- **AI提示词：** `psychedelic lighting, fluid rainbow light trails weaving through space, consciousness visualized as glowing ribbons, surreal color flow`
- **风险提示：** 流动有方向(思维→画面)，忌随机噪点；饱和度高但光量适度

## 52. 闪回记忆褪色光（Flashback / Memory Fade Light）
- **布光位置：** 回忆段画面整体褪色，边缘漫出柔光晕(过曝边缘)，进出有光过渡
- **光质：** 柔光漫射+边缘过曝(光晕)，画面如被时间洗白
- **明暗对比：** 低，画面整体提亮、边缘光晕渐隐
- **色温色彩：** 褪暖(茶黄/老照片棕)或褪青(旧胶片青)，过渡区高调白
- **塑形效果：** 画面边角被柔光晕吞没、整体褪色如旧照、光线从外部漫入标记记忆的边界
- **情绪氛围：** 怀旧、不真实、美好但不持久、伤痛被时间淡化
- **适用场景：** 回忆杀、闪回、逝者遗像、旧时光、创伤记忆
- **经典案例：** 画面边缘柔白光晕渐漫，回忆场景褪成茶黄色旧照片质感
- **视觉关键词：** memory fade lighting, vintage photo tone, edge soft white glow, time-washed nostalgic, flashback visual
- **AI提示词：** `memory fade lighting, edges dissolving into soft white glow, sepia-toned nostalgic warmth, dream-like washed-out look, time-softened edges`
- **风险提示：** 褪色+光晕不同于"失焦"(18)；边缘光晕区域不宜过大吞没信息

## 使用提示
- **情绪选光速记：** 温馨→暖调家庭光；悬疑→低调/百叶窗；浪漫→黄金时刻/烛光；恐怖→底光/闪烁/雾光；潮酷→霓虹/双色；孤独→屏幕冷光/月光。
- **可叠加：** 一个镜头常是「主布光 + 实用光 + 氛围光」组合（如：低调 + 霓虹实用光 + 雾光）。
- **生视频时：** 把 `视觉关键词` 直接拼入提示词，并配合「运镜库 + 景别库」组装成完整镜头方案。
- 本库共 **52 条**：经典布光12 + 自然时间光8 + 风格氛围光9 + 情绪功能光7 + 特殊与场景光8（舞台动感/水面焦散/Gobo投影/闪电/反弹补光/彩色凝胶/节日烟花/探照灯束）+ 科幻与心理光8（全息投影/能量核心/驾驶舱/生化变异光/时间停滞/恐惧扭曲/迷幻意识流/闪回记忆）。
