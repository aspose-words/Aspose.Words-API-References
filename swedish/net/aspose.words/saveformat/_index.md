---
title: SaveFormat Enum
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.SaveFormat enum för att enkelt välja dokumentformat, vilket förbättrar din filhantering och kompatibilitet för sömlösa arbetsflöden.
type: docs
weight: 5580
url: /sv/net/aspose.words/saveformat/
---
## SaveFormat enumeration

Anger formatet som dokumentet sparas i.

```csharp
public enum SaveFormat
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Unknown | `0` | Standardvärde, ogiltigt värde för filformat. |
| Doc | `10` | Sparar dokumentet i dokumentformatet Microsoft Word 97–2007. |
| Dot | `11` | Sparar dokumentet i mallformatet Microsoft Word 97-2007. |
| Docx | `20` | Sparar dokumentet som ett Office Open XML WordprocessingML-dokument (makrofritt). |
| Docm | `21` | Sparar dokumentet som ett Office Open XML WordprocessingML-makroaktiverat dokument. |
| Dotx | `22` | Sparar dokumentet som en Office Open XML WordprocessingML-mall (makrofri). |
| Dotm | `23` | Sparar dokumentet som en Office Open XML WordprocessingML-makroaktiverad mall. |
| FlatOpc | `24` | Sparar dokumentet som ett Office Open XML WordprocessingML-program som lagras i en platt XML-fil istället för ett ZIP-paket. |
| FlatOpcMacroEnabled | `25` | Sparar dokumentet som ett Office Open XML WordprocessingML-makroaktiverat dokument som lagras i en platt XML-fil istället för ett ZIP-paket. |
| FlatOpcTemplate | `26` | Sparar dokumentet som en Office Open XML WordprocessingML-mall (makrofri) lagrad i en platt XML-fil istället för ett ZIP-paket. |
| FlatOpcTemplateMacroEnabled | `27` | Sparar dokumentet som en Office Open XML WordprocessingML-makroaktiverad mall lagrad i en platt XML-fil istället för ett ZIP-paket. |
| Rtf | `30` | Sparar dokumentet i RTF-format. Alla tecken över 7 bitar escapes som hexadecimala tecken eller Unicode-tecken. |
| WordML | `31` | Sparar dokumentet i Microsoft Word 2003 WordprocessingML-formatet. |
| Pdf | `40` | Sparar dokumentet i PDF-format (Adobe Portable Document). |
| Xps | `41` | Sparar dokumentet i XPS-format (XML Paper Specification). |
| XamlFixed | `42` | Sparar dokumentet i XAML-format (Extensible Application Markup Language) som ett fast dokument. |
| Svg | `44` | Sparar dokumentet i Svg-format (skalbar vektorgrafik). |
| HtmlFixed | `45` | Sparar dokumentet i HTML-format med absolut positionerade element. |
| OpenXps | `46` | Sparar dokumentet i OpenXPS-formatet (Ecma-388). |
| Ps | `47` | Sparar dokumentet i PS-format (PostScript). |
| Pcl | `48` | Sparar dokumentet i PCL-format (Printer Control Language). |
| Html | `50` | Sparar dokumentet i HTML-format. |
| Mhtml | `51` | Sparar dokumentet i MHTML-format (webbarkiv). |
| Epub | `52` | Sparar dokumentet i EPUB-format. |
| Azw3 | `53` | Sparar dokumentet i AZW3-formatet. |
| Mobi | `54` | Sparar dokumentet i MOBI-format. |
| Odt | `60` | Sparar dokumentet som ett ODF-textdokument. |
| Ott | `61` | Sparar dokumentet som en ODF-textdokumentmall. |
| Text | `70` | Sparar dokumentet i oformaterad text. |
| XamlFlow | `71` | **Beta.** Sparar dokumentet i XAML-format (Extensible Application Markup Language) som ett flödesdokument. |
| XamlFlowPack | `72` | **Beta.** Sparar dokumentet i XAML-paketformatet (Extensible Application Markup Language) som ett flödesdokument. |
| Markdown | `73` | Sparar dokumentet i Markdown-format. |
| Xlsx | `80` | Sparar dokumentet som ett Office Open XML SpreadsheetML-dokument (makrofritt). |
| Tiff | `100` | Återger en eller flera sidor av dokumentet och sparar dem i en TIFF-fil med en eller flera sidor. |
| Png | `101` | Renderar en sida av dokumentet och sparar den som en PNG-fil. |
| Bmp | `102` | Renderar en sida av dokumentet och sparar den som en BMP-fil. |
| Emf | `103` | Renderar en sida av dokumentet och sparar den som en vektor EMF-fil (Enhanced Meta File). |
| Jpeg | `104` | Återger en sida av dokumentet och sparar den som en JPEG-fil. |
| Gif | `105` | Renderar en sida av dokumentet och sparar den som en GIF-fil. |
| Eps | `106` | Renderar en sida av dokumentet och sparar den som en EPS-fil. |
| WebP | `107` | Renderar en sida av dokumentet och sparar den som en WebP-fil. |

## Exempel

Visar hur man konverterar från DOCX till HTML-format.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToHtml.html", SaveFormat.Html);
```

### Se även

* method [Save](../document/save/)
* class [SaveOptions](../../aspose.words.saving/saveoptions/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
