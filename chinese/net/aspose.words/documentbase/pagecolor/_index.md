---
title: DocumentBase.PageColor
linktitle: PageColor
articleTitle: PageColor
second_title: Aspose.Words for .NET
description: 探索 DocumentBase 的 PageColor 属性，轻松自定义文档的页面颜色。这项用户友好的功能简化了设计！
type: docs
weight: 70
url: /zh/net/aspose.words/documentbase/pagecolor/
---
## DocumentBase.PageColor property

获取或设置文档的页面颜色。此属性是[`BackgroundShape`](../backgroundshape/).

```csharp
public Color PageColor { get; set; }
```

## 评论

此属性提供了一种为文档指定纯色页面颜色的简单方法。 设置此属性可创建并设置适当的[`BackgroundShape`](../backgroundshape/)。

如果未设置页面颜色（例如文档中没有背景形状）返回 Empty。

## 例子

展示如何设置文档所有页面的背景颜色。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.PageColor = System.Drawing.Color.LightGray;

doc.Save(ArtifactsDir + "DocumentBase.SetPageColor.docx");
```

### 也可以看看

* class [DocumentBase](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
