---
title: HtmlLoadOptions.SupportVml
linktitle: SupportVml
articleTitle: SupportVml
second_title: Aspose.Words for .NET
description: 了解 HtmlLoadOptions SupportVml 属性如何通过启用 VML 图像支持来提高图形质量，从而增强您的 Web 体验。
type: docs
weight: 70
url: /zh/net/aspose.words.loading/htmlloadoptions/supportvml/
---
## HtmlLoadOptions.SupportVml property

获取或设置一个值，指示是否支持 VML 图像。

```csharp
public bool SupportVml { get; set; }
```

## 例子

展示如何在加载 HTML 文档时支持条件注释。

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// 如果值为真，那么我们在解析加载的文档时会考虑 VML 代码。
loadOptions.SupportVml = supportVml;

// 本文档包含“<!--[if gte vml 1]>”标签内的 JPEG 图像，
// 以及“<![if !vml]>”标签内的不同 PNG 图像。
// 如果我们将“SupportVml”标志设置为“true”，那么Aspose.Words 将加载 JPEG。
// 如果我们将此标志设置为“false”，那么 Aspose.Words 将仅加载 PNG。
Document doc = new Document(MyDir + "VML conditional.htm", loadOptions);

if (supportVml)
    Assert.AreEqual(ImageType.Jpeg, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
else
    Assert.AreEqual(ImageType.Png, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
```

### 也可以看看

* class [HtmlLoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
