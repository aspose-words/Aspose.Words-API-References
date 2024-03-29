---
title: Run.IsPhoneticGuide
linktitle: IsPhoneticGuide
articleTitle: IsPhoneticGuide
second_title: 用于 .NET 的 Aspose.Words
description: Run IsPhoneticGuide 财产. 获取一个布尔值指示该运行是语音指南 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words/run/isphoneticguide/
---
## Run.IsPhoneticGuide property

获取一个布尔值，指示该运行是语音指南。

```csharp
public bool IsPhoneticGuide { get; }
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

* class [Run](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
