---
title: "Aspose::Words::SaveFormat enum"
linktitle: "SaveFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::SaveFormat enum. Anger det format i vilket dokumentet sparas i C++."
type: docs
weight: 114000
url: /sv/cpp/aspose.words/saveformat/
---
## SaveFormat enum


Anger formatet i vilket dokumentet sparas.

```cpp
enum class SaveFormat
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Okänd | 0 | Standard, ogiltigt värde för filformat. |
| Doc | 10 | Sparar dokumentet i Microsoft Word 97 - 2007 [Document](../document/) formatet. |
| Dot | 11 | Sparar dokumentet i Microsoft Word 97 - 2007 mallformat. |
| Docx | 20 | Sparar dokumentet som ett Office Open XML WordprocessingML [Document](../document/) (utan makron). |
| Docm | 21 | Sparar dokumentet som ett Office Open XML WordprocessingML makroaktiverat [Document](../document/). |
| Dotx | 22 | Sparar dokumentet som en Office Open XML WordprocessingML-mall (utan makron). |
| Dotm | 23 | Sparar dokumentet som en Office Open XML WordprocessingML makroaktiverad mall. |
| FlatOpc | 24 | Sparar dokumentet som ett Office Open XML WordprocessingML lagrat i en platt XML‑fil istället för ett ZIP‑paket. |
| FlatOpcMacroEnabled | 25 | Sparar dokumentet som ett Office Open XML WordprocessingML makroaktiverat [Document](../document/) lagrat i en platt XML‑fil istället för ett ZIP‑paket. |
| FlatOpcTemplate | 26 | Sparar dokumentet som en Office Open XML WordprocessingML-mall (utan makron) lagrad i en platt XML‑fil istället för ett ZIP‑paket. |
| FlatOpcTemplateMacroEnabled | 27 | Sparar dokumentet som en Office Open XML WordprocessingML makroaktiverad mall lagrad i en platt XML‑fil istället för ett ZIP‑paket. |
| Rtf | 30 | Sparar dokumentet i RTF‑formatet. Alla tecken över 7‑bit ersätts med hexadecimala eller Unicode‑tecken. |
| WordML | 31 | Sparar dokumentet i Microsoft Word 2003 WordprocessingML‑formatet. |
| Pdf | 40 | Sparar dokumentet som PDF (Adobe Portable [Document](../document/)) format. |
| Xps | 41 | Sparar dokumentet i XPS (XML Paper Specification) format. |
| XamlFixed | 42 | Sparar dokumentet i Extensible Application [Markup](../../aspose.words.markup/) Language (XAML) format som ett fast dokument. |
| Svg | 44 | Sparar dokumentet i Svg (Scalable Vector Graphics) format. |
| HtmlFixed | 45 | Sparar dokumentet i HTML-format med absolut positionerade element. |
| OpenXps | 46 | Sparar dokumentet i OpenXPS (Ecma-388) format. |
| Ps | 47 | Sparar dokumentet i PS (PostScript) format. |
| Pcl | 48 | Sparar dokumentet i PCL (Printer Control Language) format. |
| Html | 50 | Sparar dokumentet i HTML-format. |
| Mhtml | 51 | Sparar dokumentet i MHTML (Web archive) format. |
| Epub | 52 | Sparar dokumentet i EPUB-format. |
| Azw3 | 53 | Sparar dokumentet i AZW3-format. |
| Mobi | 54 | Sparar dokumentet i MOBI-format. |
| Odt | 60 | Sparar dokumentet som ett ODF Text [Document](../document/). |
| Ott | 61 | Sparar dokumentet som en ODF Text [Document](../document/) mall. |
| Text | 70 | Sparar dokumentet i vanligt textformat. |
| XamlFlow | 71 | **Beta.** Sparar dokumentet i Extensible Application [Markup](../../aspose.words.markup/) Language (XAML) format som ett flödesdokument. |
| XamlFlowPack | 72 | **Beta.** Sparar dokumentet i Extensible Application [Markup](../../aspose.words.markup/) Language (XAML) paketformat som ett flödesdokument. |
| Markdown | 73 | Sparar dokumentet i Markdown-format. |
| Xlsx | 80 | Sparar dokumentet som ett Office Open XML SpreadsheetML [Document](../document/) (utan makron). |
| Docling | 81 | Sparar dokumentet i Docling JSON-format. |
| Tiff | 100 | Renderar en sida eller flera sidor i dokumentet och sparar dem i en enkel- eller flersidig TIFF-fil. |
| Png | 101 | Renderar en sida i dokumentet och sparar den som en PNG-fil. |
| Bmp | 102 | Renderar en sida i dokumentet och sparar den som en BMP-fil. |
| Emf | 103 | Renderar en sida i dokumentet och sparar den som en vektor‑EMF‑fil (Enhanced Meta File). |
| Jpeg | 104 | Renderar en sida i dokumentet och sparar den som en JPEG-fil. |
| Gif | 105 | Renderar en sida i dokumentet och sparar den som en GIF-fil. |
| Eps | 106 | Renderar en sida i dokumentet och sparar den som en EPS-fil. |


## Exempel



Visar hur man konverterar från DOCX till HTML-format.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

doc->Save(get_ArtifactsDir() + u"Document.ConvertToHtml.html", Aspose::Words::SaveFormat::Html);
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
