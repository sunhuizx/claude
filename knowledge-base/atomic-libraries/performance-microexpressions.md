# 表演数据库 · 微表情（Performance / Micro-Expressions）

> 原子库 · 目标 ~69 条 ｜ 底层依据：**FACS 面部动作编码系统**（Action Unit, AU）。
> 铁律：任何情绪都**禁止直接写情绪词**，必须翻译成「镜头能拍到的肌肉微动」。本库就是这套「情绪→肌肉」的翻译字典，直接供模块4（提示词生成器）调用。

## 字段格式
```
情绪名称 / 强度等级 / 面部分解(眉·眼·眼睑·鼻翼·嘴角·下颌·喉结) /
FACS动作单元(AU) / 肢体语言 / 呼吸与声音特征 /
持续时间(微表情<0.5s / 宏表情) / 易混淆情绪区分 / 视觉关键词 / 表演案例
```

## AU 速查（常用面部动作单元）
| AU | 含义 | AU | 含义 |
|---|---|---|---|
| AU1 | 眉内角上提 | AU12 | 嘴角上拉（笑） |
| AU2 | 眉外角上提 | AU14 | 嘴角收紧（酒窝/假笑） |
| AU4 | 皱眉/眉下压 | AU15 | 嘴角下拉 |
| AU5 | 上眼睑上提（睁大） | AU17 | 下巴上提 |
| AU6 | 脸颊上提（真笑/眼周） | AU20 | 嘴角水平拉伸（恐惧） |
| AU7 | 眼睑收紧 | AU23 | 双唇收紧 |
| AU9 | 皱鼻 | AU24 | 双唇紧抿 |
| AU10 | 上唇上提（厌恶） | AU25/26 | 双唇张开/下颌下垂 |
| AU43/45 | 闭眼/眨眼 | AU27 | 嘴大张 |

---

# 一、基础情绪（8 种 · 跨文化通用）

## 1. 喜悦（真心）
- **强度等级：** 微笑 → 大笑 → 喜极
- **面部分解：** 眼角收缩起鱼尾纹、下眼睑微鼓；颧肌上提；嘴角自然上扬、露上齿；眉舒展
- **FACS：** AU6 + AU12（真笑必含 AU6 眼周；缺 AU6 即假笑）
- **肢体语言：** 身体打开、肩放松、可能轻仰头、手部上扬
- **呼吸与声音：** 呼吸轻快，可能伴笑声/气音上扬
- **持续时间：** 真情绪可持续数秒，自然起落
- **易混淆区分：** 与假笑区别——真笑眼睛在动（鱼尾纹），假笑只动嘴
- **视觉关键词：** genuine smile, crow's feet wrinkles, raised cheeks, sparkling eyes, relaxed brows
- **表演案例：** 久别重逢瞬间的绽放笑容

## 2. 悲伤
- **强度等级：** 黯然 → 含泪 → 痛哭
- **面部分解：** 眉内角上提并皱起（八字眉）；上眼睑松垂；目光下移；嘴角缓缓下拉；下唇可能极轻颤；喉结滚动（吞咽）
- **FACS：** AU1 + AU4 + AU15
- **肢体语言：** 含胸、肩下垂、头低垂、动作迟缓、手无力下垂
- **呼吸与声音：** 呼吸变浅或断续，声音低哑发闷
- **持续时间：** 宏表情，缓起缓落
- **易混淆区分：** 与疲惫区别——悲伤有 AU1 八字眉，疲惫只是眼睑垂
- **视觉关键词：** inner brow raised, drooping eyelids, downturned mouth corners, downcast gaze, trembling lower lip
- **表演案例：** 得知噩耗时强忍的瞬间

## 3. 愤怒
- **强度等级：** 不悦 → 动怒 → 暴怒
- **面部分解：** 眉头下压并内聚（竖纹）；瞪视、眼睑收紧；鼻翼扩张；双唇抿成线或下颌前突露下齿；颈侧/太阳穴青筋
- **FACS：** AU4 + AU5 + AU7 + AU23（暴怒加 AU10 露齿）
- **肢体语言：** 身体前倾、握拳指节发白、肩随呼吸起伏、可能指向对方
- **呼吸与声音：** 呼吸加重、鼻息粗，声音压低或爆发性提高
- **持续时间：** 可瞬间爆发也可压抑持续
- **易混淆区分：** 与专注区别——愤怒鼻翼张+下颌紧，专注无鼻翼变化
- **视觉关键词：** lowered furrowed brows, glaring eyes, flared nostrils, clenched jaw, tight lips, bulging neck veins
- **表演案例：** 隐忍多时后的临界爆发前一秒

## 4. 恐惧
- **强度等级：** 不安 → 惊恐 → 极度恐惧
- **面部分解：** 眉上提并拉平、内角靠拢；上眼睑大睁露出眼白；瞳孔聚焦；嘴角水平向后拉伸；嘴微张
- **FACS：** AU1 + AU2 + AU4 + AU5 + AU20 + AU26
- **肢体语言：** 身体后缩/僵直、手微颤、肩耸起护住脖颈、后退
- **呼吸与声音：** 呼吸急促而浅、屏息，声音发抖或哽住
- **持续时间：** 微表情可极短（瞬间闪过）
- **易混淆区分：** 与惊讶区别——恐惧眉内聚+嘴横拉，惊讶眉高挑+嘴圆张
- **视觉关键词：** raised flattened brows, wide eyes showing sclera, stretched lips, tense face, recoiling body
- **表演案例：** 黑暗中听到异响的刹那

## 5. 惊讶
- **强度等级：** 轻讶 → 震惊
- **面部分解：** 眉快速整体上挑（额头横纹）；眼睁大；嘴张开下颌下垂（O 形）；头微后仰
- **FACS：** AU1 + AU2 + AU5 + AU26
- **肢体语言：** 短暂定格、身体后仰、手可能捂嘴
- **呼吸与声音：** 短促吸气（倒抽一口气），可能脱口惊呼
- **持续时间：** 最短暂的情绪，常 <1 秒后转为其他情绪
- **易混淆区分：** 惊讶是中性的，下一拍才转喜/惊/怒；恐惧从一开始就带眉内聚
- **视觉关键词：** raised arched brows, wide open eyes, dropped jaw, head tilted back, gasp
- **表演案例：** 推开门看到意外场面的第一帧

## 6. 厌恶
- **强度等级：** 反感 → 恶心
- **面部分解：** 上唇上提；鼻梁皱起（皱鼻）；眯眼；下唇外推；头微侧避
- **FACS：** AU9 + AU10 + AU15 + AU16
- **肢体语言：** 身体后撤、手推开或掩鼻、转头回避
- **呼吸与声音：** 短促呼气/作呕音，"啧"或"呃"
- **持续时间：** 中短
- **易混淆区分：** 与愤怒区别——厌恶皱鼻+上唇提，愤怒皱眉+瞪眼
- **视觉关键词：** wrinkled nose, raised upper lip, squinted eyes, head turning away
- **表演案例：** 闻到腐臭/看到恶心画面的瞬间

