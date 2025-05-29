---
title: LoadOptions.LoadFormat
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: Aspose.Words for .NET
description: 探索 LoadOptions 的 LoadFormat 属性，轻松指定文档格式。使用默认的“自动”设置优化加载，实现流畅的性能。
type: docs
weight: 90
url: /zh/net/aspose.words.loading/loadoptions/loadformat/
---
## LoadOptions.LoadFormat property

指定要加载的文档的格式。 默认值为Auto.

```csharp
public LoadFormat LoadFormat { get; set; }
```

## 评论

建议您指定Auto值，并让 Aspose.Words 自动检测文件格式。如果您知道即将加载的文档的格式，可以明确指定格式，这将略微减少加载时间，因为自动检测格式会降低加载时间。如果您指定了明确的加载格式，但结果错误，则将调用自动检测并再次尝试加载文件。

## 例子

展示如何在打开 html 文档时指定基本 URI。

```csharp
// 假设我们要加载一个包含通过相对 URI 链接的图像的 .html 文档
// 但图像位于其他位置。在这种情况下，我们需要将相对 URI 解析为绝对 URI。
 // 我们可以使用 HtmlLoadOptions 对象提供基本 URI。
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// 当输入 .html 中的图像损坏时，我们的自定义基本 URI 帮助我们修复了链接。
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// 此输出文档将显示缺失的图像。
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

### 也可以看看

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [LoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
