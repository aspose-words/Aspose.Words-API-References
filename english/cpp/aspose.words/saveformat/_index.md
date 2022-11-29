---
title: SaveFormat
second_title: Aspose.Words for C++ API Reference
description: Indicates the format in which the document is saved.
type: docs
weight: 1470
url: /cpp/aspose.words/saveformat/
---
## SaveFormat enum


Indicates the format in which the document is saved.

```cpp
enum class SaveFormat
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Unknown | 0 | Default, invalid value for file format. |
| Doc | 10 | Saves the document in the Microsoft Word 97 - 2007 [Document](../document/) format. |
| Dot | 11 | Saves the document in the Microsoft Word 97 - 2007 Template format. |
| Docx | 20 | Saves the document as an Office Open XML WordprocessingML [Document](../document/) (macro-free). |
| Docm | 21 | Saves the document as an Office Open XML WordprocessingML Macro-Enabled [Document](../document/). |
| Dotx | 22 | Saves the document as an Office Open XML WordprocessingML Template (macro-free). |
| Dotm | 23 | Saves the document as an Office Open XML WordprocessingML Macro-Enabled Template. |
| FlatOpc | 24 | Saves the document as an Office Open XML WordprocessingML stored in a flat XML file instead of a ZIP package. |
| FlatOpcMacroEnabled | 25 | Saves the document as an Office Open XML WordprocessingML Macro-Enabled [Document](../document/) stored in a flat XML file instead of a ZIP package. |
| FlatOpcTemplate | 26 | Saves the document as an Office Open XML WordprocessingML Template (macro-free) stored in a flat XML file instead of a ZIP package. |
| FlatOpcTemplateMacroEnabled | 27 | Saves the document as an Office Open XML WordprocessingML Macro-Enabled Template stored in a flat XML file instead of a ZIP package. |
| Rtf | 30 | Saves the document in the RTF format. All characters above 7-bits are escaped as hexadecimal or Unicode characters. |
| WordML | 31 | Saves the document in the Microsoft Word 2003 WordprocessingML format. |
| Pdf | 40 | Saves the document as PDF (Adobe Portable [Document](../document/)) format. |
| Xps | 41 | Saves the document in the XPS (XML Paper Specification) format. |
| XamlFixed | 42 | Saves the document in the Extensible Application [Markup](../../aspose.words.markup/) Language (XAML) format as a fixed document. |
| Svg | 44 | Saves the document in the Svg (Scalable Vector Graphics) format. |
| HtmlFixed | 45 | Saves the document in the HTML format using absolutely positioned elements. |
| OpenXps | 46 | Saves the document in the OpenXPS (Ecma-388) format. |
| Ps | 47 | Saves the document in the PS (PostScript) format. |
| Pcl | 48 | Saves the document in the PCL (Printer Control Language) format. |
| Html | 50 | Saves the document in the HTML format. |
| Mhtml | 51 | Saves the document in the MHTML (Web archive) format. |
| Epub | 52 | Saves the document in the EPUB format. |
| Azw3 | 53 | Saves the document in the AZW3 format. |
| Odt | 60 | Saves the document as an ODF Text [Document](../document/). |
| Ott | 61 | Saves the document as an ODF Text [Document](../document/) Template. |
| Text | 70 | Saves the document in the plain text format. |
| XamlFlow | 71 | **Beta.** Saves the document in the Extensible Application [Markup](../../aspose.words.markup/) Language (XAML) format as a flow document. |
| XamlFlowPack | 72 | **Beta.** Saves the document in the Extensible Application [Markup](../../aspose.words.markup/) Language (XAML) package format as a flow document. |
| Markdown | 73 | Saves the document in the Markdown format. |
| Tiff | 100 | Renders a page or pages of the document and saves them into a single or multipage TIFF file. |
| Png | 101 | Renders a page of the document and saves it as a PNG file. |
| Bmp | 102 | Renders a page of the document and saves it as a BMP file. |
| Emf | 103 | Renders a page of the document and saves it as a vector EMF (Enhanced Meta File) file. |
| Jpeg | 104 | Renders a page of the document and saves it as a JPEG file. |
| Gif | 105 | Renders a page of the document and saves it as a GIF file. |


## Examples



Shows how to convert from DOCX to HTML format. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Document.docx");

doc->Save(ArtifactsDir + u"Document.ConvertToHtml.html", SaveFormat::Html);
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words](../../)
