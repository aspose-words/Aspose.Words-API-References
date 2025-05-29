---
title: Paragraph.IsFormatRevision
linktitle: IsFormatRevision
articleTitle: IsFormatRevision
second_title: Aspose.Words for .NET
description: 了解 Microsoft Word 中的 IsFormatRevision 属性如何跟踪格式变化，确保准确的文档编辑和增强协作。
type: docs
weight: 90
url: /zh/net/aspose.words/paragraph/isformatrevision/
---
## Paragraph.IsFormatRevision property

如果在启用更改跟踪的情况下 Microsoft Word 中的对象格式发生更改，则返回 true。

```csharp
public bool IsFormatRevision { get; }
```

## 例子

展示如何检查某个段落是否是格式修订。

```csharp
Document doc = new Document(MyDir + "Format revision.docx");

// 本段是“格式”修订，当我们更改现有文本的格式时会发生这种情况
// 同时通过“审阅”->“跟踪更改”在 Microsoft Word 中跟踪修订。
Assert.True(doc.FirstSection.Body.FirstParagraph.IsFormatRevision);
```

### 也可以看看

* class [Paragraph](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
