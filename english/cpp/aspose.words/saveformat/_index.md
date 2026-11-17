---
title: Aspose::Words::SaveFormat enum
linktitle: SaveFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::SaveFormat enum. Indicates the format in which the document is saved in C++.'
type: docs
weight: 114000
url: /cpp/aspose.words/saveformat/
---
## SaveFormat enum


Indicates the format in which the document is saved.

```cpp
enum class SaveFormat : int
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Azw3 | 53 | Saves the document in the AZW3 format. |
| Bmp | 102 | Renders a page of the document and saves it as a BMP file. |
| Doc | 10 | Saves the document in the Microsoft Word 97 - 2007 Document format. |
| Docling | 81 | Saves the document in Docling JSON format. |
| Docm | 21 | Saves the document as an Office Open XML WordprocessingML Macro-Enabled Document. |
| Docx | 20 | Saves the document as an Office Open XML WordprocessingML Document (macro-free). |
| Dot | 11 | Saves the document in the Microsoft Word 97 - 2007 Template format. |
| Dotm | 23 | Saves the document as an Office Open XML WordprocessingML Macro-Enabled Template. |
| Dotx | 22 | Saves the document as an Office Open XML WordprocessingML Template (macro-free). |
| Emf | 103 | Renders a page of the document and saves it as a vector EMF (Enhanced Meta File) file. |
| Eps | 106 | Renders a page of the document and saves it as an EPS file. |
| Epub | 52 | Saves the document in the EPUB format. |
| FlatOpc | 24 | Saves the document as an Office Open XML WordprocessingML stored in a flat XML file instead of a ZIP package. |
| FlatOpcMacroEnabled | 25 | Saves the document as an Office Open XML WordprocessingML Macro-Enabled Document stored in a flat XML file instead of a ZIP package. |
| FlatOpcTemplate | 26 | Saves the document as an Office Open XML WordprocessingML Template (macro-free) stored in a flat XML file instead of a ZIP package. |
| FlatOpcTemplateMacroEnabled | 27 | Saves the document as an Office Open XML WordprocessingML Macro-Enabled Template stored in a flat XML file instead of a ZIP package. |
| Gif | 105 | Renders a page of the document and saves it as a GIF file. |
| Html | 50 | Saves the document in the HTML format. |
| HtmlFixed | 45 | Saves the document in the HTML format using absolutely positioned elements |
| Jpeg | 104 | Renders a page of the document and saves it as a JPEG file. |
| Markdown | 73 | Saves the document in the Markdown format. |
| Mhtml | 51 | Saves the document in the MHTML (Web archive) format. |
| Mobi | 54 | Saves the document in the MOBI format. |
| Odt | 60 | Saves the document as an ODF Text Document. |
| OpenXps | 46 | Saves the document in the OpenXPS (Ecma-388) format. |
| Ott | 61 | Saves the document as an ODF Text Document Template. |
| Pcl | 48 | Saves the document in the PCL (Printer Control Language) format. |
| Pdf | 40 | Saves the document as PDF (Adobe Portable Document) format. |
| Png | 101 | Renders a page of the document and saves it as a PNG file. |
| Ps | 47 | Saves the document in the PS (PostScript) format. |
| Rtf | 30 | Saves the document in the RTF format. All characters above 7-bits are escaped as hexadecimal or Unicode characters. |
| Svg | 44 | Saves the document in the Svg (Scalable Vector Graphics) format. |
| Text | 70 | Saves the document in the plain text format. |
| Tiff | 100 | Renders a page or pages of the document and saves them into a single or multipage TIFF file. |
| Unknown | 0 | Default, invalid value for file format. |
| WordML | 31 | Saves the document in the Microsoft Word 2003 WordprocessingML format. |
| XamlFixed | 42 | Saves the document in the Extensible Application Markup Language (XAML) format as a fixed document. |
| XamlFlow | 71 | Beta. Saves the document in the Extensible Application Markup Language (XAML) format as a flow document. |
| XamlFlowPack | 72 | Beta. Saves the document in the Extensible Application Markup Language (XAML) package format as a flow document. |
| Xlsx | 80 | Saves the document as an Office Open XML SpreadsheetML Document (macro-free). |
| Xps | 41 | Saves the document in the XPS (XML Paper Specification) format. |

## Examples


Shows how to convert from DOCX to HTML format.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Document.docx"));

doc->Save(get_ArtifactsDir() + u"Document.ConvertToHtml.html", SaveFormat::Html);
```
## See Also

* [Save()](../document/save/)
* [SaveOptions](../../aspose.words.saving/saveoptions/)

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
