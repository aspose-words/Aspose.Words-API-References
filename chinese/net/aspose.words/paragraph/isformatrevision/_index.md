---
title: Paragraph.IsFormatRevision
linktitle: IsFormatRevision
articleTitle: IsFormatRevision
second_title: 用于 .NET 的 Aspose.Words
description: Paragraph IsFormatRevision 财产. 如果在启用更改跟踪的情况下在 Microsoft Word 中更改了对象的格式则返回 true 在 C#.
type: docs
weight: 90
url: /zh/net/aspose.words/paragraph/isformatrevision/
---
## Paragraph.IsFormatRevision property

如果在启用更改跟踪的情况下在 Microsoft Word 中更改了对象的格式，则返回 true。

```csharp
public bool IsFormatRevision { get; }
```

## 例子

演示如何检查段落是否是格式修订版。

```csharp
Document doc = new Document(MyDir + "Format revision.docx");

// 本段是“格式”修订，当我们更改现有文本的格式时会发生这种情况
// 在 Microsoft Word 中通过“审阅”跟踪修订时 -> “跟踪变化”。
Assert.True(doc.FirstSection.Body.FirstParagraph.IsFormatRevision);
```

### 也可以看看

* class [Paragraph](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
