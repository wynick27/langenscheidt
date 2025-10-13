## Langenscheidt

朗氏德汉双解大词典 文本
```
model_name = "gemini-2.5-pro"

system_instruction = """

OCR，识别提取pdf文件当中的文字。要求如下：

1. 页眉部分表示页码的阿拉伯数字，置于“〈〉”符号之中，（页眉同一行的其余索引文字删除不要），且把它放在输出最开始的位置，下面加一空行；假如不存在页码，用“〈?〉”占位表示。
2. 这是一本德汉词典，注意德文的正确拼写，不要忽略变音符号。
3. 页面左右分栏，识别阅读顺序为先左栏再右栏。
4. 正文部分首尾要完整识别，不要遗漏内容。每页起始部分的文字，无需和上一页连接在一起，按照原书排版自然断开即可。
5. 每一个词条的黑体字词头请放入【】符号内，以和词条的释义内容互相区分。
6. 在不同的词条之间空一行。
7. 识别结果以plain text格式输出，不要添加多余的markdown标记等。
8. 文中用放在方框内的Vi、Vt、Vt/i、Vimp等表示动词的类别，请把它们置于〔〕当中，分别用〔Vi〕〔Vt〕〔Vt/i〕〔Vimp〕表示。文中还有一些看上去特殊的符号，比如[口]，是[]的“口”字，表示口语，注意鉴别。
9. 你的默认输出长度限制是65536个token，把它用足，不要偷懒。
10. 每一个pdf文件有25页，需要全部识别，不要没完成任务就半途中断。

切记，下面这里是至关重要的要求和标准，务必满足：在同一页面内，同一词条中的相关释义文字要编辑合并在一个自然段落里，不可像图中那样因为版面限制而断开分行。

下面是一些识别结果的示例文本，供参考：

【auf.ra.gen】 (hat) 〔Vi〕 (不及物) etw. ragt auf etw. ragt in die Höhe(物作主语)耸立,突起

【auf.rap.peln, sich】 (hat) 〔Vr〕(反身) gespr[口]1. sich a. mühsam aufstehen吃力地站起来〈sich nach e-m Sturz a. 摔跤后吃力地站起来〉2. sich wieder a. sich nach e-r Krankheit langsam erholen 恢复健康,康复 3. sich zu etw. a. sich zu etw. aufraffen (3)強打精神去做 || NB(注意):ich rapple mich auf 我振作起来(打起精神)

【auf.rau.en】 [-rauən]; raute auf, hat aufgeraut; 〔Vt〕(及物) etw. a. etw. rau machen 使(表面)粗糙:aufgeraute Hände haben 有一双皮肤粗糙的手

【aufräumen】 (hat) 〔Vt/i〕(及物/不及物)1.(etw.) a. herumliegende Dinge an ihren Platz bringen, um Ordnung zu schaffen整理,收拾: den Schreibtisch a.收拾书桌; 〔Vi〕(不及物)2. mit etw. a. die Existenz od. Verbreitung von Vorurteilen, Einstellungen o. Ä. beenden 清除,消除,放弃:Moderne Wissenschaftler räumen mit altmodischen Ansichten auf 当代科学家放弃过时的观点 3. unter 〈Personen人(Dat)三格〉a. gespr[口]; mehrere Personen e-r Gruppe (von mst Kriminellen) töten od. verhaften:肃清,清洗(多用于罪犯) Die Soldaten hatten unter den Rebellen gründlich aufgeräumt 士兵彻底肃清了反叛者

【auf.rech.nen】 (hat) 〔Vt〕 (及物) etw. mit/gegen etw. a. Dinge miteinander vergleichen u. den Unterschied festlegen用……平衡,抵消,抵账 〈Konten, Summen, Schulden gegeneinander a.平衡账目,结清款项,相互抵消债务〉:Als die Forderungen gegeneinander aufgerechnet wurden, blieb nichts übrig 债务相互结清,没留任何尾巴

"""
```