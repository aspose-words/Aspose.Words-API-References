---
title: LoadOptions.LoadFormat
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: 用于 .NET 的 Aspose.Words
description: LoadOptions LoadFormat 财产. 指定要加载的文档的格式 默认为Auto 在 C#.
type: docs
weight: 90
url: /zh/net/aspose.words.loading/loadoptions/loadformat/
---
## LoadOptions.LoadFormat property

指定要加载的文档的格式。 默认为Auto.

```csharp
public LoadFormat LoadFormat { get; set; }
```

## 评论

建议您指定Auto值并让 Aspose.Words 自动检测 文件格式。如果您知道要加载的文档的格式，则可以显式指定 format ，这将通过与自动检测格式相关的开销稍微减少加载时间。 如果您指定显式加载格式，它将变成如果错误，将调用自动检测并尝试加载该文件。

## 例子

演示如何在打开 html 文档时指定基本 URI。

```csharp
// 假设我们要加载一个 .html 文档，其中包含通过相对 URI 链接的图像
// 当图像位于不同位置时。在这种情况下，我们需要将相对 URI 解析为绝对 URI。
 // 我们可以使用 HtmlLoadOptions 对象提供基本 URI。
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// 虽然输入 .html 中的图像已损坏，但我们的自定义基本 URI 帮助我们修复了链接。
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// 此输出文档将显示丢失的图像。
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

### 也可以看看

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [LoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
