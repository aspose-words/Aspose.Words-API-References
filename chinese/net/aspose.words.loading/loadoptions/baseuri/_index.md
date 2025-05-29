---
title: LoadOptions.BaseUri
linktitle: BaseUri
articleTitle: BaseUri
second_title: Aspose.Words for .NET
description: 探索 LoadOptions BaseUri 属性，轻松将文档中的相对 URI 转换为绝对 URI。立即增强您的 URI 管理！
type: docs
weight: 20
url: /zh/net/aspose.words.loading/loadoptions/baseuri/
---
## LoadOptions.BaseUri property

获取或设置用于在需要时将文档中找到的相对 URI 解析为绝对 URI 的字符串。 可以`无效的`或空字符串。默认为`无效的`.

```csharp
public string BaseUri { get; set; }
```

## 评论

在下列情况下，此属性用于将相对 URI 解析为绝对 URI：

1. 从流加载 HTML 文档时，如果文档包含带有 相对 URI 的图像，并且没有在 BASE HTML 元素中指定基本 URI。
2. 将文档保存为 PDF 和其他格式时，检索使用相对 URIs 链接的图像，以便将图像保存到输出文档中。

## 例子

展示如何使用基本 URI 从流中打开包含图像的 HTML 文档。

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // 加载时传递基本文件夹的 URI
    // 这样就可以找到 HTML 文档中具有相对 URI 的任何图像。
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // 验证文档的第一个形状是否包含有效的图像。
    Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    Assert.IsTrue(shape.IsImage);
    Assert.IsNotNull(shape.ImageData.ImageBytes);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Width), 0.01);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Height), 0.01);
}
```

### 也可以看看

* class [LoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
