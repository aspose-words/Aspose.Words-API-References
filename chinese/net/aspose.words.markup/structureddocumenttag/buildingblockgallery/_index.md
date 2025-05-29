---
title: StructuredDocumentTag.BuildingBlockGallery
linktitle: BuildingBlockGallery
articleTitle: BuildingBlockGallery
second_title: Aspose.Words for .NET
description: 探索 StructuredDocumentTag BuildingBlockGallery 属性，定义 SDT 的构建块类型。确保文档无缝定制！
type: docs
weight: 40
url: /zh/net/aspose.words.markup/structureddocumenttag/buildingblockgallery/
---
## StructuredDocumentTag.BuildingBlockGallery property

指定此构建块的类型**特殊和差别待遇**. 不能`无效的`.

```csharp
public string BuildingBlockGallery { get; set; }
```

## 评论

访问此属性仅适用于BuildingBlockGalleryand DocPartObjSDT 类型。对于**特殊和差别待遇**文档部分类型。

对于所有其他 SDT 类型，都会发生异常。

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
