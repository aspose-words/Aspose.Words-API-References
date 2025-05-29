---
title: FieldToc.CaptionlessTableOfFiguresLabel
linktitle: CaptionlessTableOfFiguresLabel
articleTitle: CaptionlessTableOfFiguresLabel
second_title: Aspose.Words for .NET
description: 探索 FieldToc CaptionlessTableOfFiguresLabel 属性，自定义图表目录。轻松管理无标题的序列标识符！
type: docs
weight: 30
url: /zh/net/aspose.words.fields/fieldtoc/captionlesstableoffigureslabel/
---
## FieldToc.CaptionlessTableOfFiguresLabel property

获取或设置构建不包含标题标签和编号的图表时使用的序列标识符的名称。

```csharp
public string CaptionlessTableOfFiguresLabel { get; set; }
```

## 例子

显示如何设置序列标识符的名称。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);
fieldToc.CaptionlessTableOfFiguresLabel = "Test";

Assert.AreEqual(" TOC  \\a Test", fieldToc.GetFieldCode());
```

### 也可以看看

* class [FieldToc](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
