---
title: StructuredDocumentTag.BuildingBlockCategory
linktitle: BuildingBlockCategory
articleTitle: BuildingBlockCategory
second_title: 用于 .NET 的 Aspose.Words
description: StructuredDocumentTag BuildingBlockCategory 财产. 为此指定构建块的类别SDTnode. 不能为空 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words.markup/structureddocumenttag/buildingblockcategory/
---
## StructuredDocumentTag.BuildingBlockCategory property

为此指定构建块的类别**SDT**node. 不能为空。

```csharp
public string BuildingBlockCategory { get; set; }
```

## 评论

访问此属性仅适用于BuildingBlockGallery和 DocPartObj SDT 类型。它是只读的**SDT**文档部分类型的.

对于所有其他 SDT 类型，将发生异常。

## 例子

展示如何插入结构化文档标签作为构建块，并设置其类别和图库。

```csharp
Document doc = new Document();

StructuredDocumentTag buildingBlockSdt =
    new StructuredDocumentTag(doc, SdtType.BuildingBlockGallery, MarkupLevel.Block)
    {
        BuildingBlockCategory = "Built-in",
        BuildingBlockGallery = "Table of Contents"
    };

doc.FirstSection.Body.AppendChild(buildingBlockSdt);

doc.Save(ArtifactsDir + "StructuredDocumentTag.BuildingBlockCategories.docx");
```

### 也可以看看

* class [StructuredDocumentTag](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