## 7. 轻蔑
- **强度等级：** 不屑 → 嗤笑
- **面部分解：** **单侧**嘴角上扬收紧（不对称）；眼神俯视；下巴微抬
- **FACS：** AU12 + AU14（单侧）
- **肢体语言：** 抱臂、下巴抬高俯视、身体微后靠
- **呼吸与声音：** 鼻腔短哼"哼"、轻嗤
- **持续时间：** 微表情，常一闪而过
- **易混淆区分：** 唯一典型的**不对称**表情；与微笑区别在只动单侧且带俯视
- **视觉关键词：** one-sided lip corner raised, smirk, asymmetric mouth, chin up, looking down on
- **表演案例：** 反派听到对手威胁时的嗤笑

## 8. 平静（中性基线）
- **强度等级：** 放松 → 无表情
- **面部分解：** 眉舒展、眼睑自然、嘴唇放松微闭、面部肌肉无明显张力
- **FACS：** 无显著 AU（基线）
- **肢体语言：** 体态自然、呼吸均匀
- **呼吸与声音：** 平稳、声音平和
- **持续时间：** 持续基线状态
- **易混淆区分：** 用作对照基线；"强装平静"会有微表情泄漏（见复合情绪）
- **视觉关键词：** neutral expression, relaxed face, calm gaze, even breathing
- **表演案例：** 镜头对照基线、暴风雨前的宁静

---

# 二、复合 / 社会情绪（高频影视用）

## 9. 强忍泪水（隐忍）
- **面部分解：** 眼眶泛红积泪、快速眨眼逼回泪水、仰头吸气、咬下唇、喉结滚动、眉内角微提
- **FACS：** AU1 + AU17 + AU24 + AU45（频繁眨眼）
- **肢体语言：** 抿嘴仰头、深吸气、攥拳或攥物
- **呼吸与声音：** 颤抖的吸气、声音哽住
- **视觉关键词：** glistening teary eyes, rapid blinking, biting lower lip, tilting head up, throat swallowing
- **表演案例：** 葬礼上强撑不哭的人

## 10. 假笑（社交礼貌）
- **面部分解：** 嘴角上拉但**眼周不动**（无 AU6）、眼神空洞、笑容启停突然
- **FACS：** AU12（缺 AU6）
- **易混淆区分：** 与真笑核心区别就在眼睛——假笑眼睛"不笑"
- **视觉关键词：** mouth-only smile, eyes not engaged, polite forced smile, hollow gaze
- **表演案例：** 应付不喜欢的人时的客套笑

## 11. 强装镇定（外强中干）
- **面部分解：** 面部刻意维持平静、但有泄漏：吞咽（喉结动）、嘴角极轻抽动、眨眼频率异常、视线短暂飘移后强行拉回
- **FACS：** 基线 + 间歇 AU24（抿唇）+ AU45
- **肢体语言：** 刻意挺直、手指无意识小动作（搓、敲）
- **呼吸与声音：** 刻意放慢呼吸、咽口水、声音绷紧
- **视觉关键词：** forced calm, subtle swallow, micro lip twitch, controlled breathing, fidgeting fingers
- **表演案例：** 面试/审讯中故作从容

## 12. 焦虑 / 紧张
- **面部分解：** 频繁眨眼、视线游移闪躲、舔唇、眉微蹙
- **FACS：** AU4（轻）+ AU45 + 舔唇动作
- **肢体语言：** 手指搓动/敲击、抖腿、反复理衣物、坐立不安
- **呼吸与声音：** 呼吸浅而快、频繁吞咽、语速忽快忽乱
- **视觉关键词：** darting eyes, frequent blinking, lip licking, fidgeting hands, shallow breathing
- **表演案例：** 等待重大结果时的小动作

## 13. 思索 / 犹豫
- **面部分解：** 视线上移或侧移（调取记忆）、眉微蹙、嘴唇抿或微撅
- **FACS：** AU4（轻）+ 视线偏移
- **肢体语言：** 手摸下巴、捏鼻梁、托腮、手指轻敲
- **呼吸与声音：** 呼吸平稳，可能"嗯…"拖音、停顿
- **视觉关键词：** eyes looking up/aside, slight frown, hand on chin, pondering, pause
- **表演案例：** 被问到难题时的斟酌

## 14. 释然 / 如释重负
- **面部分解：** 长呼气、双肩放松下沉、眉头舒展、微微闭眼、嘴角淡淡松开
- **FACS：** AU43（短暂闭眼）+ 眉松
- **肢体语言：** 肩膀垮下放松、身体后靠、手抚胸口
- **呼吸与声音：** 一声长呼气/叹气（释放型）
- **视觉关键词：** long exhale, shoulders dropping, relaxing brow, eyes briefly closing, relief
- **表演案例：** 危机解除后瘫坐呼气

## 15. 隐藏的悲伤（强颜欢笑）
- **面部分解：** 嘴在笑（AU12）但眉内角上提泄漏（AU1）、眼神发空带泪光、笑容维持时眼睛先垮
- **FACS：** AU12 + AU1（矛盾组合 = 泄漏）
- **易混淆区分：** 关键在眉眼与嘴的**矛盾**——嘴笑眉悲
- **视觉关键词：** smiling mouth with sad inner brows, teary eyes behind smile, masking sadness
- **表演案例：** 送别时笑着挥手眼里含泪

## 16. 暗恋 / 心动（害羞的喜欢）
- **面部分解：** 偷瞄后迅速移开视线、脸颊泛红、抿嘴忍笑、眼神发亮、低头
- **FACS：** AU12（轻）+ AU6 + 视线回避
- **肢体语言：** 手摸头发/耳朵、身体微侧、脚尖内扣
- **呼吸与声音：** 轻笑、语气放软、说话变小声
- **视觉关键词：** stolen glances, blushing cheeks, shy suppressed smile, looking away then back, touching hair
- **表演案例：** 暗恋对象走近时的慌乱与窃喜

## 17. 撒谎 / 心虚
- **面部分解：** 视线回避或过度对视（刻意）、眨眼异常、微表情泄漏（一闪的真实情绪）、抿唇、不自觉摸鼻/嘴
- **FACS：** AU24 + AU45 异常 + 微表情泄漏
- **肢体语言：** 手触脸/摸鼻/挡嘴、身体朝向偏离、脚指向出口
- **呼吸与声音：** 吞咽、清嗓、语速或停顿异常、细节回避
- **视觉关键词：** averted gaze, touching nose/mouth, micro-expression leak, throat clearing, fidgeting
- **表演案例：** 被识破前的细微破绽

