---
title: PdfSaveOptions.TextCompression
second_title: Aspose.Words for .NET API 参考
description: PdfSaveOptions 财产. 指定用于文档中所有文本内容的压缩类型
type: docs
weight: 260
url: /zh/net/aspose.words.saving/pdfsaveoptions/textcompression/
---
## PdfSaveOptions.TextCompression property

指定用于文档中所有文本内容的压缩类型。

```csharp
public PdfTextCompression TextCompression { get; set; }
```

### 评论

默认为Flate.

保存未压缩的文档时显着增加输出大小。

### 例子

显示在将文档保存为 PDF 时如何应用文本压缩。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 100; i++)
    builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// 创建一个“PdfSaveOptions”对象，我们可以将它传递给文档的“Save”方法
// 修改该方法如何将文档转换为 .PDF。
PdfSaveOptions options = new PdfSaveOptions();

// 将“TextCompression”属性设置为“PdfTextCompression.None”以不应用任何
// 当我们将文档保存为 PDF 时压缩为文本。
// 将“TextCompression”属性设置为“PdfTextCompression.Flate”以应用 ZIP 压缩
// 当我们将文档保存为 PDF 时转换为文本。文件越大，这将产生的影响越大。
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

### 也可以看看

* enum [PdfTextCompression](../../pdftextcompression/)
* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../pdfsaveoptions/)
* 部件 [Aspose.Words](../../../)


