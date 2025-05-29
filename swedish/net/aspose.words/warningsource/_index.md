---
title: WarningSource Enum
linktitle: WarningSource
articleTitle: WarningSource
second_title: Aspose.Words för .NET
description: Upptäck enumereringen Aspose.Words.WarningSource, som identifierar varningskällor under dokumentinläsning och sparning för förbättrad dokumenthantering.
type: docs
weight: 7500
url: /sv/net/aspose.words/warningsource/
---
## WarningSource enumeration

Anger modulen som utlöser en varning när dokumentet laddas eller sparas.

```csharp
public enum WarningSource
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Unknown | `0` | Varningskällan är inte specificerad. |
| Layout | `1` | Modul som bygger en dokumentlayout. |
| DrawingML | `2` | Modul som renderar DrawingML-former. |
| OfficeMath | `3` | Modul som renderar OfficeMath. |
| Shapes | `4` | Modul som återger vanliga former. |
| Metafile | `5` | Modul som renderar metafiler. |
| Xps | `6` | Modul som renderar XPS. |
| Pdf | `7` | Modul som renderar PDF. |
| Image | `8` | Modul som renderar bilder. |
| Docx | `9` | Modul som läser/skriver DOCX-filer. |
| Doc | `10` | Modul som läser/skriver binära DOC-filer. |
| Text | `11` | Modul som läser/skriver klartextfiler. |
| Rtf | `12` | Modul som läser/skriver RTF-filer. |
| WordML | `13` | Modul som läser/skriver WML-filer. |
| Nrx | `14` | Gemensamma moduler som delas mellan DOCX/WML-läsar-/skrivarmoduler. |
| Odt | `15` | Modul som läser/skriver ODT-filer. |
| Html | `16` | Modul som läser/skriver HTML/MHTML-filer. |
| Validator | `17` | Modul som verifierar modellens konsistens och validitet. |
| Xaml | `18` | Modul som läser/skriver Xaml-filer. |
| Svm | `19` | Modul som läser Svm-filer. |
| MathML | `20` | Modul som läser W3C MathML-filer. |
| Font | `21` | Modul som läser teckensnittsfiler. |
| Svg | `22` | Modul som läser SVG-filer. |
| Markdown | `23` | Modul som läser/skriver Markdown-filer. |
| Chm | `24` | Modul som läser CHM-filer. |
| Epub | `25` | Modul som läser/skriver EPUB-filer. |
| Xml | `26` | Modul som läser XML-filer. |
| Xlsx | `27` | Modul som skriver XLSX-filer. |

## Exempel

Visar hur man arbetar med varningskällan.

```csharp
Document doc = new Document(MyDir + "Emphases markdown warning.docx");

WarningInfoCollection warnings = new WarningInfoCollection();
doc.WarningCallback = warnings;
doc.Save(ArtifactsDir + "DocumentBuilder.EmphasesWarningSourceMarkdown.md");

foreach (WarningInfo warningInfo in warnings)
{
    if (warningInfo.Source == WarningSource.Markdown)
        Assert.AreEqual("The (*, 0:11) cannot be properly written into Markdown.", warningInfo.Description);
}
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