## 18. 决绝 / 下定决心
- **面部分解：** 眼神聚焦坚定、下颌收紧、双唇抿紧成线、眉平压而非皱
- **FACS：** AU23 + AU7 + 眼神锁定
- **肢体语言：** 深吸一口气后挺直、握拳、迈步坚定
- **呼吸与声音：** 一次深吸气作为"启动"、声音沉稳有力
- **视觉关键词：** steady determined gaze, set jaw, pressed lips, deep breath, resolute
- **表演案例：** 赴死/告别前的最后一眼

## 19. 绝望 / 崩溃边缘
- **面部分解：** 目光涣散失焦、眉内角高提、嘴角下拉颤抖、面部肌肉松垮、泪溢出
- **FACS：** AU1 + AU4 + AU15 + 失焦
- **肢体语言：** 瘫软、跪地、扶墙、手掩面、身体蜷缩
- **呼吸与声音：** 抽噎、断续喘息、气声、无声张嘴
- **视觉关键词：** vacant unfocused eyes, contorted brow, trembling downturned mouth, collapsing posture, overflowing tears
- **表演案例：** 至亲离世瞬间的失控

## 20. 惊喜（惊讶转喜悦）
- **面部分解：** 先惊讶（眉挑眼大嘴张）瞬间→转喜悦（颧肌上提、眼周收缩、大笑）
- **FACS：** (AU1+AU2+AU5+AU26) → (AU6+AU12)
- **肢体语言：** 捂嘴→张开双臂、跳起、拥抱
- **呼吸与声音：** 倒吸气→惊呼/欢笑
- **视觉关键词：** surprise turning to joy, hands over mouth then opening, gasp into laughter
- **表演案例：** 拆开意外礼物的两段式反应

## 21. 冷笑 / 阴险（反派）
- **面部分解：** 单侧或缓慢的嘴角上扬、眼神阴冷不带笑意、眼睑微收、下巴微抬
- **FACS：** AU12 + AU14 + AU7（眼冷）
- **肢体语言：** 缓慢动作、手指交叠、居高临下
- **呼吸与声音：** 低沉短笑"呵"、语速慢而笃定
- **视觉关键词：** slow cold smirk, cruel eyes without warmth, calculating gaze, sinister
- **表演案例：** 反派识破主角计划后的从容

## 22. 痛苦（生理疼痛）
- **面部分解：** 紧闭双眼、皱眉、皱鼻、龇牙咧嘴、脸部全面收紧
- **FACS：** AU4 + AU6 + AU7 + AU9 + AU10 + AU43
- **肢体语言：** 蜷曲、捂住伤处、肌肉紧绷、冷汗
- **呼吸与声音：** 倒吸气、闷哼、咬牙的嘶声
- **视觉关键词：** clenched shut eyes, grimace, bared teeth, contorted face, clutching wound
- **表演案例：** 受伤瞬间的本能反应

## 23. 鄙夷中带怒（复合负面）
- **面部分解：** 皱鼻（厌恶）+ 皱眉瞪视（愤怒）+ 单侧嘴角下撇
- **FACS：** AU4 + AU9 + AU10 + 单侧 AU15
- **视觉关键词：** disgust mixed with anger, wrinkled nose with glare, sneering scowl
- **表演案例：** 面对卑劣行径的怒斥前

## 24. 心碎（震惊后的崩塌）
- **面部分解：** 先怔住（眼神空、嘴微张）→ 眉内角缓提、嘴角下垮、泪盈眶，一拍延迟才反应
- **FACS：** 基线怔住 → AU1 + AU15
- **肢体语言：** 身体僵住、手缓缓松开、后退半步
- **呼吸与声音：** 呼吸停顿（屏息）→ 颤抖呼气
- **视觉关键词：** frozen shock then crumbling, delayed reaction, welling tears, hand going limp
- **表演案例：** 听到背叛真相的延迟崩塌

# 三、进阶 / 复杂情绪（25–55）

## 25. 得意 / 自满
- **面部分解：** 下巴微抬；单/双侧嘴角上扬并收紧；眼睑微眯（满意）；眉轻挑
- **FACS：** AU12 + AU14 + 下巴抬 + AU2(轻)
- **肢体语言：** 挺胸、抱臂或叉腰、身体后靠、晃头
- **呼吸与声音：** 轻哼、语气上扬拖长、得意的"哈"
- **视觉关键词：** smug grin, chin raised, narrowed satisfied eyes, self-satisfied smirk, puffed chest
- **表演案例：** 计谋得逞后的洋洋自得

## 26. 嫉妒 / 眼红
- **面部分解：** 眉微皱；目光紧盯目标（执着凝视）；嘴角下压或抿；眼神阴沉；轻咬牙
- **FACS：** AU4 + AU7 + AU24 + 固定凝视
- **肢体语言：** 身体僵、手攥紧、视线追随对方
- **呼吸与声音：** 短促呼气、压低阴阳怪气的语气
- **易混淆区分：** 与愤怒区别——嫉妒含"盯住某对象"的执着＋隐藏
- **视觉关键词：** fixed envious stare, subtle scowl, clenched jaw, simmering resentment, eyes tracking rival
- **表演案例：** 看到情敌得宠时暗自咬牙

## 27. 愧疚 / 自责
- **面部分解：** 目光下垂回避（不敢直视）；眉内角提；嘴角下拉；低头；可能咬唇
- **FACS：** AU1 + AU15 + 视线下移
- **肢体语言：** 含肩低头、手不安、后缩
- **呼吸与声音：** 声音低弱、欲言又止、叹气
- **易混淆区分：** 与悲伤区别——愧疚有"不敢看对方"的回避
- **视觉关键词：** lowered guilty gaze, avoiding eye contact, inner brow raised, bowed head, biting lip
- **表演案例：** 做错事后不敢抬头

## 28. 警惕 / 戒备
- **面部分解：** 眉微压；眼睛快速扫视环境；眼睑微收；嘴抿；下巴微收
- **FACS：** AU4(轻) + AU7 + 眼球快速移动
- **肢体语言：** 身体绷紧半侧、重心下沉、手护身前、缓慢移动
- **呼吸与声音：** 屏息或浅呼吸、压低声音
- **视觉关键词：** alert scanning eyes, lowered brows, tense guarded posture, on guard, darting watchful glance
- **表演案例：** 进入未知危险区时的环视

## 29. 困惑 / 迷茫
- **面部分解：** 单侧眉上挑或双眉微蹙；眼神游移；嘴微张或撇；头微歪
- **FACS：** AU4 + 单侧 AU2 + 头倾
- **肢体语言：** 歪头、挠头、摊手、停顿
- **呼吸与声音：** "啊？""嗯…？"上扬疑问、停顿
- **视觉关键词：** furrowed confused brow, one raised eyebrow, tilted head, puzzled searching eyes, scratching head
- **表演案例：** 听到不合逻辑的话时的歪头

## 30. 陶醉 / 沉醉
- **面部分解：** 微闭眼或眼神柔和失焦；嘴角松松上扬；眉舒展；面部放松
- **FACS：** AU43(半闭) + AU12(轻) + AU6(柔)
- **肢体语言：** 头微仰或微晃、身体放松摇曳、手轻抚
- **呼吸与声音：** 深长呼吸、满足的"嗯~"、轻哼
- **视觉关键词：** half-closed blissful eyes, soft dreamy gaze, gentle smile, enraptured relaxed face, savoring
- **表演案例：** 品尝美食/听动人音乐时的沉醉

