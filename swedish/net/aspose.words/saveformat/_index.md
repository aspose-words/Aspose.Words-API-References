---
title: SaveFormat Enum
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words för .NET
description: Aspose.Words.SaveFormat uppräkning. Indikerar formatet som dokumentet har sparats i i C#.
type: docs
weight: 4840
url: /sv/net/aspose.words/saveformat/
---
## SaveFormat enumeration

Indikerar formatet som dokumentet har sparats i.

```csharp
public enum SaveFormat
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Unknown | `0` | Standard, ogiltigt värde för filformat. |
| Doc | `10` | Sparar dokumentet i Microsoft Word 97 - 2007 dokumentformat. |
| Dot | `11` | Sparar dokumentet i Microsoft Word 97 - 2007 mallformat. |
| Docx | `20` | Sparar dokumentet som ett Office Open XML WordprocessingML-dokument (makrofritt). |
| Docm | `21` | Sparar dokumentet som ett Office Open XML WordprocessingML Macro-Enabled Document. |
| Dotx | `22` | Sparar dokumentet som en Office Open XML WordprocessingML-mall (makrofri). |
| Dotm | `23` | Sparar dokumentet som en Office Open XML WordprocessingML Macro-Enabled Mall. |
| FlatOpc | `24` | Sparar dokumentet som ett Office Open XML WordprocessingML lagrat i en platt XML-fil istället för ett ZIP-paket. |
| FlatOpcMacroEnabled | `25` | Sparar dokumentet som ett Office Open XML WordprocessingML Macro-Enabled Document lagrat i en platt XML-fil istället för ett ZIP-paket. |
| FlatOpcTemplate | `26` | Sparar dokumentet som en Office Open XML WordprocessingML-mall (makrofri) lagrad i en platt XML-fil istället för ett ZIP-paket. |
| FlatOpcTemplateMacroEnabled | `27` | Sparar dokumentet som en Office Open XML WordprocessingML Macro-Enabled Mall lagrad i en platt XML-fil istället för ett ZIP-paket. |
| Rtf | `30` | Sparar dokumentet i RTF-format. Alla tecken över 7-bitar är escaped som hexadecimala eller Unicode-tecken. |
| WordML | `31` | Sparar dokumentet i Microsoft Word 2003 WordprocessingML-format. |
| Pdf | `40` | Sparar dokumentet som PDF-format (Adobe Portable Document). |
| Xps | `41` | Sparar dokumentet i formatet XPS (XML Paper Specification). |
| XamlFixed | `42` | Sparar dokumentet i XAML-formatet (Extensible Application Markup Language) som ett fast dokument. |
| Svg | `44` | Sparar dokumentet i formatet Svg (Scalable Vector Graphics). |
| HtmlFixed | `45` | Sparar dokumentet i HTML-format med absolut placerade element |
| OpenXps | `46` | Sparar dokumentet i formatet OpenXPS (Ecma-388). |
| Ps | `47` | Sparar dokumentet i PS-format (PostScript). |
| Pcl | `48` | Sparar dokumentet i PCL-format (Printer Control Language). |
| Html | `50` | Sparar dokumentet i HTML-format. |
| Mhtml | `51` | Sparar dokumentet i MHTML-format (webbarkiv). |
| Epub | `52` | Sparar dokumentet i EPUB-format. |
| Azw3 | `53` | Sparar dokumentet i AZW3-format. |
| Mobi | `54` | Sparar dokumentet i MOBI-format. |
| Odt | `60` | Sparar dokumentet som ett ODF-textdokument. |
| Ott | `61` | Sparar dokumentet som en ODF-textdokumentmall. |
| Text | `70` | Sparar dokumentet i vanlig textformat. |
| XamlFlow | `71` | **Beta.** Sparar dokumentet i XAML-formatet (Extensible Application Markup Language) som ett flödesdokument. |
| XamlFlowPack | `72` | **Beta.** Sparar dokumentet i paketformatet Extensible Application Markup Language (XAML) som ett flödesdokument. |
| Markdown | `73` | Sparar dokumentet i Markdown-format. |
| Xlsx | `80` | Sparar dokumentet som ett Office Open XML SpreadsheetML-dokument (makrofritt). |
| Tiff | `100` | Återger en sida eller sidor i dokumentet och sparar dem i en enkel eller flersidig TIFF-fil. |
| Png | `101` | Återger en sida i dokumentet och sparar den som en PNG-fil. |
| Bmp | `102` | Återger en sida i dokumentet och sparar den som en BMP-fil. |
| Emf | `103` | Återger en sida i dokumentet och sparar den som en vektor-EMF-fil (Enhanced Meta File). |
| Jpeg | `104` | Återger en sida i dokumentet och sparar den som en JPEG-fil. |
| Gif | `105` | Återger en sida i dokumentet och sparar den som en GIF-fil. |
| Eps | `106` | Återger en sida i dokumentet och sparar den som en EPS-fil. |

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
