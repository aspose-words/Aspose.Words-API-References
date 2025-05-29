---
title: PhoneticGuide Class
linktitle: PhoneticGuide
articleTitle: PhoneticGuide
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.PhoneticGuide 类，使用语音指南增强文本可读性。轻松提升用户体验和可访问性！
type: docs
weight: 5160
url: /zh/net/aspose.words/phoneticguide/
---
## PhoneticGuide class

代表语音指南。

```csharp
public class PhoneticGuide
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BaseText](../../aspose.words/phoneticguide/basetext/) { get; } | 获取语音指南的基本文本。 |
| [RubyText](../../aspose.words/phoneticguide/rubytext/) { get; } | 获取语音指南的 ruby 文本。 |

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

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
