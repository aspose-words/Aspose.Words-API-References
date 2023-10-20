---
title: Paragraph.IsFormatRevision
linktitle: IsFormatRevision
articleTitle: IsFormatRevision
second_title: 用于 .NET 的 Aspose.Words
description: Paragraph IsFormatRevision 财产. 如果启用更改跟踪时在 Microsoft Word 中更改了对象的格式则返回 true 在 C#.
type: docs
weight: 90
url: /zh/net/aspose.words/paragraph/isformatrevision/
---
## Paragraph.IsFormatRevision property

如果启用更改跟踪时在 Microsoft Word 中更改了对象的格式，则返回 true。

```csharp
public bool IsFormatRevision { get; }
```

## 例子

显示如何检查段落是否为格式修订。

```csharp
Document doc = new Document(MyDir + "Format revision.docx");

// 这一段是“格式”修订，当我们改变现有文本的格式时发生
// 同时通过“审阅”跟踪 Microsoft Word 中的修订 -> “跟踪变化”。
Assert.True(doc.FirstSection.Body.FirstParagraph.IsFormatRevision);
```

### 也可以看看

* class [Paragraph](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
