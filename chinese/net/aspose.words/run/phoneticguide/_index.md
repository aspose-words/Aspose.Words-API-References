---
title: Run.PhoneticGuide
linktitle: PhoneticGuide
articleTitle: PhoneticGuide
second_title: Aspose.Words for .NET
description: 使用 PhoneticGuide 解锁无缝发音。获取个性化语音洞察，提升您的语言技能和沟通能力。
type: docs
weight: 40
url: /zh/net/aspose.words/run/phoneticguide/
---
## Run.PhoneticGuide property

获得`PhoneticGuide`对象.

```csharp
public PhoneticGuide PhoneticGuide { get; }
```

## 例子

展示如何获取语音指南的属性。

```csharp
Document doc = new Document(MyDir + "Phonetic guide.docx");

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;
// 在亚洲文本中使用语音指南。
Assert.AreEqual(true, runs[0].IsPhoneticGuide);

PhoneticGuide phoneticGuide = runs[0].PhoneticGuide;
Assert.AreEqual("base", phoneticGuide.BaseText);
Assert.AreEqual("ruby", phoneticGuide.RubyText);
```

### 也可以看看

* class [PhoneticGuide](../../phoneticguide/)
* class [Run](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
