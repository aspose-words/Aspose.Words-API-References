---
title: "Aspose::Words::SaveFormat 枚举"
linktitle: "SaveFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::SaveFormat 枚举。指示文档在 C++ 中保存的格式。"
type: docs
weight: 114000
url: /zh/cpp/aspose.words/saveformat/
---
## SaveFormat enum


指示文档保存的格式。

```cpp
enum class SaveFormat
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 未知 | 0 | 默认，文件格式的无效值。 |
| Doc | 10 | 将文档保存为 Microsoft Word 97 - 2007 [文档](../document/) 格式。 |
| Dot | 11 | 将文档保存为 Microsoft Word 97 - 2007 模板格式。 |
| Docx | 20 | 将文档保存为 Office Open XML WordprocessingML [文档](../document/)（无宏）。 |
| Docm | 21 | 将文档保存为 Office Open XML WordprocessingML 启用宏的 [文档](../document/)。 |
| Dotx | 22 | 将文档保存为 Office Open XML WordprocessingML 模板（无宏）。 |
| Dotm | 23 | 将文档保存为 Office Open XML WordprocessingML 启用宏的模板。 |
| FlatOpc | 24 | 将文档保存为存储在平面 XML 文件而非 ZIP 包中的 Office Open XML WordprocessingML。 |
| FlatOpcMacroEnabled | 25 | 将文档保存为启用宏的 Office Open XML WordprocessingML [文档](../document/)，存储在平面 XML 文件而非 ZIP 包中。 |
| FlatOpcTemplate | 26 | 将文档保存为（无宏）的 Office Open XML WordprocessingML 模板，存储在平面 XML 文件而非 ZIP 包中。 |
| FlatOpcTemplateMacroEnabled | 27 | 将文档保存为启用宏的 Office Open XML WordprocessingML 模板，存储在平面 XML 文件而非 ZIP 包中。 |
| Rtf | 30 | 以 RTF 格式保存文档。所有超过 7 位的字符均以十六进制或 Unicode 字符转义。 |
| WordML | 31 | 以 Microsoft Word 2003 WordprocessingML 格式保存文档。 |
| Pdf | 40 | 将文档保存为 PDF（Adobe Portable [文档](../document/)）格式。 |
| Xps | 41 | 以 XPS（XML Paper Specification）格式保存文档。 |
| XamlFixed | 42 | 以可扩展应用程序 [标记](../../aspose.words.markup/) 语言（XAML）格式保存文档为固定文档。 |
| Svg | 44 | 以 Svg（Scalable Vector Graphics）格式保存文档。 |
| HtmlFixed | 45 | 以 HTML 格式保存文档，使用绝对定位的元素。 |
| OpenXps | 46 | 以 OpenXPS（Ecma-388）格式保存文档。 |
| Ps | 47 | 以 PS（PostScript）格式保存文档。 |
| Pcl | 48 | 以 PCL（Printer Control Language）格式保存文档。 |
| Html | 50 | 以 HTML 格式保存文档。 |
| Mhtml | 51 | 以 MHTML（Web 存档）格式保存文档。 |
| Epub | 52 | 以 EPUB 格式保存文档。 |
| Azw3 | 53 | 以 AZW3 格式保存文档。 |
| Mobi | 54 | 以 MOBI 格式保存文档。 |
| Odt | 60 | 将文档保存为 ODF 文本 [Document](../document/)。 |
| Ott | 61 | 将文档保存为 ODF 文本 [Document](../document/) 模板。 |
| 文本 | 70 | 以纯文本格式保存文档。 |
| XamlFlow | 71 | **Beta.** 将文档保存为可扩展应用程序 [Markup](../../aspose.words.markup/) 语言 (XAML) 格式的流文档。 |
| XamlFlowPack | 72 | **Beta.** 将文档保存为可扩展应用程序 [Markup](../../aspose.words.markup/) 语言 (XAML) 包格式的流文档。 |
| Markdown | 73 | 以 Markdown 格式保存文档。 |
| Xlsx | 80 | 将文档保存为 Office Open XML SpreadsheetML [Document](../document/)（无宏）。 |
| Docling | 81 | 以 Docling JSON 格式保存文档。 |
| Tiff | 100 | 渲染文档的一个或多个页面，并将其保存为单页或多页 TIFF 文件。 |
| Png | 101 | 渲染文档的页面，并将其保存为 PNG 文件。 |
| Bmp | 102 | 渲染文档的页面，并将其保存为 BMP 文件。 |
| Emf | 103 | 渲染文档的页面，并将其保存为矢量 EMF（增强型元文件）文件。 |
| Jpeg | 104 | 渲染文档的页面，并将其保存为 JPEG 文件。 |
| Gif | 105 | 渲染文档的页面，并将其保存为 GIF 文件。 |
| Eps | 106 | 渲染文档的一页并将其保存为 EPS 文件。 |


## 示例



展示如何将 DOCX 转换为 HTML 格式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

doc->Save(get_ArtifactsDir() + u"Document.ConvertToHtml.html", Aspose::Words::SaveFormat::Html);
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
