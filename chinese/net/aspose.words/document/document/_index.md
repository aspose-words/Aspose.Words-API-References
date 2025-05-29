---
title: Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words for .NET
description: 使用我们用户友好的文档构造器，轻松创建空白 Word 文档。立即简化您的写作流程！
type: docs
weight: 10
url: /zh/net/aspose.words/document/document/
---
## Document() {#constructor}

创建一个空白的 Word 文档。

```csharp
public Document()
```

## 评论

从资源中检索空白文档，默认情况下，生成的文档看起来更像是由Word2007. 此空白文档包含默认字体表、最小默认样式和潜在样式。

[`OptimizeFor`](../../../aspose.words.settings/compatibilityoptions/optimizefor/)方法可用于优化文档内容以及特定版本 MS Word 的默认 Aspose.Words 行为。

文档纸张大小默认为 Letter。如需更改页面设置，请使用 [`PageSetup`](../../section/pagesetup/)。

创建完成后即可使用[`DocumentBuilder`](../../documentbuilder/)轻松添加文档内容。

## 例子

展示如何使用字体属性来格式化文本。

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

展示如何创建简单文档。

```csharp
Document doc = new Document();

// 默认情况下，新的 Document 对象带有最小的节点集
// 需要开始添加内容，例如文本和形状：一个部分、一个正文和一个段落。
doc.AppendChild(new Section(doc))
    .AppendChild(new Body(doc))
    .AppendChild(new Paragraph(doc))
    .AppendChild(new Run(doc, "Hello world!"));
```

展示如何创建和加载文档。

```csharp
// 有两种方法可以使用 Aspose.Words 创建 Document 对象。
// 1 - 创建一个空白文档：
Document doc = new Document();

// 默认情况下，新的 Document 对象带有最小的节点集
// 需要开始添加内容，例如文本和形状：一个部分、一个正文和一个段落。
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - 加载本地文件系统中存在的文档：
doc = new Document(MyDir + "Document.docx");

// 加载的文档将包含我们可以访问和编辑的内容。
Assert.AreEqual("Hello World!", doc.FirstSection.Body.FirstParagraph.GetText().Trim());

// 加载过程中需要发生的一些操作，例如使用密码解密文档，
// 可以通过在加载文档时传递 LoadOptions 对象来完成。
doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));

Assert.AreEqual("Test encrypted document.", doc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## Document(*string*) {#constructor_3}

从文件中打开现有文档。自动检测文件格式。

```csharp
public Document(string fileName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | 要打开的文档的文件名。 |

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | 该文档格式无法识别或不受支持。 |
| [FileCorruptedException](../../filecorruptedexception/) | 该文档似乎已损坏，无法加载。 |
| Exception | 该文档存在问题，应报告给 Aspose.Words 开发人员。 |
| IOException | 存在输入/输出异常。 |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | 该文档已加密，需要密码才能打开，但您提供的密码不正确。 |
| ArgumentException | 文件名不能为空或空字符串。 |

## 例子

展示如何打开文档并将其转换为 .PDF。

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToPdf.pdf");
```

展示如何将 PDF 转换为 .docx。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

// 加载我们刚刚保存的 PDF 文档，并将其转换为 .docx。
Document pdfDoc = new Document(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

pdfDoc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.docx");
```

展示如何加载 PDF。

```csharp
Document doc = new Aspose.Words.Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

// 以下是使用 Aspose 产品加载 PDF 文档的两种方法。
// 1 - 作为 Aspose.Words 文档加载：
Document asposeWordsDoc = new Document(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

Assert.AreEqual("Hello world!", asposeWordsDoc.GetText().Trim());

// 2 - 作为 Aspose.Pdf 文档加载：
Aspose.Pdf.Document asposePdfDoc = new Aspose.Pdf.Document(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

TextFragmentAbsorber textFragmentAbsorber = new TextFragmentAbsorber();
asposePdfDoc.Pages.Accept(textFragmentAbsorber);

Assert.AreEqual("Hello world!", textFragmentAbsorber.Text.Trim());
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## Document(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_4}

从文件中打开现有文档。允许指定其他选项，例如加密密码。

```csharp
public Document(string fileName, LoadOptions loadOptions)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | 要打开的文档的文件名。 |
| loadOptions | LoadOptions | 加载文档时使用的附加选项。可以是`无效的`。 |

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | 该文档格式无法识别或不受支持。 |
| [FileCorruptedException](../../filecorruptedexception/) | 该文档似乎已损坏，无法加载。 |
| Exception | 该文档存在问题，应报告给 Aspose.Words 开发人员。 |
| IOException | 存在输入/输出异常。 |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | 该文档已加密，需要密码才能打开，但您提供的密码不正确。 |
| ArgumentException | 文件名不能为空或空字符串。 |

## 例子

展示如何加载加密的 Microsoft Word 文档。

```csharp
Document doc;

// 如果我们尝试在没有密码的情况下打开加密文档，Aspose.Words 会抛出异常。
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// 加载此类文档时，密码将通过 LoadOptions 对象传递给文档的构造函数。
LoadOptions options = new LoadOptions("docPassword");

// 有两种方法可以使用 LoadOptions 对象加载加密文档。
// 1 - 通过文件名从本地文件系统加载文档：
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - 从流中加载文档：
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

展示如何创建和加载文档。

```csharp
// 有两种方法可以使用 Aspose.Words 创建 Document 对象。
// 1 - 创建一个空白文档：
Document doc = new Document();

// 默认情况下，新的 Document 对象带有最小的节点集
// 需要开始添加内容，例如文本和形状：一个部分、一个正文和一个段落。
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - 加载本地文件系统中存在的文档：
doc = new Document(MyDir + "Document.docx");

// 加载的文档将包含我们可以访问和编辑的内容。
Assert.AreEqual("Hello World!", doc.FirstSection.Body.FirstParagraph.GetText().Trim());

// 加载过程中需要发生的一些操作，例如使用密码解密文档，
// 可以通过在加载文档时传递 LoadOptions 对象来完成。
doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));

