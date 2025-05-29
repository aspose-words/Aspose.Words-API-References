---
title: FootnoteSeparatorCollection Class
linktitle: FootnoteSeparatorCollection
articleTitle: FootnoteSeparatorCollection
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Notes.FootnoteSeparatorCollection för enkel åtkomst till fotnotsavgränsare i dina dokument. Förbättra din dokumentformatering idag!
type: docs
weight: 5000
url: /sv/net/aspose.words.notes/footnoteseparatorcollection/
---
## FootnoteSeparatorCollection class

Ger maskinskriven åtkomst till[`FootnoteSeparator`](../footnoteseparator/) noder i ett dokument.

```csharp
public class FootnoteSeparatorCollection : IEnumerable<FootnoteSeparator>
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FootnoteSeparatorCollection](footnoteseparatorcollection/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Item](../../aspose.words.notes/footnoteseparatorcollection/item/) { get; } | Hämtar en[`FootnoteSeparator`](../footnoteseparator/) av den angivna typen. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetEnumerator](../../aspose.words.notes/footnoteseparatorcollection/getenumerator/)() |  |

## Exempel

Visar hur man hanterar formatet för fotnotsavgränsare.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
// Justera fotnotsavgränsaren.
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### Se även

* class [FootnoteSeparator](../footnoteseparator/)
* namnutrymme [Aspose.Words.Notes](../../aspose.words.notes/)
* hopsättning [Aspose.Words](../../)
