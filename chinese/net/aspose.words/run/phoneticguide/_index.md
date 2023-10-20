---
title: Run.PhoneticGuide
linktitle: PhoneticGuide
articleTitle: PhoneticGuide
second_title: 用于 .NET 的 Aspose.Words
description: Run PhoneticGuide 财产. 获得PhoneticGuide对象 在 C#.
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

演示如何获取拼音指南的属性。

```csharp
Document doc = new Document(MyDir + "Phonetic guide.docx");            

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;
// 在亚洲文本中使用拼音指南。
Assert.AreEqual(true, runs[0].IsPhoneticGuide);
Assert.AreEqual("base", runs[0].PhoneticGuide.BaseText);
Assert.AreEqual("ruby", runs[0].PhoneticGuide.RubyText);
```

### 也可以看看

* class [PhoneticGuide](../../phoneticguide/)
* class [Run](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
