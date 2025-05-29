---
title: DocumentBuilder.Underline
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words for .NET
description: 探索 DocumentBuilder 的“下划线”属性，轻松自定义字体样式。使用丰富的下划线选项，提升文档的专业外观。
type: docs
weight: 190
url: /zh/net/aspose.words/documentbuilder/underline/
---
## DocumentBuilder.Underline property

获取/设置当前字体的下划线类型。

```csharp
public Underline Underline { get; set; }
```

## 例子

展示如何格式化文档生成器插入的文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Underline = Underline.Dash;
builder.Font.Color = Color.Blue;
builder.Font.Size = 32;

// 构建器将格式应用于其当前段落以及随后添加的任何新文本。
builder.Writeln("Large, blue, and underlined text.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertUnderline.docx");
```

### 也可以看看

* enum [Underline](../../underline/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
