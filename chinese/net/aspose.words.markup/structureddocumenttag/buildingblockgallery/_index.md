---
title: StructuredDocumentTag.BuildingBlockGallery
second_title: Aspose.Words for .NET API 参考
description: StructuredDocumentTag 财产. 指定构建块的类型 特殊测试. 不能无效的.
type: docs
weight: 40
url: /zh/net/aspose.words.markup/structureddocumenttag/buildingblockgallery/
---
## StructuredDocumentTag.BuildingBlockGallery property

指定构建块的类型 **特殊测试**. 不能`无效的`.

```csharp
public string BuildingBlockGallery { get; set; }
```

### 评论

访问该属性仅适用于BuildingBlockGallery和 DocPartObjSDT 类型。它是只读的 **特殊测试**文档部分类型的。

对于所有其他 SDT 类型，都会发生异常。

### 例子

演示如何插入结构化文档标签作为构建块，并设置其类别和库。

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
* 命名空间 [Aspose.Words.Markup](../../structureddocumenttag/)
* 部件 [Aspose.Words](../../../)


