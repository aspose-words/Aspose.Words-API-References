---
title: DocumentSplitCriteria Enum
linktitle: DocumentSplitCriteria
articleTitle: DocumentSplitCriteria
second_title: Aspose.Words för .NET
description: Aspose.Words.Saving.DocumentSplitCriteria uppräkning. Anger hur dokumentet delas upp i delar när det sparas tillHtml  Epub ellerAzw3 format i C#.
type: docs
weight: 4960
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
| None | `0` | Dokumentet är inte delat. |
| PageBreak | `1` | Dokumentet delas upp i delar vid explicita sidbrytningar. En sidbrytning kan anges av en[`PageBreak`](../../aspose.words/controlchar/pagebreak/) tecken, en avsnittsbrytning som anger början av ett nytt avsnitt på en ny sida, eller ett stycke som har sin[`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) egenskapen inställd på`Sann` . |
| ColumnBreak | `2` | Dokumentet delas upp i delar vid kolumnbrytningar. En kolumnbrytning kan anges av en[`ColumnBreak`](../../aspose.words/controlchar/columnbreak/) tecken or en sektionsbrytning som anger början av ett nytt avsnitt i en ny kolumn. |
| SectionBreak | `4` | Dokumentet delas upp i delar vid en sektionsbrytning av vilken typ som helst. |
| HeadingParagraph | `8` | Dokumentet delas upp i delar i ett stycke formaterat med en rubrikstil**Rubrik 1** ,**Rubrik 2** etc. Använd tillsammans med[`DocumentSplitHeadingLevel`](../htmlsaveoptions/documentsplitheadinglevel/) för att ange rubriknivåerna (från 1 till den angivna nivån) som ska delas upp. |

## Anmärkningar

`DocumentSplitCriteria`är en uppsättning flaggor som kan kombineras. Du kan till exempel dela upp document vid sidbrytningar och rubrikstycken i samma exportoperation.

Olika kriterier kan delvis överlappa varandra. Till exempel,**Rubrik 1** stil ges ofta [`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) egendom så den faller under två kriterier:PageBreak och HeadingParagraph. Vissa avsnittsbrytningar kan orsaka sidbrytningar och så vidare. I typiska fall är det mest praktiska alternativet att specificera endast en flagga.

## Exempel

Visar hur du använder en specifik kodning när du sparar ett dokument i .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Använd ett SaveOptions-objekt för att ange kodningen för ett dokument som vi ska spara.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Som standard kommer ett utdata .epub-dokument att ha allt innehåll i en HTML-del.
// Ett delat kriterium tillåter oss att segmentera dokumentet i flera HTML-delar.
// Vi kommer att ställa in kriterierna för att dela upp dokumentet i rubriker.
// Detta är användbart för läsare som inte kan läsa HTML-filer som är större än en viss storlek.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Ange att vi vill exportera dokumentegenskaper.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
