---
title: PhoneticGuide.RubyText
linktitle: RubyText
articleTitle: RubyText
second_title: 用于 .NET 的 Aspose.Words
description: PhoneticGuide RubyText 财产. 获取拼音指南的拼音文本 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words/phoneticguide/rubytext/
---
## PhoneticGuide.RubyText property

获取拼音指南的拼音文本。

```csharp
public string RubyText { get; }
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

* class [PhoneticGuide](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