## 31. 尴尬 / 窘迫
- **面部分解：** 脸红；勉强僵硬的笑；视线乱飘回避；抿嘴；可能摸脸
- **FACS：** AU12(僵) + AU24 + 视线回避 + 脸颊泛红
- **肢体语言：** 摸后颈、搓手、缩脖、脚动
- **呼吸与声音：** 干笑"哈哈…"、结巴、清嗓
- **易混淆区分：** 与羞愧区别——尴尬偏社交不适且常带干笑，羞愧更沉重
- **视觉关键词：** awkward forced smile, blushing, darting eyes, rubbing neck, flustered, nervous chuckle
- **表演案例：** 当众说错话后的强笑

## 32. 不甘 / 憋屈
- **面部分解：** 咬牙；眼眶泛红含泪但瞪着；眉皱；嘴角下压颤抖；鼻翼动
- **FACS：** AU4 + AU7 + AU23 + 泪光
- **肢体语言：** 攥拳发抖、低头又猛抬、身体绷紧
- **呼吸与声音：** 粗重鼻息、压抑颤音、咬牙的"凭什么"
- **易混淆区分：** 愤怒+悲伤+不服三合一，"瞪着却含泪"是关键
- **视觉关键词：** clenched teeth with teary defiant eyes, trembling suppressed resentment, unwilling, fists shaking
- **表演案例：** 努力却被否定时红着眼眶咬牙

## 33. 怀疑 / 质疑
- **面部分解：** 单侧眉挑；眼睑微眯；斜眼打量；嘴角一侧下压；下巴微收
- **FACS：** 单侧 AU2 + AU7(眯) + 斜视
- **肢体语言：** 身体微后仰、抱臂、上下打量
- **呼吸与声音：** 拖长的"哦~是吗？"、停顿审视
- **视觉关键词：** raised single eyebrow, narrowed skeptical eyes, sidelong scrutinizing glance, doubtful smirk, sizing up
- **表演案例：** 听到可疑解释时眯眼打量

## 34. 失望
- **面部分解：** 眼神黯淡下垂；眉先扬后落；嘴角下拉；轻摇头；垂眸
- **FACS：** AU15 + AU1(轻) + 摇头
- **肢体语言：** 肩塌、转身、手垂、轻叹
- **呼吸与声音：** 泄气的叹息、声音低落、"算了"
- **易混淆区分：** 与悲伤区别——失望常带"摇头/转身"的放弃
- **视觉关键词：** dimmed downcast eyes, slight head shake, sighing, drooping mouth, deflated, letdown
- **表演案例：** 期望落空后的摇头叹气

## 35. 期待 / 憧憬
- **面部分解：** 眼睛发亮放大；眉上扬；嘴微张含笑；目光望向远方/上方
- **FACS：** AU1 + AU2 + AU5(轻) + AU12(轻)
- **肢体语言：** 身体前倾、双手交握胸前、踮脚、坐不住
- **呼吸与声音：** 轻快呼吸、语气上扬充满希望
- **视觉关键词：** bright hopeful eyes, raised brows, leaning forward eagerly, dreamy upward gaze, anticipation
- **表演案例：** 等待心上人到来时的雀跃

## 36. 厌倦 / 无聊
- **面部分解：** 眼皮半垂；目光涣散；面无表情；可能打哈欠；嘴撇
- **FACS：** AU43(半垂) + 面部松弛
- **肢体语言：** 托腮、瘫靠、转笔、看表、坐姿散漫
- **呼吸与声音：** 长叹气、有气无力的"嗯"、拖音
- **视觉关键词：** half-lidded vacant eyes, propping chin, slouching, yawning, listless, glazed over
- **表演案例：** 冗长会议中的神游

## 37. 受惊 / 惊吓反射
- **面部分解：** 瞬间全脸收缩；紧闭眼；眉猛压；缩头（反射性，极快）
- **FACS：** AU4 + AU5 → AU7 + AU43(瞬闭)
- **肢体语言：** 全身一震、肩猛耸、双手护头、后跳
- **呼吸与声音：** 倒抽气、短促惊叫、屏息
- **易混淆区分：** 与恐惧区别——惊吓是瞬间反射(<0.2s)，恐惧是持续状态
- **视觉关键词：** startle reflex, flinch, sudden full-body jolt, shoulders jerking up, recoiling, gasp
- **表演案例：** 背后突然被拍肩的激灵

## 38. 委屈
- **面部分解：** 眼眶迅速泛红蓄泪；瘪嘴（下唇前推上顶）；眉内角高提；低头又抬眼看人
- **FACS：** AU1 + AU17 + AU15 + 泪
- **肢体语言：** 缩肩、绞手、低头、可能扑向人怀
- **呼吸与声音：** 抽噎前颤音、带哭腔的"我没有…"、吸鼻
- **易混淆区分：** 中式情感核心——"觉得被冤枉"的瘪嘴＋泪眼看对方
- **视觉关键词：** quivering pouting lip, welling teary eyes, raised inner brows, looking up wronged, sniffling
- **表演案例：** 被误会后含泪辩解

## 39. 羞愧 / 羞耻
- **面部分解：** 深深低头；闭眼或不敢睁；脸涨红；嘴角紧；捂脸
- **FACS：** AU4 + AU43 + 脸红 + 低头幅度大
- **肢体语言：** 整个人想缩小、捂脸、转身背对、蹲下
- **呼吸与声音：** 几不可闻的声音、哽住、"对不起…"
- **易混淆区分：** 比尴尬更重，有"想消失"的躲藏感
- **视觉关键词：** deeply bowed head, covering face, flushed with shame, shrinking away, unable to look up
- **表演案例：** 当众出丑后捂脸蹲下

## 40. 同情 / 怜悯
- **面部分解：** 眉内角上提；眼神温柔含怜；嘴角微下但柔和；头微侧
- **FACS：** AU1 + 柔和注视
- **肢体语言：** 身体前倾靠近、伸手轻抚/搭肩、放慢动作
- **呼吸与声音：** 放柔语气、轻声安慰、"没事的…"
- **易混淆区分：** 与悲伤区别——同情是"看向他人"的外向关怀
- **视觉关键词：** softened pitying gaze, raised inner brows, tender concerned look, reaching out gently, empathy
- **表演案例：** 看到他人受苦时的轻抚

## 41. 麻木 / 心如死灰
- **面部分解：** 完全空洞的眼神（死鱼眼）；面无表情；嘴微张松；眨眼极少
- **FACS：** 全面部松弛、无 AU、凝滞凝视
- **肢体语言：** 呆坐不动、动作机械、目光放空盯虚空
- **呼吸与声音：** 浅缓近停滞、声音平板无起伏、单字回应
- **易混淆区分：** 与平静区别——麻木是"被掏空"的死寂，平静是放松
- **视觉关键词：** hollow vacant stare, dead eyes, blank affectless face, emotionally numb, thousand-yard stare
- **表演案例：** 经历巨大创伤后的呆滞

