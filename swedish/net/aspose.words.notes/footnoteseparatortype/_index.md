---
title: FootnoteSeparatorType Enum
linktitle: FootnoteSeparatorType
articleTitle: FootnoteSeparatorType
second_title: Aspose.Words för .NET
description: Upptäck enumereringen Aspose.Words.FootnoteSeparatorType för att anpassa fotnots- och slutnotsavgränsare, vilket förbättrar dokumentformatering och läsbarhet.
type: docs
weight: 5010
url: /sv/net/aspose.words.notes/footnoteseparatortype/
---
## FootnoteSeparatorType enumeration

Anger typen av fotnots-/slutnotsavgränsare.

```csharp
public enum FootnoteSeparatorType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| FootnoteSeparator | `0` | Avgränsare mellan huvudtext och fotnotstext. |
| FootnoteContinuationSeparator | `1` | Skrivs ovanför fotnotstext på en sida när texten måste fortsätta från en föregående sida. |
| FootnoteContinuationNotice | `2` | Tryckt under fotnotstext på en sida när fotnotstext måste fortsätta på en efterföljande sida. |
| EndnoteSeparator | `3` | Avgränsare mellan huvudtext och slutnotstext. |
| EndnoteContinuationSeparator | `4` | Skrivs ovanför slutnotstext på en sida när texten måste fortsätta från en föregående sida. |
| EndnoteContinuationNotice | `5` | Skrivs under slutnotstexten på en sida när slutnotstexten måste fortsätta på en efterföljande sida. |

## Exempel

Visar hur man tar bort slutnotsavgränsaren.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator endnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.EndnoteSeparator];
// Ta bort slutnotsavgränsare.
endnoteSeparator.FirstParagraph.FirstChild.Remove();
```

Visar hur man hanterar formatet för fotnotsavgränsare.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
// Justera fotnotsavgränsaren.
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### Se även

* namnutrymme [Aspose.Words.Notes](../../aspose.words.notes/)
* hopsättning [Aspose.Words](../../)
