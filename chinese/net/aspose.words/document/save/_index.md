---
title: Document.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words for .NET
description: 使用我们的智能保存方法轻松保存您的文档，根据文件扩展名自动选择正确的格式实现无缝存储。
type: docs
weight: 750
url: /zh/net/aspose.words/document/save/
---
## Save(*string*) {#save_2}

将文档保存为文件。根据扩展名自动确定保存格式。

```csharp
public SaveOutputParameters Save(string fileName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | 文档的名称。如果已存在具有指定文件名 the 的文档，则会覆盖现有文档。 |

### 返回值

您可以选择性使用的附加信息。

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

### 也可以看看

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## Save(*string, [SaveFormat](../../saveformat/)*) {#save_3}

将文档保存为指定格式的文件。

```csharp
public SaveOutputParameters Save(string fileName, SaveFormat saveFormat)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | 文档的名称。如果已存在具有指定文件名 the 的文档，则会覆盖现有文档。 |
| saveFormat | SaveFormat | 保存文档的格式。 |

### 返回值

您可以选择性使用的附加信息。

## 例子

展示如何从 DOCX 转换为 HTML 格式。

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToHtml.html", SaveFormat.Html);
```

### 也可以看看

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* enum [SaveFormat](../../saveformat/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## Save(*string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#save_4}

使用指定的保存选项将文档保存到文件。

```csharp
public SaveOutputParameters Save(string fileName, SaveOptions saveOptions)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | 文档的名称。如果已存在具有指定文件名 the 的文档，则会覆盖现有文档。 |
| saveOptions | SaveOptions | 指定控制文档保存方式的选项。可以是`无效的`。 |

### 返回值

您可以选择性使用的附加信息。

## 例子

展示如何使用 SaveOptions 提高渲染文档的质量。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 60;
builder.Writeln("Some text.");

SaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
doc.Save(ArtifactsDir + "Document.ImageSaveOptions.Default.jpg", options);

options.UseAntiAliasing = true;
options.UseHighQualityRendering = true;

doc.Save(ArtifactsDir + "Document.ImageSaveOptions.HighQuality.jpg", options);
```

展示如何将 PDF 转换为 .docx 并使用 SaveOptions 对象自定义保存过程。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.pdf");

// 加载我们刚刚保存的 PDF 文档，并将其转换为 .docx。
Document pdfDoc = new Document(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.pdf");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);

// 设置“密码”属性，使用密码加密保存的文档。
saveOptions.Password = "MyPassword";

pdfDoc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.docx", saveOptions);
```

展示如何将文档的每一页渲染为单独的 TIFF 图像。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// 创建一个“ImageSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档呈现为图像的方式。
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // 将“PageSet”属性设置为第一页的页码
    // 从哪里开始渲染文档。
    options.PageSet = new PageSet(i);
    // 以 2325x5325 像素和 600 dpi 导出页面。
    options.Resolution = 600;
    options.ImageSize = new Size(2325, 5325);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

展示如何将文档中的一页渲染为 JPEG 图像。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// 创建一个“ImageSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档呈现为图像的方式。
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
// 将“PageSet”设置为“1”以通过以下方式选择第二页
// 从零开始的索引来呈现文档。
options.PageSet = new PageSet(1);

// 当我们将文档保存为 JPEG 格式时，Aspose.Words 只会呈现一页。
// 此图像将包含从第二页开始的一页，
// 这只是原始文档的第二页。
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

展示如何在将文档保存为 JPEG 时配置压缩。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// 创建一个“ImageSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档呈现为图像的方式。
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);
// 将“JpegQuality”属性设置为“10”以在呈现文档时使用更强的压缩。
// 这将减小文档的文件大小，但图像将显示更明显的压缩伪影。
imageOptions.JpegQuality = 10;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// 将“JpegQuality”属性设置为“100”以在渲染文档时使用较弱的压缩。
// 这将提高图像的质量，但会增加文件大小。
imageOptions.JpegQuality = 100;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

展示如何将整个文档转换为具有文档大纲三个级别的 PDF。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入 1 至 5 级标题。
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;

builder.Writeln("Heading 1.2.2.1");
builder.Writeln("Heading 1.2.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.2.2.2.1");
builder.Writeln("Heading 1.2.2.2.2");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions options = new PdfSaveOptions();

// 输出的 PDF 文档将包含一个大纲，它是一个列出文档正文中标题的目录。
// 单击此大纲中的条目将带我们到其相应标题的位置。
// 将“HeadingsOutlineLevels”属性设置为“4”，以从大纲中排除所有级别高于 4 的标题。
options.OutlineOptions.HeadingsOutlineLevels = 4;