## 42. 狂喜 / 亢奋
- **面部分解：** 大笑露齿；眼睛发光眯起；眉高扬；满脸放光
- **FACS：** AU6 + AU12(极) + AU1 + AU2
- **肢体语言：** 跳跃、振臂、拥抱身边人、手舞足蹈
- **呼吸与声音：** 大笑、欢呼、高声呐喊、急促兴奋
- **视觉关键词：** ecstatic beaming grin, sparkling eyes, jumping with joy, arms thrown up, euphoric, exhilarated
- **表演案例：** 中奖/夺冠瞬间的爆发欢呼

## 43. 隐忍 / 压抑
- **面部分解：** 刻意维持平静但肌肉紧绷；咬肌鼓动（咬牙）；嘴抿成线；眼神下压克制；太阳穴跳
- **FACS：** AU24 + AU17 + 咬肌收缩
- **肢体语言：** 攥拳藏于身侧、肩绷、深吸气强压、僵立
- **呼吸与声音：** 刻意深长的呼吸控制、从齿缝挤字、声音绷紧发抖
- **易混淆区分：** 关键是"明显在压抑强烈情绪"的张力外泄
- **视觉关键词：** tightly suppressed emotion, jaw muscle twitching, pressed lips, controlled trembling, holding back
- **表演案例：** 听到挑衅强忍不发作

## 44. 好奇
- **面部分解：** 眼睛睁大发亮；眉上扬；头前伸靠近；嘴微张
- **FACS：** AU1 + AU2 + AU5(轻) + 前倾
- **肢体语言：** 凑近、踮脚张望、伸长脖子、手指轻点
- **呼吸与声音：** 轻"咦？"、上扬探问、屏息细看
- **易混淆区分：** 与惊讶区别——好奇是持续探究欲，带主动靠近
- **视觉关键词：** wide curious eyes, raised brows, leaning in to look closer, craning neck, intrigued, inquisitive
- **表演案例：** 发现新奇事物凑近端详

## 45. 感动 / 动容
- **面部分解：** 眼眶湿润；眉内角提；嘴角微颤上扬（含泪的笑）；目光柔软凝视
- **FACS：** AU1 + AU12(轻) + 泪光
- **肢体语言：** 手抚胸口、微微点头、捂嘴、身体微倾
- **呼吸与声音：** 哽咽的吸气、颤抖的"谢谢…"、轻抽气
- **易混淆区分：** "含泪而笑"的正向感动，与心碎相反
- **视觉关键词：** glistening moved eyes, trembling tender smile, hand on chest, touched, grateful welling tears
- **表演案例：** 收到意外关怀时红了眼眶

## 46. 怀念 / 追忆
- **面部分解：** 目光柔和飘向远方；嘴角若有若无的浅笑；眼神失焦；眉微舒
- **FACS：** 柔和远眺 + AU12(极轻)
- **肢体语言：** 手轻抚旧物、静止出神、头微仰
- **呼吸与声音：** 悠长呼吸、轻叹、放缓低柔的语气
- **视觉关键词：** wistful distant gaze, faint reminiscent smile, eyes losing focus, lost in memory, nostalgic, bittersweet
- **表演案例：** 翻看旧照片时怅然浅笑

## 47. 恍惚 / 出神
- **面部分解：** 目光呆滞放空；眼神不聚焦；面部静止；对外界无反应
- **FACS：** 凝滞凝视、无 AU
- **肢体语言：** 僵在原地、手中物可能滑落、被叫才一震回神
- **呼吸与声音：** 平缓无意识、被唤"啊？"猛回神
- **易混淆区分：** 与麻木区别——恍惚是"思绪飘走"可被唤回，麻木是情感死寂
- **视觉关键词：** spacing out, unfocused distant stare, lost in thought, zoning out, snapping back when called
- **表演案例：** 沉浸思绪被叫醒前的呆滞

## 48. 不耐烦
- **面部分解：** 翻白眼；皱眉；抿嘴或撇嘴；频繁瞥向别处；深吸气
- **FACS：** AU4 + 眼球上转(翻白眼) + AU24
- **肢体语言：** 抖腿、手指快速敲击、看表、抱臂、跺脚
- **呼吸与声音：** 重重叹气、"快点""行了行了"、催促语速
- **视觉关键词：** rolling eyes, frowning impatiently, tapping fingers, checking time, huffing, foot tapping
- **表演案例：** 排长队等待时的烦躁

## 49. 怯懦 / 畏缩
- **面部分解：** 眼神躲闪不敢直视；眉内角提；缩着脸；抿唇
- **FACS：** AU1 + 视线回避 + 收缩
- **肢体语言：** 含胸缩肩、身体后缩、双手护身前、小步后退
- **呼吸与声音：** 细弱发颤的声音、结巴、"我…我不…"
- **易混淆区分：** 与恐惧区别——怯懦是面对强势者的退缩，偏社交弱势
- **视觉关键词：** timid averted eyes, cowering hunched posture, meek, flinching back, submissive, shrinking
- **表演案例：** 被强势者呵斥时的瑟缩

## 50. 苦笑
- **面部分解：** 嘴角上扬但眉内角悲伤上提；眼神无奈；笑里带涩；轻摇头
- **FACS：** AU12 + AU1(矛盾) + 摇头
- **肢体语言：** 摊手、轻耸肩、低头轻笑
- **呼吸与声音：** 一声无奈轻笑"呵"、自嘲的叹
- **易混淆区分：** 与"强颜欢笑"近似，但苦笑更主动表达"无奈/自嘲"
- **视觉关键词：** bitter wry smile, helpless self-mocking grin, sad eyes behind smile, rueful, chuckle with head shake
- **表演案例：** 面对无解困境的自嘲一笑

## 51. 后怕（惊魂未定）
- **面部分解：** 危机过后长呼气；抚胸；眼睛仍睁大未褪惊；眉松开又皱
- **FACS：** AU5(残留) → 长呼气 + AU43
- **肢体语言：** 手按胸口、扶墙瘫软、拍胸、腿软
- **呼吸与声音：** 大口喘气后长舒、"吓死我了"、心有余悸的颤
- **视觉关键词：** catching breath after a scare, hand clutching chest, wide eyes still shaken, shaky relief
- **表演案例：** 险些出事后的拍胸喘息

## 52. 强忍笑意
- **面部分解：** 嘴角不断上抽却努力抿住；脸颊鼓；眼睛眯起泛笑意；憋红脸
- **FACS：** AU12(对抗) + AU24(抿) + AU6
- **肢体语言：** 捂嘴、低头、肩一耸一耸、转过身
- **呼吸与声音：** 憋笑的鼻音"噗"、漏气轻笑、岔气
- **视觉关键词：** suppressing a laugh, lips twitching to hold back smile, puffed cheeks, shaking shoulders, stifled giggle
- **表演案例：** 严肃场合看到好笑事憋笑

