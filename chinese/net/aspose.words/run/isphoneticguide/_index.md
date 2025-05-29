---
title: Run.IsPhoneticGuide
linktitle: IsPhoneticGuide
articleTitle: IsPhoneticGuide
second_title: Aspose.Words for .NET
description: 发现 IsPhoneticGuide，这是一个强大的工具，可以确定连续的文字是否作为语音指南，从而增强文本的清晰度和可读性。
type: docs
weight: 20
url: /zh/net/aspose.words/run/isphoneticguide/
---
## Run.IsPhoneticGuide property

获取一个布尔值，指示运行是否为语音指南。

```csharp
public bool IsPhoneticGuide { get; }
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

* class [Run](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