// 如果大纲条目在其自身和相同或较低级别下一个条目之间有更高级别的后续条目，
// 条目左侧会出现一个箭头。此条目是多个此类“子条目”的“所有者”。
// 在我们的文档中，第 5 个标题级别的大纲条目是第二个第 4 级大纲条目的子条目，
// 第 4 和第 5 个标题级条目是第二个第 3 级条目的子条目，依此类推。
// 在大纲中，我们可以点击“所有者”条目的箭头来折叠/展开其所有子条目。
// 将“ExpandedOutlineLevels”属性设置为“2”，以自动展开所有标题级别 2 及以下的大纲条目
// 当我们打开文档时，折叠所有级别和 3 及更高级别的条目。
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### 也可以看看

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## Save(*Stream, [SaveFormat](../../saveformat/)*) {#save}

使用指定格式将文档保存到流。

```csharp
public SaveOutputParameters Save(Stream stream, SaveFormat saveFormat)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | Stream | 流式传输文档的保存位置。 |
| saveFormat | SaveFormat | 保存文档的格式。 |

### 返回值

您可以选择性使用的附加信息。

## 例子

展示如何将文档保存到流中。

```csharp
Document doc = new Document(MyDir + "Document.docx");

using (MemoryStream dstStream = new MemoryStream())
{
    doc.Save(dstStream, SaveFormat.Docx);

    // 验证流是否包含该文档。
    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", new Document(dstStream).GetText().Trim());
}
```

展示如何通过流将文档保存为图像，然后从该流中读取图像。

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Font.Name = "Times New Roman";
            builder.Font.Size = 24;
            builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

            builder.InsertImage(ImageDir + "Logo.jpg");

#if NET461_OR_GREATER || JAVA
            using (MemoryStream stream = new MemoryStream())
            {
                doc.Save(stream, SaveFormat.Bmp);

                stream.Position = 0;

                // 将流读回到图像中。
                using (Image image = Image.FromStream(stream))
                {
                    Assert.AreEqual(ImageFormat.Bmp, image.RawFormat);
                    Assert.AreEqual(816, image.Width);
                    Assert.AreEqual(1056, image.Height);
                }
            }
#elif NET5_0_OR_GREATER
            using (MemoryStream stream = new MemoryStream())
            {
                doc.Save(stream, SaveFormat.Bmp);

                stream.Position = 0;

                SKCodec codec = SKCodec.Create(stream);
                Assert.AreEqual(SKEncodedImageFormat.Bmp, codec.EncodedFormat);

                stream.Position = 0;

                using (SKBitmap image = SKBitmap.Decode(stream))
                {
                    Assert.AreEqual(816, image.Width);
                    Assert.AreEqual(1056, image.Height);
                }
            }
#endif
```

### 也可以看看

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* enum [SaveFormat](../../saveformat/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## Save(*Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#save_1}

使用指定的保存选项将文档保存到流中。

```csharp
public SaveOutputParameters Save(Stream stream, SaveOptions saveOptions)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | Stream | 流式传输文档的保存位置。 |
| saveOptions | SaveOptions | 指定控制文档保存方式的选项。可以是`无效的` . 如果这是`无效的`，文档将以二进制DOC格式保存。 |

### 返回值

您可以选择性使用的附加信息。

## 例子

展示如何将文档中的部分页面转换为 PDF。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

using (Stream stream = File.Create(ArtifactsDir + "PdfSaveOptions.OnePage.pdf"))
{
    // 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
    // 修改该方法将文档转换为 .PDF 的方式。
    PdfSaveOptions options = new PdfSaveOptions();

    // 将“PageIndex”设置为“1”以从第二页开始呈现文档的一部分。
    options.PageSet = new PageSet(1);

    // 本文档将包含从第二页开始的一页，其中只包含第二页。
    doc.Save(stream, options);
}
```

### 也可以看看

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## Save(*HttpResponse, string, [ContentDisposition](../../contentdisposition/), [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#save_5}

将文档发送到客户端浏览器。

```csharp
public SaveOutputParameters Save(HttpResponse response, string fileName, 
    ContentDisposition contentDisposition, SaveOptions saveOptions)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| response | HttpResponse | 响应对象，用于保存文档。 |
| fileName | String | 将在客户端浏览器中显示的文档的名称。 名称不应包含路径。 |
| contentDisposition | ContentDisposition | 一个[`ContentDisposition`](../../contentdisposition/)值 that 指定文档在客户端浏览器中的呈现方式。 |
| saveOptions | SaveOptions | 指定控制文档保存方式的选项。可以是`无效的`。 |

### 返回值

您可以选择性使用的附加信息。

## 评论

在内部，此方法首先保存到内存流，然后复制到响应stream ，因为响应流不支持查找。

## 例子

展示如何执行邮件合并，然后将文档保存到客户端浏览器。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD FullName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Company ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Address ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

doc.MailMerge.Execute(new string[] { "FullName", "Company", "Address", "City" },
    new object[] { "James Bond", "MI5 Headquarters", "Milbank", "London" });

// 将文档发送到客户端浏览器。
//由于测试中 HttpResponse 为空而抛出。
Assert.Throws<ArgumentNullException>(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null));

// 我们需要手动关闭此响应，以确保保存后不会向文档添加任何多余的内容。
Assert.Throws<NullReferenceException>(() => response.End());
```

### 也可以看看

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* enum [ContentDisposition](../../contentdisposition/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
