---
title: StructuredDocumentTag.SdtType
second_title: Aspose.Words for .NET API 参考
description: StructuredDocumentTag 财产. 获取 this 的类型 结构化文档标签.
type: docs
weight: 250
url: /zh/net/aspose.words.markup/structureddocumenttag/sdttype/
---
## StructuredDocumentTag.SdtType property

获取 this 的类型 **结构化文档标签**.

```csharp
public SdtType SdtType { get; }
```

### 例子

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
* class [StructuredDocumentTag](../)
* 命名空间 [Aspose.Words.Markup](../../structureddocumenttag/)
* 部件 [Aspose.Words](../../../)


