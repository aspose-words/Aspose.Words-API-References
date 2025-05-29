---
title: Watermarker.SetText
linktitle: SetText
articleTitle: SetText
second_title: Aspose.Words for .NET
description: 使用我们的 Watermarker SetText 方法增强您的文档。轻松添加可自定义的文本水印，提升品牌形象和专业性。
type: docs
weight: 30
url: /zh/net/aspose.words.lowcode/watermarker/settext/
---
## SetText(*string, string, string*) {#settext_4}

在文档中添加文本水印。

```csharp
public static void SetText(string inputFileName, string outputFileName, string watermarkText)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 输出文件名。 |
| watermarkText | String | 显示为水印的文本。 |

## 评论

如果输出格式为图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则输出的每一页都将保存为单独的文件。指定的输出文件名将用于生成每个部分的文件名，并遵循以下规则：outputFile_partIndex.extension。

如果输出格式为 TIFF，则输出将保存为单个多帧 TIFF 文件。

## 例子

显示如何在文档中插入水印文本。

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.1.docx", watermarkText);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.2.docx", SaveFormat.Docx, watermarkText);
TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
watermarkOptions.Color = Color.Red;
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.3.docx", watermarkText, watermarkOptions);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.4.docx", SaveFormat.Docx, watermarkText, watermarkOptions);
```

### 也可以看看

* class [Watermarker](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## SetText(*string, string, string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext_5}

使用选项在文档中添加文本水印。

```csharp
public static void SetText(string inputFileName, string outputFileName, string watermarkText, 
    TextWatermarkOptions options)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 输出文件名。 |
| watermarkText | String | 显示为水印的文本。 |
| options | TextWatermarkOptions | 定义文本水印的附加选项。 |

## 评论

如果输出格式为图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则输出的每一页都将保存为单独的文件。指定的输出文件名将用于生成每个部分的文件名，并遵循以下规则：outputFile_partIndex.extension。

如果输出格式为 TIFF，则输出将保存为单个多帧 TIFF 文件。

## 例子

显示如何在文档中插入水印文本。

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.1.docx", watermarkText);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.2.docx", SaveFormat.Docx, watermarkText);
TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
watermarkOptions.Color = Color.Red;
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.3.docx", watermarkText, watermarkOptions);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.4.docx", SaveFormat.Docx, watermarkText, watermarkOptions);
```

### 也可以看看

* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## SetText(*string, string, [SaveFormat](../../../aspose.words/saveformat/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext_2}

使用选项和指定的保存格式在文档中添加文本水印。

```csharp
public static void SetText(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    string watermarkText, TextWatermarkOptions options = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 输出文件名。 |
| saveFormat | SaveFormat | 保存格式。 |
| watermarkText | String | 显示为水印的文本。 |
| options | TextWatermarkOptions | 定义文本水印的附加选项。 |

## 评论

如果输出格式为图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则输出的每一页都将保存为单独的文件。指定的输出文件名将用于生成每个部分的文件名，并遵循以下规则：outputFile_partIndex.extension。

如果输出格式为 TIFF，则输出将保存为单个多帧 TIFF 文件。

## 例子

显示如何在文档中插入水印文本。

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.1.docx", watermarkText);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.2.docx", SaveFormat.Docx, watermarkText);
TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
watermarkOptions.Color = Color.Red;
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.3.docx", watermarkText, watermarkOptions);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.4.docx", SaveFormat.Docx, watermarkText, watermarkOptions);
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## SetText(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext_3}

使用选项和指定的保存格式在文档中添加文本水印。

```csharp
public static void SetText(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    string watermarkText, TextWatermarkOptions options = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 输出文件名。 |
| saveOptions | SaveOptions | 保存选项。 |
| watermarkText | String | 显示为水印的文本。 |
| options | TextWatermarkOptions | 定义文本水印的附加选项。 |

## 评论

如果输出格式为图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则输出的每一页都将保存为单独的文件。指定的输出文件名将用于生成每个部分的文件名，并遵循以下规则：outputFile_partIndex.extension。

如果输出格式为 TIFF，则输出将保存为单个多帧 TIFF 文件。

### 也可以看看

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## SetText(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext}

使用选项从流中将文本水印添加到文档中。

```csharp
public static void SetText(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    string watermarkText, TextWatermarkOptions options = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | Stream | 输入流。 |
| outputStream | Stream | 输出流。 |
| saveFormat | SaveFormat | 保存格式。 |
| watermarkText | String | 显示为水印的文本。 |
| options | TextWatermarkOptions | 定义文本水印的附加选项。 |

## 评论

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则只有输出的第一页会保存到指定的流。

如果输出格式为 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流。

## 例子

展示如何从流中将水印文本插入到文档中。

```csharp
string watermarkText = "This is a watermark";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.WatermarkTextStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Watermarker.SetText(streamIn, streamOut, SaveFormat.Docx, watermarkText);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.WatermarkTextStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
    {
        TextWatermarkOptions options = new TextWatermarkOptions();
        options.Color = Color.Red;
        Watermarker.SetText(streamIn, streamOut, SaveFormat.Docx, watermarkText, options);
    }
}
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## SetText(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext_1}

使用选项从流中将文本水印添加到文档中。

```csharp
public static void SetText(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    string watermarkText, TextWatermarkOptions options = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | Stream | 输入流。 |
| outputStream | Stream | 输出流。 |
| saveOptions | SaveOptions | 保存选项。 |
| watermarkText | String | 显示为水印的文本。 |
| options | TextWatermarkOptions | 定义文本水印的附加选项。 |

## 评论

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则只有输出的第一页会保存到指定的流。

如果输出格式为 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流。

### 也可以看看

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)
