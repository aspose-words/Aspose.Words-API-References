---
title: LoadOptions
linktitle: LoadOptions
articleTitle: LoadOptions
second_title: 用于 .NET 的 Aspose.Words
description: LoadOptions 构造函数. 使用默认值初始化此类的新实例 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words.loading/loadoptions/loadoptions/
---
## LoadOptions() {#constructor}

使用默认值初始化此类的新实例。

```csharp
public LoadOptions()
```

## 例子

演示如何使用基本 URI 打开包含来自流的图像的 HTML 文档。

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // 加载时传递基本文件夹的 URI
    // 这样就可以找到 HTML 文档中具有相对 URI 的任何图像。
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // 验证文档的第一个形状是否包含有效图像。
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

---

## LoadOptions(*string*) {#constructor_2}

使用指定的密码初始化此类的新实例以加载加密文档的快捷方式。

```csharp
public LoadOptions(string password)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| password | String | 打开加密文档的密码。可`无效的`或空字符串。 |

## 例子

演示如何加载加密的 Microsoft Word 文档。

```csharp
Document doc;

// 如果我们尝试在没有密码的情况下打开加密文档，Aspose.Words 会抛出异常。
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// 加载此类文档时，密码将使用 LoadOptions 对象传递给文档的构造函数。
LoadOptions options = new LoadOptions("docPassword");

// 使用 LoadOptions 对象加载加密文档有两种方法。
// 1 - 按文件名从本地文件系统加载文档：
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - 从流加载文档：
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

### 也可以看看

* class [LoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)

---

## LoadOptions(*[LoadFormat](../../../aspose.words/loadformat/), string, string*) {#constructor_1}

初始化此类新实例并将属性设置为指定值的快捷方式。

```csharp
public LoadOptions(LoadFormat loadFormat, string password, string baseUri)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| loadFormat | LoadFormat | 要加载的文档的格式。 |
| password | String | 打开加密文档的密码。可`无效的`或空字符串。 |
| baseUri | String | 将用于将相对 URI 解析为绝对 URI 的字符串。可`无效的`或空字符串。 |

## 例子

演示如何将网页另存为 .docx 文件。

```csharp
const string url = "https://www.aspose.com/";

using (HttpClient client = new HttpClient()) 
{
    var bytes = await client.GetByteArrayAsync(url);
    using (MemoryStream stream = new MemoryStream(bytes))
    {
        // URL 再次用作 baseUri，以确保正确检索任何相对图像路径。
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // 从流加载 HTML 文档并传递 LoadOptions 对象。
        Document doc = new Document(stream, options);

        // 在此阶段，我们可以读取和编辑文档的内容，然后将其保存到本地文件系统。
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

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