Assert.AreEqual("Test encrypted document.", doc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### 也可以看看

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## Document(*Stream*) {#constructor_1}

从流中打开现有文档。自动检测文件格式。

```csharp
public Document(Stream stream)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | Stream | 从哪里加载文档的流。 |

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | 该文档格式无法识别或不受支持。 |
| [FileCorruptedException](../../filecorruptedexception/) | 该文档似乎已损坏，无法加载。 |
| Exception | 该文档存在问题，应报告给 Aspose.Words 开发人员。 |
| IOException | 存在输入/输出异常。 |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | 该文档已加密，需要密码才能打开，但您提供的密码不正确。 |
| ArgumentNullException | 流不能为空。 |
| NotSupportedException | 该流不支持读取或查找。 |
| ObjectDisposedException | 该流是一个已处置的对象。 |

## 评论

文档必须存储在流的开头。流必须支持随机定位。

## 例子

展示如何使用流加载文档。

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.docx"))
{
    Document doc = new Document(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

展示如何从 URL 加载文档。

```csharp
// 创建指向 Microsoft Word 文档的 URL。
const string url = "https://filesamples.com/samples/document/docx/sample3.docx”；

// 将文档下载到字节数组中，然后使用内存流将该数组加载到文档中。
using (WebClient webClient = new WebClient())
{
    byte[] dataBytes = webClient.DownloadData(url);

    using (MemoryStream byteStream = new MemoryStream(dataBytes))
    {
        Document doc = new Document(byteStream);

        // 在此阶段，我们可以读取和编辑文档的内容，然后将其保存到本地文件系统。
        Assert.AreEqual("There are eight section headings in this document. At the beginning, \"Sample Document\" is a level 1 heading. " +
                        "The main section headings, such as \"Headings\" and \"Lists\" are level 2 headings. " +
                        "The Tables section contains two sub-headings, \"Simple Table\" and \"Complex Table,\" which are both level 3 headings.",
            doc.FirstSection.Body.Paragraphs[3].GetText().Trim());

        doc.Save(ArtifactsDir + "Document.LoadFromWeb.docx");
    }
}
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## Document(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_2}

从流中打开现有文档。允许指定其他选项，例如加密密码。

```csharp
public Document(Stream stream, LoadOptions loadOptions)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | Stream | 从中加载文档的流。 |
| loadOptions | LoadOptions | 加载文档时使用的附加选项。可以是`无效的`。 |

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | 该文档格式无法识别或不受支持。 |
| [FileCorruptedException](../../filecorruptedexception/) | 该文档似乎已损坏，无法加载。 |
| Exception | 该文档存在问题，应报告给 Aspose.Words 开发人员。 |
| IOException | 存在输入/输出异常。 |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | 该文档已加密，需要密码才能打开，但您提供的密码不正确。 |
| ArgumentNullException | 流不能为空。 |
| NotSupportedException | 该流不支持读取或查找。 |
| ObjectDisposedException | 该流是一个已处置的对象。 |

## 评论

文档必须存储在流的开头。流必须支持随机定位。

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

展示如何将网页保存为 .docx 文件。

```csharp
const string url = "https://products.aspose.com/words/”;

using (WebClient client = new WebClient())
{
    var bytes = client.DownloadData(url);
    using (MemoryStream stream = new MemoryStream(bytes))
    {
        // URL 再次用作 baseUri，以确保正确检索任何相对图像路径。
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // 从流中加载 HTML 文档并传递 LoadOptions 对象。
        Document doc = new Document(stream, options);

        // 在此阶段，我们可以读取和编辑文档的内容，然后将其保存到本地文件系统。
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

展示如何加载加密的 Microsoft Word 文档。

```csharp
Document doc;

// 如果我们尝试在没有密码的情况下打开加密文档，Aspose.Words 会抛出异常。
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// 加载此类文档时，密码将通过 LoadOptions 对象传递给文档的构造函数。
LoadOptions options = new LoadOptions("docPassword");

// 有两种方法可以使用 LoadOptions 对象加载加密文档。
// 1 - 通过文件名从本地文件系统加载文档：
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - 从流中加载文档：
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

### 也可以看看

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
