---
title: PhoneticGuide.RubyText
linktitle: RubyText
articleTitle: RubyText
second_title: Aspose.Words for .NET
description: 探索 PhoneticGuide RubyText 属性来访问和增强 ruby 文本，从而提高应用程序中的语音清晰度。
type: docs
weight: 20
url: /zh/net/aspose.words/phoneticguide/rubytext/
---
## PhoneticGuide.RubyText property

获取语音指南的 ruby 文本。

```csharp
public string RubyText { get; }
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
