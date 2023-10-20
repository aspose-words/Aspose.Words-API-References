---
title: DocumentBase.PageColor
linktitle: PageColor
articleTitle: PageColor
second_title: 用于 .NET 的 Aspose.Words
description: DocumentBase PageColor 财产. 获取或设置文档的页面颜色这个属性是一个更简单的版本BackgroundShape 在 C#.
type: docs
weight: 60
url: /zh/net/aspose.words/documentbase/pagecolor/
---
## DocumentBase.PageColor property

获取或设置文档的页面颜色。这个属性是一个更简单的版本[`BackgroundShape`](../backgroundshape/).

```csharp
public Color PageColor { get; set; }
```

## 评论

此属性提供了一种简单的方法来指定文档的纯色页面颜色。 设置此属性会创建并设置适当的颜色[`BackgroundShape`](../backgroundshape/)。

如果未设置页面颜色（例如文档中没有背景形状）则返回 Empty。

## 例子

演示如何设置文档所有页面的背景颜色。

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