## 53. 娇嗔 / 嗔怒
- **面部分解：** 假装生气的撅嘴；轻皱鼻；瞪一眼但眼里带笑；扭头
- **FACS：** AU17(撅) + AU4(假) + 眼带笑意
- **肢体语言：** 轻捶对方、跺脚、扭身、叉腰
- **呼吸与声音：** 拖长的"讨厌啦~""哼"、嗲音
- **易混淆区分：** 恋爱/亲昵中的"假怒真撒娇"，怒中带甜
- **视觉关键词：** playful pout, mock-angry glare with smiling eyes, cute huff, teasing sulk, turning away coyly
- **表演案例：** 情侣间被打趣时的撒娇捶打

## 54. 大彻大悟 / 顿悟
- **面部分解：** 先怔 → 眼睛缓缓睁亮；眉舒展；嘴微张"啊…"；面部由紧转松
- **FACS：** AU4(困) → AU1 + AU2 + AU5(亮)
- **肢体语言：** 猛地抬头、身体一震又松、缓缓点头、手一拍
- **呼吸与声音：** 恍然的吸气、"原来如此…"、释然的笑
- **视觉关键词：** dawning realization, eyes lighting up, brows lifting in understanding, "aha" moment, slow nod of clarity
- **表演案例：** 想通关键真相的那一刻

## 55. 心满意足 / 安然
- **面部分解：** 柔和浅笑；眼神温暖平和；眉完全舒展；面部松弛
- **FACS：** AU12(轻) + AU6(柔) + 全面部放松
- **肢体语言：** 舒展靠坐、双手交叠腹前、缓慢满足的呼吸、微微点头
- **呼吸与声音：** 满足的长舒气、轻柔的"嗯，真好"、温和语调
- **易混淆区分：** 与喜悦区别——满足是平静持久的暖，喜悦是外放的高峰
- **视觉关键词：** serene content smile, warm peaceful eyes, fully relaxed brow, settled and at ease, quiet satisfaction
- **表演案例：** 完成心愿后的安然微笑


---

# 四、跨文化微表情差异（56–59）

## 56. 东亚含蓄式厌恶（文化微表情）
- **强度等级：** 轻微反感 → 嫌恶回避
- **面部分解：** 上唇极轻微上提（几乎不可见）；鼻翼微微收紧但不皱鼻；嘴角轻轻下压；目光快速扫过目标后移开；面部整体保持礼节性克制。与西方"全脸皱鼻+上唇猛提"不同，东亚厌恶主要通过视线回避和嘴角微动作表达
- **FACS：** AU10(极轻) + AU15(极轻) + 视线回避
- **肢体语言：** 身体微侧；手自然收起不接触目标物；礼貌后退半步；不直接当面拒绝
- **呼吸与声音：** 短暂屏息或极轻鼻息；"礼貌的沉默"替代直接批评；可能发出极轻的"嗯…"拖音
- **持续时间：** 微表情闪现（<0.3s）后迅速恢复中性
- **易混淆区分：** 与西方厌恶区别——东亚版极度克制，面部肌肉动作幅度极小，像"厌恶被礼貌压下去了"；影视指导应给镜头特写捕捉嘴角/鼻翼微动
- **视觉关键词：** subtle disgust micro-movement, minimal nose wrinkle, polite aversion, restrained lip curl, gaze avoidance, East Asian restrained expression, barely visible disdain
- **表演案例：** 宴会上尝到不合口味的食物却维持礼貌微笑

## 57. 拉美热情式惊讶（文化微表情）
- **强度等级：** 微微讶异 → 高度惊诧
- **面部分解：** 眉大幅高挑并形成夸张额头横纹；眼大睁但伴随明亮笑意（AU6参与）；嘴大张呈椭圆而非圆形；惊讶后极快伴随双手动作。与欧亚"定格式惊讶"不同，拉美惊讶偏向动态夸张且常带积极情绪预判
- **FACS：** AU1 + AU2 + AU5 + AU26 + AU6(伴随)
- **肢体语言：** 双手张开、举过头顶、身体夸张后仰、拍胸口、指向目标物；动作幅度大且多
- **呼吸与声音：** 大声倒吸气或惊呼"¡Dios mío!"式感叹；语调上翘、音量偏大
- **易混淆区分：** 与经典惊讶区别——拉美版本动作幅度×3，且惊讶中混有兴奋/期待的正面情感色彩；在中国观众看来可能被误读为"故意做作"
- **视觉关键词：** exaggerated surprise, wide theatrical eyes, open-mouthed gasp, hands flying up, animated Latin expression, enthusiastic shock
- **表演案例：** 拉美角色收到意外礼物时的夸张惊呼与手舞足蹈

## 58. 中东礼仪性微笑（文化微表情）
- **强度等级：** 客套礼 → 热情欢迎
- **面部分解：** 嘴角对称上扬但幅度中大（介于真笑与假笑之间）；眼周有轻度AU6参与但眼神保持一定距离；眉舒展；面部整体温暖但带礼节感。与"假笑（缺AU6）"不同——中东礼仪笑有真笑成分但受社交规则调节
- **FACS：** AU12 + AU6(中度) + 眉心完全舒展
- **肢体语言：** 右手抚胸（手掌贴左胸口的标志礼仪）；微躬身或点头致意；身体前倾表示热情；与对方握手时双手握住对方单手
- **呼吸与声音：** 温和的问候语、语调缓慢庄重；常伴随祝福语
- **易混淆区分：** 与"真笑"区别——中东礼仪笑虽含AU6但笑容进入/退出有明显社交节奏；与"假笑"区别——眼部参与真实但受压制
- **视觉关键词：** warm ceremonial smile, hand on heart gesture, respectful eye engagement, Middle Eastern greeting expression, measured genuine warmth
- **表演案例：** 中东角色以手抚胸微笑向客人表示欢迎

## 59. 北欧克制式悲伤（文化微表情）
- **强度等级：** 内心哀痛 → 外显淡漠
- **面部分解：** 面部几乎保持中性基线——眉内角仅极微上提（AU1极轻）；嘴角无下拉，仅"不笑了"；眼睑不发红但眼神空洞向下45°偏移。与东亚/南欧"含泪啜泣"不同，北欧悲伤的核心是"情绪撤出"而非"情绪外泄"
- **FACS：** AU1(极轻) + 视线下移 + 面部活动全面减少
- **肢体语言：** 静止不动；手插口袋或交叠于身前；不寻求肢体接触；可能独自走进另一房间
- **呼吸与声音：** 呼吸极为平稳但略浅；长时间沉默；声音平淡不带哭腔
- **持续时间：** 持续状态，缓慢起落；数分钟内无明显变化
- **易混淆区分：** 与"麻木/心死"区别——北欧克制悲伤是文化习得的情绪管理，内心仍有痛感但不外泄；与"平静"区别——有AU1极微颤动和沉默时间异常
- **视觉关键词：** stoic grief, barely visible inner brow movement, emotional withdrawal, Nordic restrained sorrow, minimal facial activity, still silence
- **表演案例：** 北欧角色接到噩耗后安静独坐、面无波澜但久久不动

