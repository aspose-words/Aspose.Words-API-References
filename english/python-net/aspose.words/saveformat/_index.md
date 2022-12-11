---
title: SaveFormat enumeration
second_title: Aspose.Words for Python via .NET API Reference
description: "Indicates the format in which the document is saved."
type: docs
weight: 990
url: /python-net/aspose.words/saveformat/
---

## SaveFormat enumeration

Indicates the format in which the document is saved.


### Members

| Name | Description |
| --- | --- |
| UNKNOWN | Default, invalid value for file format. |
| DOC | Saves the document in the Microsoft Word 97 - 2007 Document format. |
| DOT | Saves the document in the Microsoft Word 97 - 2007 Template format. |
| DOCX | Saves the document as an Office Open XML WordprocessingML Document (macro-free). |
| DOCM | Saves the document as an Office Open XML WordprocessingML Macro-Enabled Document. |
| DOTX | Saves the document as an Office Open XML WordprocessingML Template (macro-free). |
| DOTM | Saves the document as an Office Open XML WordprocessingML Macro-Enabled Template. |
| FLAT_OPC | Saves the document as an Office Open XML WordprocessingML stored in a flat XML file instead of a ZIP package. |
| FLAT_OPC_MACRO_ENABLED | Saves the document as an Office Open XML WordprocessingML Macro-Enabled Document stored in a flat XML file instead of a ZIP package. |
| FLAT_OPC_TEMPLATE | Saves the document as an Office Open XML WordprocessingML Template (macro-free) stored in a flat XML file instead of a ZIP package. |
| FLAT_OPC_TEMPLATE_MACRO_ENABLED | Saves the document as an Office Open XML WordprocessingML Macro-Enabled Template stored in a flat XML file instead of a ZIP package. |
| RTF | Saves the document in the RTF format.  All characters above 7-bits are escaped as hexadecimal or Unicode characters. |
| WORD_ML | Saves the document in the Microsoft Word 2003 WordprocessingML format. |
| PDF | Saves the document as PDF (Adobe Portable Document) format. |
| XPS | Saves the document in the XPS (XML Paper Specification) format. |
| XAML_FIXED | Saves the document in the Extensible Application Markup Language (XAML) format as a fixed document. |
| SVG | Saves the document in the Svg (Scalable Vector Graphics) format. |
| HTML_FIXED | Saves the document in the HTML format using absolutely positioned elements |
| OPEN_XPS | Saves the document in the OpenXPS (Ecma-388) format. |
| PS | Saves the document in the PS (PostScript) format. |
| PCL | Saves the document in the PCL (Printer Control Language) format. |
| HTML | Saves the document in the HTML format. |
| MHTML | Saves the document in the MHTML (Web archive) format. |
| EPUB | Saves the document in the EPUB format. |
| AZW3 | Saves the document in the AZW3 format. |
| ODT | Saves the document as an ODF Text Document. |
| OTT | Saves the document as an ODF Text Document Template. |
| TEXT | Saves the document in the plain text format. |
| XAML_FLOW | **Beta.** Saves the document in the Extensible Application Markup Language (XAML) format as a flow document. |
| XAML_FLOW_PACK | **Beta.** Saves the document in the Extensible Application Markup Language (XAML) package format as a flow document. |
| MARKDOWN | Saves the document in the Markdown format. |
| TIFF | Renders a page or pages of the document and saves them into a single or multipage TIFF file. |
| PNG | Renders a page of the document and saves it as a PNG file. |
| BMP | Renders a page of the document and saves it as a BMP file. |
| EMF | Renders a page of the document and saves it as a vector EMF (Enhanced Meta File) file. |
| JPEG | Renders a page of the document and saves it as a JPEG file. |
| GIF | Renders a page of the document and saves it as a GIF file. |

### Examples

Shows how to convert from DOCX to HTML format.

```python
doc = aw.Document(MY_DIR + "Document.docx")

doc.save(ARTIFACTS_DIR + "Document.convert_to_html.html", aw.SaveFormat.HTML)
```

### See Also

* module [aspose.words](../)
* method [Document.save()](../document/save/#bytesio_saveformat)
* class [SaveOptions](../../aspose.words.saving/saveoptions/)

