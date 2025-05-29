---
title: IStructuredDocumentTag.SdtType
linktitle: SdtType
articleTitle: SdtType
second_title: Aspose.Words for .NET
description: 发现 IStructuredDocumentTag SdtType 属性，轻松识别结构化文档标签的类型，从而增强文档管理。
type: docs
weight: 120
url: /zh/net/aspose.words.markup/istructureddocumenttag/sdttype/
---
## IStructuredDocumentTag.SdtType property

获取此类型**结构化文档标签**.

```csharp
public SdtType SdtType { get; }
```

## 例子

展示如何获取结构化文档标签的类型。

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

List<StructuredDocumentTag> tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true)
    .OfType<StructuredDocumentTag>().ToList();

Assert.AreEqual(SdtType.RepeatingSection, tags[0].SdtType);
Assert.AreEqual(SdtType.RepeatingSectionItem, tags[1].SdtType);
Assert.AreEqual(SdtType.RichText, tags[2].SdtType);
```

### 也可以看看

* enum [SdtType](../../sdttype/)
* interface [IStructuredDocumentTag](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
