---
title: FootnoteSeparatorCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words för .NET
description: Få åtkomst till egenskapen FootnoteSeparatorCollection Item för att enkelt hämta anpassade fotnotsavgränsare efter typ, vilket förbättrar dokumentformateringen.
type: docs
weight: 20
url: /sv/net/aspose.words.notes/footnoteseparatorcollection/item/
---
## FootnoteSeparatorCollection indexer

Hämtar en[`FootnoteSeparator`](../../footnoteseparator/) av den angivna typen.

```csharp
public FootnoteSeparator this[FootnoteSeparatorType separatorType] { get; }
```

## Anmärkningar

Returer`null` om fotnots-/slutnotsavgränsaren av den angivna typen inte hittas.

## Exempel

Visar hur man hanterar formatet för fotnotsavgränsare.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
// Justera fotnotsavgränsaren.
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### Se även

* class [FootnoteSeparator](../../footnoteseparator/)
* enum [FootnoteSeparatorType](../../footnoteseparatortype/)
* class [FootnoteSeparatorCollection](../)
* namnutrymme [Aspose.Words.Notes](../../../aspose.words.notes/)
* hopsättning [Aspose.Words](../../../)
