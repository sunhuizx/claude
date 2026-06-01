# 表演数据库 · 微表情（Performance / Micro-Expressions）

> 原子库 · 目标 ~55 条 ｜ 底层依据：**FACS 面部动作编码系统**（Action Unit, AU）。
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

## 使用提示
- **强度 = 微动作的幅度 × 数量**：隐忍=幅度小、单一部位；爆发=幅度大、多部位联动。
- **复合情绪靠"矛盾"取胜**：嘴笑+眉悲=强颜欢笑，是最高级的表演细节。
- **微表情泄漏**（一闪而过的真实情绪）是「撒谎/强装」类的灵魂，生视频时标注"micro-expression flash"。
- 本库现共 **55 条**：基础情绪 8 + 复合情绪 16 + 进阶/复杂情绪 31，覆盖影视/短剧绝大多数表演场景。