---

# 五、AI 表情生成常见缺陷与规避（60–64）

## 60. AI缺陷：塑料感笑容（恐怖谷效应）
- **缺陷描述：** AI生成微笑时，嘴角上拉的肌肉运动曲线过于平滑对称、缺乏真人微笑的微不对称和启停惯性；眼周AU6缺失或过度夸张，导致"眼睛在笑但没灵魂"的恐怖谷效果
- **出问题部位：** 颧肌收缩曲线（AU6）与嘴角上扬曲线（AU12）的时间同步性——真人微笑时AU6先于AU12启动约0.05s，AI很容易把两者设成全同步
- **提示词规避策略：** 避免直接写smile；改用"slight asymmetric curve at lip corners"，"eyes crinkling naturally with genuine warmth"，"imperfect human smile with micro-timing offset between eyes and mouth"
- **规避关键词：** asymmetrical micro-smile, eyes warming before lips, natural crow's feet, organic facial curve, genuine uneven grin, not CG-smooth
- **实用提示词片段：** "a subtle asymmetrical smile where the left corner lifts slightly before the right, crow's feet appear with 0.05s natural delay after lip movement, avoid uncanny symmetry"

## 61. AI缺陷：死鱼眼/空洞凝视
- **缺陷描述：** 角色面部在做情绪表达时眼神不跟随——嘴在笑但瞳孔锁定不动、愤怒时眼睛睁大但缺乏焦点移动扫视、悲伤时眼泪流但眼神没有"向内看"的失焦。眼球微动（saccade）和注视点切换是AI最容易忽略的层
- **出问题部位：** 瞳孔焦点、saccade微幅快动、注视时长分布；真人每200-400ms有一次微扫视，AI生成往往完全缺失
- **提示词规避策略：** 在提示词中明确标注眼动方向和时间:"gaze shifts from object to camera with slight 0.3s delay"，"eyes darting in micro-saccades during nervous speech"，"pupil defocuses as she looks inward"
- **规避关键词：** micro-saccade eye movements, shifting focal point, gaze darting subtly, pupil dilation change, natural scanning pattern, not frozen stare
- **实用提示词片段：** "her gaze continuously shifts in 0.2-0.4s micro-movements scanning the room, pupils contract slightly when focusing on the threat, avoid frozen fixed stare"

## 62. AI缺陷：肢体与面部不同步
- **缺陷描述：** 面部表情与身体动作之间的因果关系断裂——角色攥拳时面部肌肉却未同步收紧、大笑着拍桌但面部笑容已在手势前0.5s消退、恐惧时身体后退但面部的AU20还没出现。真人肢体-面部情绪是耦合的，AI常把它们当作独立通道生成
- **出问题部位：** 面部AU激活与肢体动作的时间轴对齐；情感强度在肢体与面部的幅度匹配
- **提示词规避策略：** 用联动句式标注:"as fists clench, jaw tightens simultaneously"，"smile reaches eyes at the exact moment he opens his arms"，"brows furrow in sync with shoulders tensing"
- **规避关键词：** synchronized face-body expression, simultaneous clench, emotion cascading from body to face, coupled muscle activation, gesture-facial lock
- **实用提示词片段：** "when she slams the table with her right hand, her jaw tightens and nostrils flare in perfect sync, the anger travels from hand impact up to her face in one continuous wave"

## 63. AI缺陷：五官过度扭曲（崩溃式表情）
- **缺陷描述：** 在生成高愤怒/极度恐惧/痛哭等极端情绪时，AI容易把五官推向解剖学不可能的位置——嘴角拉到耳根、眼睛大到眼眶装不下、眉毛挑到发际线……造成"橡皮脸"崩溃效果而非真实的高强度表情
- **出问题部位：** 各AU的动作幅度在极端值附近的非线性限制；真人肌肉有物理极限（如AU12嘴角上拉最大约45°），AI常无视这些边界
- **提示词规避策略：** 用解剖级约束标注:"maximum lip corner elevation limited by zygomaticus anatomy"，"brow furrowing within natural orbital rim range"，"mouth open to 2/3 of anatomical maximum"
- **规避关键词：** anatomically constrained expression, natural muscle range, within physical limits, realistic intense emotion, not exaggerated distortion, humanly possible
- **实用提示词片段：** "intense anger with jaw clenched within natural masseter contraction range, brow depression limited by orbital bone structure, no rubber-face distortion, maintain anatomical credibility at extreme emotion"

## 64. AI规避：微表情标注总策略
- **策略描述：** AI视频/图像模型本质是统计拟合，缺乏对"0.04-0.5秒级别微表情"的建模——它们倾向于把每一种情绪都渲染成持续的宏表情。生视频时必须用时间+解剖学约束来绕过这个底层瓶颈
- **核心原则：** ①永远在提示词中包含时间窗口（"0.3s micro-flash of X before returning to baseline"）；②用AU编号而非情绪词（"AU4+AU7 for 0.2s"而非"angry"）；③始终给一个"基线回归"锚点；④混用矛盾AU人为制造真实感（AU12嘴笑+AU1眉悲）
- **规避关键词：** micro-expression flash under 0.5s, AU-level granularity, return to neutral baseline, contradictory AU combination, emotion leak only
- **通用提示词模板：** "[面部区域] undergoes [AU变化] for [0.X秒] then returns to [基线状态], while [另一区域] briefly contradicts with [另一AU], creating a micro-expression leak that betrays the true emotion beneath the surface mask"
- **视觉关键词：** AU-based prompt engineering, micro-expression temporal annotation, baseline return anchor, contradictory facial cues

---

# 六、复合情绪微表情扩展（65–69）

## 65. 愤怒中的恐惧（受威胁的攻击者）
- **强度等级：** 低强度压制 → 高强度爆发中的颤栗
- **面部分解：** 愤怒层（皱眉下压AU4、鼻翼扩张AU10、咬肌鼓动）与恐惧层（眉内角上提AU1、嘴角微横拉AU20、眨眼频率异常增高）同时出现。愤怒主导面部上2/3，恐惧泄漏在嘴和眼周——嘴巴在怒吼但嘴角带着后退的横拉，眼睛在瞪但带有闪避式高频眨眼
- **FACS：** AU4 + AU10 + AU23（愤怒）∩ AU1 + AU20 + 高频AU45（恐惧泄漏）
- **肢体语言：** 身体前倾攻击姿态，但脚指向出口方向（恐惧泄漏）；握拳挥出但同时有微幅后退重心
- **呼吸与声音：** 怒吼声量中带微颤；呼吸急促但有吞咽（喉结滚动泄漏恐惧）
- **易混淆区分：** 与纯愤怒区别——存在"攻击同时防御"的矛盾体语；瞳孔放大（恐惧）vs 瞳孔缩小（愤怒）的矛盾也可利用
- **视觉关键词：** anger with fear underneath, aggressive yet trembling mouth, forward body with backward feet, threatening but scared eyes, defensive aggression, flinching glare
- **表演案例：** 被逼入绝境的反派最后威胁——表面凶狠但眼里已流露恐惧

