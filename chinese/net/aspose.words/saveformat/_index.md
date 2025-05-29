---
title: SaveFormat Enum
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.SaveFormat 枚举以轻松选择文档保存格式，增强文件管理和无缝工作流程的兼容性。
type: docs
weight: 5580
url: /zh/net/aspose.words/saveformat/
---
## SaveFormat enumeration

表示文档保存的格式。

```csharp
public enum SaveFormat
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Unknown | `0` | 默认，文件格式的值无效。 |
| Doc | `10` | 将文档保存为 Microsoft Word 97 - 2007 文档格式。 |
| Dot | `11` | 将文档保存为 Microsoft Word 97 - 2007 模板格式。 |
| Docx | `20` | 将文档另存为 Office Open XML WordprocessingML 文档（无宏）。 |
| Docm | `21` | 将文档保存为 Office Open XML WordprocessingML 启用宏的文档。 |
| Dotx | `22` | 将文档保存为 Office Open XML WordprocessingML 模板（无宏）。 |
| Dotm | `23` | 将文档保存为 Office Open XML WordprocessingML 启用宏的模板。 |
| FlatOpc | `24` | 将文档另存为存储在平面 XML 文件（而不是 ZIP 包）中的 Office Open XML WordprocessingML。 |
| FlatOpcMacroEnabled | `25` | 将文档另存为 Office Open XML WordprocessingML 启用宏的文档，该文档存储在平面 XML 文件而不是 ZIP 包中。 |
| FlatOpcTemplate | `26` | 将文档另存为 Office Open XML WordprocessingML 模板（无宏），存储在平面 XML 文件而不是 ZIP 包中。 |
| FlatOpcTemplateMacroEnabled | `27` | 将文档另存为 Office Open XML WordprocessingML 启用宏的模板，该模板存储在平面 XML 文件而不是 ZIP 包中。 |
| Rtf | `30` | 将文档保存为 RTF 格式。 所有 7 位以上的字符均转义为十六进制或 Unicode 字符。 |
| WordML | `31` | 将文档保存为 Microsoft Word 2003 WordprocessingML 格式。 |
| Pdf | `40` | 将文档保存为 PDF（Adobe 便携式文档）格式。 |
| Xps | `41` | 以 XPS（XML 纸张规范）格式保存文档。 |
| XamlFixed | `42` | 将文档以可扩展应用程序标记语言 (XAML) 格式保存为固定文档。 |
| Svg | `44` | 以 Svg（可缩放矢量图形）格式保存文档。 |
| HtmlFixed | `45` | 使用绝对定位元素以 HTML 格式保存文档 |
| OpenXps | `46` | 以 OpenXPS (Ecma-388) 格式保存文档。 |
| Ps | `47` | 以 PS (PostScript) 格式保存文档。 |
| Pcl | `48` | 以 PCL（打印机控制语言）格式保存文档。 |
| Html | `50` | 以 HTML 格式保存文档。 |
| Mhtml | `51` | 以 MHTML（Web 存档）格式保存文档。 |
| Epub | `52` | 将文档保存为 EPUB 格式。 |
| Azw3 | `53` | 以 AZW3 格式保存文档。 |
| Mobi | `54` | 以 MOBI 格式保存文档。 |
| Odt | `60` | 将文档保存为 ODF 文本文档。 |
| Ott | `61` | 将文档保存为 ODF 文本文档模板。 |
| Text | `70` | 以纯文本格式保存文档。 |
| XamlFlow | `71` | **测试版。**将文档以可扩展应用程序标记语言 (XAML) 格式保存为流文档。 |
| XamlFlowPack | `72` | **测试版。**将文档以可扩展应用程序标记语言 (XAML) 包格式保存为流文档。 |
| Markdown | `73` | 以 Markdown 格式保存文档。 |
| Xlsx | `80` | 将文档保存为 Office Open XML SpreadsheetML 文档（无宏）。 |
| Tiff | `100` | 呈现文档的一页或多页并将其保存为单页或多页 TIFF 文件。 |
| Png | `101` | 渲染文档的一页并将其保存为 PNG 文件。 |
| Bmp | `102` | 渲染文档的一页并将其保存为 BMP 文件。 |
| Emf | `103` | 渲染文档的一页并将其保存为矢量 EMF（增强元文件）文件。 |
| Jpeg | `104` | 呈现文档的一页并将其保存为 JPEG 文件。 |
| Gif | `105` | 呈现文档的一页并将其保存为 GIF 文件。 |
| Eps | `106` | 渲染文档的一页并将其保存为 EPS 文件。 |
| WebP | `107` | 渲染文档的一页并将其保存为 WebP 文件。 |

## 例子

展示如何从 DOCX 转换为 HTML 格式。

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToHtml.html", SaveFormat.Html);
```

### 也可以看看

* method [Save](../document/save/)
* class [SaveOptions](../../aspose.words.saving/saveoptions/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
