---
title: IStructuredDocumentTag.Appearance
linktitle: Appearance
articleTitle: Appearance
second_title: Aspose.Words for .NET
description: 发现 IStructuredDocumentTag 外观属性来定制和增强您的结构化文档标签，以改善用户体验。
type: docs
weight: 10
url: /zh/net/aspose.words.markup/istructureddocumenttag/appearance/
---
## IStructuredDocumentTag.Appearance property

获取或设置结构化文档标签的外观。

```csharp
public SdtAppearance Appearance { get; set; }
```

## 例子

展示如何在内容周围显示标签。

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");
StructuredDocumentTagRangeStart tag =
    doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true) as StructuredDocumentTagRangeStart;

if (tag.Appearance == SdtAppearance.Hidden)
    tag.Appearance = SdtAppearance.Tags;
```

### 也可以看看

* enum [SdtAppearance](../../sdtappearance/)
* interface [IStructuredDocumentTag](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
