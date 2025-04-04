---
title: SaveFormat enumeration
linktitle: SaveFormat enumeration
articleTitle: SaveFormat enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.SaveFormat enumeration. Indicates the format in which the document is saved."
type: docs
weight: 1150
url: /nodejs-net/aspose.words/saveformat/
---

## SaveFormat enumeration

Indicates the format in which the document is saved.


### Members

| Name | Description |
| --- | --- |
| Unknown | Default, invalid value for file format. |
| Doc | Saves the document in the Microsoft Word 97 - 2007 Document format. |
| Dot | Saves the document in the Microsoft Word 97 - 2007 Template format. |
| Docx | Saves the document as an Office Open XML WordprocessingML Document (macro-free). |
| Docm | Saves the document as an Office Open XML WordprocessingML Macro-Enabled Document. |
| Dotx | Saves the document as an Office Open XML WordprocessingML Template (macro-free). |
| Dotm | Saves the document as an Office Open XML WordprocessingML Macro-Enabled Template. |
| FlatOpc | Saves the document as an Office Open XML WordprocessingML stored in a flat XML file instead of a ZIP package. |
| FlatOpcMacroEnabled | Saves the document as an Office Open XML WordprocessingML Macro-Enabled Document stored in a flat XML file instead of a ZIP package. |
| FlatOpcTemplate | Saves the document as an Office Open XML WordprocessingML Template (macro-free) stored in a flat XML file instead of a ZIP package. |
| FlatOpcTemplateMacroEnabled | Saves the document as an Office Open XML WordprocessingML Macro-Enabled Template stored in a flat XML file instead of a ZIP package. |
| Rtf | Saves the document in the RTF format.  All characters above 7-bits are escaped as hexadecimal or Unicode characters. |
| WordML | Saves the document in the Microsoft Word 2003 WordprocessingML format. |
| Pdf | Saves the document as PDF (Adobe Portable Document) format. |
| Xps | Saves the document in the XPS (XML Paper Specification) format. |
| XamlFixed | Saves the document in the Extensible Application Markup Language (XAML) format as a fixed document. |
| Svg | Saves the document in the Svg (Scalable Vector Graphics) format. |
| HtmlFixed | Saves the document in the HTML format using absolutely positioned elements |
| OpenXps | Saves the document in the OpenXPS (Ecma-388) format. |
| Ps | Saves the document in the PS (PostScript) format. |
| Pcl | Saves the document in the PCL (Printer Control Language) format. |
| Html | Saves the document in the HTML format. |
| Mhtml | Saves the document in the MHTML (Web archive) format. |
| Epub | Saves the document in the EPUB format. |
| Azw3 | Saves the document in the AZW3 format. |
| Mobi | Saves the document in the MOBI format. |
| Odt | Saves the document as an ODF Text Document. |
| Ott | Saves the document as an ODF Text Document Template. |
| Text | Saves the document in the plain text format. |
| XamlFlow | **Beta.** Saves the document in the Extensible Application Markup Language (XAML) format as a flow document. |
| XamlFlowPack | **Beta.** Saves the document in the Extensible Application Markup Language (XAML) package format as a flow document. |
| Markdown | Saves the document in the Markdown format. |
| Xlsx | Saves the document as an Office Open XML SpreadsheetML Document (macro-free). |
| Tiff | Renders a page or pages of the document and saves them into a single or multipage TIFF file. |
| Png | Renders a page of the document and saves it as a PNG file. |
| Bmp | Renders a page of the document and saves it as a BMP file. |
| Emf | Renders a page of the document and saves it as a vector EMF (Enhanced Meta File) file. |
| Jpeg | Renders a page of the document and saves it as a JPEG file. |
| Gif | Renders a page of the document and saves it as a GIF file. |
| Eps | Renders a page of the document and saves it as an EPS file. |
| WebP | Renders a page of the document and saves it as a WebP file. |

### Examples

Shows how to convert from DOCX to HTML format.

```js
const doc = new aw.Document(base.myDir + "Document.docx");

doc.save(base.artifactsDir + "Document.ConvertToHtml.html", aw.SaveFormat.Html);
```

### See Also

* module [Aspose.Words](../)
* class [SaveOptions](../../aspose.words.saving/saveoptions/)

