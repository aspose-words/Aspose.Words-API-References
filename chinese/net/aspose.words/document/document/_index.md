---
title: Document
second_title: Aspose.Words for .NET API 参考
description: 创建一个空白 Word 文档
type: docs
weight: 10
url: /zh/net/aspose.words/document/document/
---
## Document() {#constructor}

创建一个空白 Word 文档。

```csharp
public Document()
```

### 评论

文档纸张尺寸默认为 Letter。如果要更改页面设置，请使用 [`Section.PageSetup`](../../section/pagesetup/).

创建后，您可以使用[`DocumentBuilder`](../../documentbuilder/)轻松添加文档内容。

### 例子

显示如何使用其字体属性格式化文本运行。

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

显示如何创建和加载文档。

```csharp
// 使用 Aspose.Words 创建 Document 对象有两种方式。
// 1 - 创建一个空白文档：
Document doc = new Document();

// 默认情况下，新文档对象带有最小的节点集
// 需要开始添加文本和形状等内容：Section、Body 和 Paragraph。
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - 加载本地文件系统中存在的文档：
doc = new Document(MyDir + "Document.docx");

// 加载的文档将包含我们可以访问和编辑的内容。
Assert.AreEqual("Hello World!", doc.FirstSection.Body.FirstParagraph.GetText().Trim());

// 加载过程中需要进行的一些操作，比如使用密码解密文档，
// 可以通过在加载文档时传递一个 LoadOptions 对象来完成。
doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));

Assert.AreEqual("Test encrypted document.", doc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../document/)
* 部件 [Aspose.Words](../../../)

---

## Document(string) {#constructor_3}

从文件中打开现有文档。自动检测文件格式

```csharp
public Document(string fileName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | 要打开的文档的文件名。 |

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | 文档格式无法识别或不受支持。 |
| [FileCorruptedException](../../filecorruptedexception/) | 文档似乎已损坏，无法加载。 |
| Exception | 文档存在问题，应报告给 Aspose.Words 开发人员。 |
| IOException | 存在输入/输出异常。 |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | 文档已加密，需要密码才能打开，但您提供的密码不正确。 |
| ArgumentException | 文件名不能为 null 或空字符串。 |

### 例子

演示如何打开文档并将其转换为 .PDF。

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

显示如何加载 PDF。

```csharp
Aspose.Words.Document doc = new Aspose.Words.Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

// 下面是使用 Aspose 产品加载 PDF 文档的两种方式。
// 1 - 加载为 Aspose.Words 文档：
Aspose.Words.Document asposeWordsDoc = new Aspose.Words.Document(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

Assert.AreEqual("Hello world!", asposeWordsDoc.GetText().Trim());

// 2 - 加载为 Aspose.Pdf 文档：
Aspose.Pdf.Document asposePdfDoc = new Aspose.Pdf.Document(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

TextFragmentAbsorber textFragmentAbsorber = new TextFragmentAbsorber();
asposePdfDoc.Pages.Accept(textFragmentAbsorber);

Assert.AreEqual("Hello world!", textFragmentAbsorber.Text.Trim());
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../document/)
* 部件 [Aspose.Words](../../../)

---

## Document(string, LoadOptions) {#constructor_4}

从文件中打开现有文档。允许指定其他选项，例如加密密码。

```csharp
public Document(string fileName, LoadOptions loadOptions)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | 要打开的文档的文件名。 |
| loadOptions | LoadOptions | 加载文档时使用的其他选项。可以为空。 |

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | 文档格式无法识别或不受支持。 |
| [FileCorruptedException](../../filecorruptedexception/) | 文档似乎已损坏，无法加载。 |
| Exception | 文档存在问题，应报告给 Aspose.Words 开发人员。 |
| IOException | 存在输入/输出异常。 |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | 文档已加密，需要密码才能打开，但您提供的密码不正确。 |
| ArgumentException | 文件名不能为 null 或空字符串。 |

### 例子

显示如何加载加密的 Microsoft Word 文档。

```csharp
Document doc;

// 如果我们尝试打开没有密码的加密文档，Aspose.Words 会抛出异常。
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// 当加载这样的文档时，密码会使用 LoadOptions 对象传递给文档的构造函数。
LoadOptions options = new LoadOptions("docPassword");

// 使用 LoadOptions 对象加载加密文档的方法有两种。
// 1 - 按文件名从本地文件系统加载文档：
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - 从流中加载文档：
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
```

显示如何创建和加载文档。

```csharp
// 使用 Aspose.Words 创建 Document 对象有两种方式。
// 1 - 创建一个空白文档：
Document doc = new Document();

// 默认情况下，新文档对象带有最小的节点集
// 需要开始添加文本和形状等内容：Section、Body 和 Paragraph。
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - 加载本地文件系统中存在的文档：
doc = new Document(MyDir + "Document.docx");

// 加载的文档将包含我们可以访问和编辑的内容。
Assert.AreEqual("Hello World!", doc.FirstSection.Body.FirstParagraph.GetText().Trim());

// 加载过程中需要进行的一些操作，比如使用密码解密文档，
// 可以通过在加载文档时传递一个 LoadOptions 对象来完成。
doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));

Assert.AreEqual("Test encrypted document.", doc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### 也可以看看

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../document/)
* 部件 [Aspose.Words](../../../)

---

## Document(Stream) {#constructor_1}

从流中打开现有文档。自动检测文件格式

```csharp
public Document(Stream stream)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | Stream | 流从哪里加载文档。 |

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | 文档格式无法识别或不受支持。 |
| [FileCorruptedException](../../filecorruptedexception/) | 文档似乎已损坏，无法加载。 |
| Exception | 文档存在问题，应报告给 Aspose.Words 开发人员。 |
| IOException | 存在输入/输出异常。 |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | 文档已加密，需要密码才能打开，但您提供的密码不正确。 |
| ArgumentNullException | 流不能为空。 |
| NotSupportedException | 该流不支持读取或查找。 |
| ObjectDisposedException | 流是一个已处置的对象。 |

### 评论

文档必须存储在流的开头。流必须支持随机定位。

### 例子

展示如何使用流加载文档。

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.docx"))
{
    Document doc = new Document(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

显示如何从 URL 加载文档。

```csharp
// 创建一个指向 Microsoft Word 文档的 URL。
const string url = "https://omextemplates.content.office.net/support/templates/en-us/tf16402488.dotx";

// 将文档下载到字节数组中，然后使用内存流将该数组加载到文档中。
using (WebClient webClient = new WebClient())
{
    byte[] dataBytes = webClient.DownloadData(url);

    using (MemoryStream byteStream = new MemoryStream(dataBytes))
    {
        Document doc = new Document(byteStream);

        // 在这个阶段，我们可以读取和编辑文档的内容，然后将其保存到本地文件系统。
        Assert.AreEqual("Use this section to highlight your relevant passions, activities, and how you like to give back. " +
                        "It’s good to include Leadership and volunteer experiences here. " +
                        "Or show off important extras like publications, certifications, languages and more.",
            doc.FirstSection.Body.Paragraphs[4].GetText().Trim());

        doc.Save(ArtifactsDir + "Document.LoadFromWeb.docx");
    }
}
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../document/)
* 部件 [Aspose.Words](../../../)

---

## Document(Stream, LoadOptions) {#constructor_2}

从流中打开现有文档。允许指定其他选项，例如加密密码。

```csharp
public Document(Stream stream, LoadOptions loadOptions)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | Stream | 从中加载文档的流。 |
| loadOptions | LoadOptions | 加载文档时使用的其他选项。可以为空。 |

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | 文档格式无法识别或不受支持。 |
| [FileCorruptedException](../../filecorruptedexception/) | 文档似乎已损坏，无法加载。 |
| Exception | 文档存在问题，应报告给 Aspose.Words 开发人员。 |
| IOException | 存在输入/输出异常。 |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | 文档已加密，需要密码才能打开，但您提供的密码不正确。 |
| ArgumentNullException | 流不能为空。 |
| NotSupportedException | 该流不支持读取或查找。 |
| ObjectDisposedException | 流是一个已处置的对象。 |

### 评论

文档必须存储在流的开头。流必须支持随机定位。

### 例子

显示如何将网页另存为 .docx 文件。

```csharp
const string url = "http://www.aspose.com/";

using (WebClient client = new WebClient()) 
{ 
    using (MemoryStream stream = new MemoryStream(client.DownloadData(url)))
    {
        // 该 URL 再次用作 baseUri，以确保正确检索任何相对图像路径。
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // 从流中加载 HTML 文档并传递 LoadOptions 对象。
        Document doc = new Document(stream, options);

        // 在这个阶段，我们可以读取和编辑文档的内容，然后将其保存到本地文件系统。
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

演示如何使用基本 URI 打开包含来自流的图像的 HTML 文档。

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // 在加载时传递基本文件夹的 URI
    // 以便可以找到 HTML 文档中具有相对 URI 的任何图像。
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

显示如何加载加密的 Microsoft Word 文档。

```csharp
Document doc;

// 如果我们尝试打开没有密码的加密文档，Aspose.Words 会抛出异常。
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// 当加载这样的文档时，密码会使用 LoadOptions 对象传递给文档的构造函数。
LoadOptions options = new LoadOptions("docPassword");

// 使用 LoadOptions 对象加载加密文档的方法有两种。
// 1 - 按文件名从本地文件系统加载文档：
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - 从流中加载文档：
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
```

### 也可以看看

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../document/)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
