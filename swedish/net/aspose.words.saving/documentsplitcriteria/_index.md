---
title: DocumentSplitCriteria Enum
linktitle: DocumentSplitCriteria
articleTitle: DocumentSplitCriteria
second_title: Aspose.Words för .NET
description: Upptäck hur Aspose.Words.Saving.DocumentSplitCriteria förbättrar dokumentdelning för optimala Html-, Epub- och Azw3-format. Effektivisera din sparprocess!
type: docs
weight: 5710
url: /sv/net/aspose.words.saving/documentsplitcriteria/
---
## DocumentSplitCriteria enumeration

Anger hur dokumentet delas upp i delar när det sparas tillHtml , Epub ellerAzw3 format.

```csharp
[Flags]
public enum DocumentSplitCriteria
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Dokumentet är inte uppdelat. |
| PageBreak | `1` | Dokumentet delas upp i delar vid explicita sidbrytningar. En sidbrytning kan anges med en[`PageBreak`](../../aspose.words/controlchar/pagebreak/) tecken, en avsnittsbrytning som anger början på ett nytt avsnitt på en ny sida, eller ett stycke som har sitt[`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) egenskapen inställd på`sann` . |
| ColumnBreak | `2` | Dokumentet delas upp i delar vid kolumnbrytningar. En kolumnbrytning kan anges med en[`ColumnBreak`](../../aspose.words/controlchar/columnbreak/) tecken eller en avsnittsbrytning som anger början på ett nytt avsnitt i en ny kolumn. |
| SectionBreak | `4` | Dokumentet delas upp i delar med en sektionsbrytning av valfri typ. |
| HeadingParagraph | `8` | Dokumentet delas upp i delar i ett stycke formaterat med en rubrikstil**Rubrik 1** ,**Rubrik 2** etc. Använd tillsammans med[`DocumentSplitHeadingLevel`](../htmlsaveoptions/documentsplitheadinglevel/) för att ange rubriknivåerna (från 1 till den angivna nivån) där de ska delas. |

## Anmärkningar

`DocumentSplitCriteria`är en uppsättning flaggor som kan kombineras. Till exempel kan du dela document vid sidbrytningar och rubrikstycken i samma exportoperation.

Olika kriterier kan delvis överlappa varandra. Till exempel,**Rubrik 1** stil ges ofta [`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) egendom så den faller under två kriterier:PageBreak och HeadingParagraphVissa avsnittsbrytningar kan orsaka sidbrytningar och så vidare. I typiska fall är det mest praktiska alternativet att bara ange en flagga.

## Exempel

Visar hur man använder en specifik kodning när man sparar ett dokument till .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Använd ett SaveOptions-objekt för att ange kodningen för ett dokument som vi ska spara.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Som standard kommer ett .epub-dokument att ha allt innehåll i en HTML-del.
// Ett delningskriterium låter oss segmentera dokumentet i flera HTML-delar.
// Vi kommer att ställa in kriterierna för att dela upp dokumentet i rubrikstycken.
// Detta är användbart för läsare som inte kan läsa HTML-filer som är större än en viss storlek.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Ange att vi vill exportera dokumentegenskaper.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