## 66. 轻蔑中的欣赏（傲娇式矛盾）
- **强度等级：** 表面不屑 → 难以掩饰的欣赏泄漏
- **面部分解：** 轻蔑层（单侧嘴角上扬AU12单侧、下巴微抬、眼神俯视）与欣赏层（另一侧眉轻挑AU2单侧、眼神短暂发亮、嘴角另一侧极轻微的正面抽动）的交错。核心是"不对称的双重表情"——左侧脸在骄傲地说不，右侧脸已在偷偷说好
- **FACS：** 单侧AU12 + 下巴抬（轻蔑）∩ 对侧AU2 + 眼睛短暂发光（欣赏泄漏）
- **肢体语言：** 嘴上说着"一般般"但身体已经在靠近；抱臂但手指轻敲对方方向；转身要走又回头看
- **呼吸与声音：** 嗤笑声尾音上扬（不屑→认可）；"哼，还算有点意思"的语调矛盾
- **易混淆区分：** 关键识别——同一个人的左右半脸呈现不同情绪，且身体姿态与面部表情产生"推拉矛盾"
- **视觉关键词：** tsundere micro-expression, contempt masking admiration, one side smirking other side softening, reluctant appreciation leak, half-face contradiction
- **表演案例：** 傲娇角色嘴上批评但眼里藏不住欣赏（动漫/青春剧高频用）

## 67. 悲喜交加（含泪的狂笑）
- **强度等级：** 笑中藏泪 → 完全交叠的悲喜不能分离
- **面部分解：** 喜悦层（颧肌上提AU6、嘴角上扬AU12、露齿）与悲伤层（眉内角上提AU1、下唇颤抖、眼眶盈泪）完全叠加。是真笑（AU6活跃）+真悲伤（AU1+泪）的同步共存，没有任何伪装成分——颧肌在往上推、眉内角也在往上提，面部上下方向相反的力量制造出极具张力的"撕裂式"表情
- **FACS：** AU6 + AU12 + AU25(露齿大笑) ∩ AU1 + 泪 + 下唇颤
- **肢体语言：** 笑到身体颤抖但手捂胸口（保护性）；大笑躺倒但手指抠紧地面；笑与抽噎交替
- **呼吸与声音：** 笑声与抽气声交替、无法区分笑与哭的声音、断断续续的换气
- **易混淆区分：** 与"强颜欢笑"区别——悲喜交加中喜悦和悲伤都是真实的、同等强度的，没有伪装成分；是真笑真哭同时发生
- **视觉关键词：** genuine laugh and cry simultaneous, tears streaming through smile, laughing while sobbing, eyes crinkling with joy while overflowing with grief, emotionally torn face
- **表演案例：** 失散多年的亲人在最不堪的时刻重逢，笑着流泪说不出话

## 68. 嫉妒中的倾慕（被吸引又痛苦）
- **强度等级：** 暗含酸涩 → 倾慕与憎恨的漩涡
- **面部分解：** 嫉妒层（眉头微压AU4、目光紧盯、咬牙AU23）与倾慕层（眼神发亮无法移开、嘴角不自觉的轻微上扬AU12、面部不自觉的柔软瞬间）交替闪现。核心节奏："盯着看→面部收紧→不自觉软下来→发现自己在软→又收紧"，循环往复
- **FACS：** AU4 + AU7 + AU23（嫉妒）↔ AU12(轻) + AU6(微) + 凝视发亮（倾慕泄漏）
- **肢体语言：** 不自觉朝对方方向倾身又猛收回；手伸向对方方向又攥紧收回；反复整理自己的衣物或头发
- **呼吸与声音：** 酸涩的轻"哼"后沉默注视；想说什么又咽回去（吞咽）；语带酸意但尾音变软
- **易混淆区分：** 与纯嫉妒区别——有反复出现的"不自觉地微笑泄漏"和"被吸引式身体靠近"；与暗恋区别——暗恋是甜中带羞，嫉妒倾慕是酸中带甜
- **视觉关键词：** jealous admiration oscillation, watching through pain, hard then soft then hard, conflicting attraction, bitter-sweet stare, being drawn in against will
- **表演案例：** 看到心上人对别人温柔——眼里既酸涩又忍不住欣赏对方的美好

## 69. 不甘后的释然（认命式苦笑）
- **强度等级：** 挣扎后的松手 → 痛中取静的放下
- **面部分解：** 不甘层（咬肌紧绷鼓动AU17+AU23、眼眶微红含泪、眉头下压AU4）逐步消解，转化为释然层（眉缓缓舒展、咬肌松开、嘴由抿紧转为微微松开——不是微笑，只是"不抿了"、眼神从紧盯转为远眺）。关键时间线：面部肌肉逐层松开的顺序——先松下巴→再松眉→最后松开嘴角
- **FACS：** (AU17 + AU23 + AU4) → (逐层松开至基线) + 长呼气 + 远眺
- **肢体语言：** 攥紧的拳头缓缓松开垂到身侧；从紧绷前倾到慢慢靠回椅背；轻摇头后静止
- **呼吸与声音：** 一声深长叹息（把最后的挣扎呼出去）；低声自语"命吧""算了"；声音从绷紧恢复到温和平淡
- **易混淆区分：** 与"失望"区别——不甘后的释然有"从紧到松"的动态过程，失望是单向下沉；与"释然/如释重负"区别——此条目是"没有解决问题但接受了无解"，释然是"问题已解决"
- **视觉关键词：** gradual muscle release, accepting the unacceptable, letting go of resentment layer by layer, softening from jaw to brow, quiet surrender, bittersweet release
- **表演案例：** 努力多年后发现无论如何也赢不了——缓缓松开拳头，望着远方轻轻说了声"算了"

---

## 使用提示
- **强度 = 微动作的幅度 × 数量**：隐忍=幅度小、单一部位；爆发=幅度大、多部位联动。
- **复合情绪靠"矛盾"取胜**：嘴笑+眉悲=强颜欢笑，是最高级的表演细节。
- **微表情泄漏**（一闪而过的真实情绪）是「撒谎/强装」类的灵魂，生视频时标注"micro-expression flash"。
- 本库现共 **69 条**：基础情绪 8 + 复合情绪 16 + 进阶/复杂情绪 31 + 跨文化微表情 4 + AI 生成缺陷与规避 5 + 复合情绪微表情扩展 5，覆盖影视/短剧绝大多数表演场景。
