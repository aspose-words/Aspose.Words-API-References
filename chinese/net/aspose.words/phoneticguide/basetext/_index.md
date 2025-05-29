---
title: PhoneticGuide.BaseText
linktitle: BaseText
articleTitle: BaseText
second_title: Aspose.Words for .NET
description: 探索 PhoneticGuide BaseText 属性，轻松访问和增强语音指南基础文本，从而提高清晰度和沟通能力。
type: docs
weight: 10
url: /zh/net/aspose.words/phoneticguide/basetext/
---
## PhoneticGuide.BaseText property

获取语音指南的基本文本。

```csharp
public string BaseText { get; }
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

* class [PhoneticGuide](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
