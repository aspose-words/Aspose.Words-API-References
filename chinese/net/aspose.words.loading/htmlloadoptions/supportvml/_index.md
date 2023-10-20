---
title: HtmlLoadOptions.SupportVml
linktitle: SupportVml
articleTitle: SupportVml
second_title: 用于 .NET 的 Aspose.Words
description: HtmlLoadOptions SupportVml 财产. 获取或设置是否支持VML图像的值 在 C#.
type: docs
weight: 60
url: /zh/net/aspose.words.loading/htmlloadoptions/supportvml/
---
## HtmlLoadOptions.SupportVml property

获取或设置是否支持VML图像的值。

```csharp
public bool SupportVml { get; set; }
```

## 例子

展示如何在加载 HTML 文档时支持条件注释。

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// 如果值为真，那么我们在解析加载的文档时会考虑 VML 代码。
loadOptions.SupportVml = supportVml;

// 此文档在“<!--[if gte vml 1]>”中包含一个 JPEG 图像标签，
// 以及 "<![if !vml]>" 中的不同 PNG 图像标签。
// 如果我们将“SupportVml”标志设置为“true”，那么 Aspose.Words 将加载 JPEG。
// 如果我们将此标志设置为“false”，那么 Aspose.Words 将只加载 PNG。
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
