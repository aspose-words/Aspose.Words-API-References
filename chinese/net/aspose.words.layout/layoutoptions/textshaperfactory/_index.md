---
title: LayoutOptions.TextShaperFactory
linktitle: TextShaperFactory
articleTitle: TextShaperFactory
second_title: Aspose.Words for .NET
description: 探索 LayoutOptions 的 TextShaperFactory 属性，实现高级排版效果。使用可自定义的 ITextShaperFactory 实现增强渲染效果。
type: docs
weight: 100
url: /zh/net/aspose.words.layout/layoutoptions/textshaperfactory/
---
## LayoutOptions.TextShaperFactory property

获取或设置[`ITextShaperFactory`](../../../aspose.words.shaping/itextshaperfactory/)用于高级排版渲染功能的实现。

```csharp
public ITextShaperFactory TextShaperFactory { get; set; }
```

## 例子

展示如何使用 HarfBuzz 文本整形引擎支持 OpenType 功能。

```csharp
Document doc = new Document(MyDir + "OpenType text shaping.docx");

// Aspose.Words 可以使用外部提供的文本整形器对象，
// 代表字体并计算文本的形状信息。
// 对于使用多种字体的文档来说，文本整形器工厂是必需的。
// 当文本整形器工厂设置时，布局使用 OpenType 功能。
// 实例属性返回包装 HarfBuzzTextShaperFactory 的静态 BasicTextShaperCache 对象。
doc.LayoutOptions.TextShaperFactory = HarfBuzzTextShaperFactory.Instance;

// 目前，导出为 PDF 或 XPS 格式时正在进行文本整形。
doc.Save(ArtifactsDir + "Document.OpenType.pdf");
```

### 也可以看看

* interface [ITextShaperFactory](../../../aspose.words.shaping/itextshaperfactory/)
* class [LayoutOptions](../)
* 命名空间 [Aspose.Words.Layout](../../../aspose.words.layout/)
* 部件 [Aspose.Words](../../../)
