---
title: TextColumnCollection.SetCount
linktitle: SetCount
articleTitle: SetCount
second_title: Aspose.Words för .NET
description: Optimera din layout med metoden TextColumnCollection SetCount, och arrangera enkelt text i önskat antal kolumner för förbättrad läsbarhet.
type: docs
weight: 70
url: /sv/net/aspose.words/textcolumncollection/setcount/
---
## TextColumnCollection.SetCount method

Ordnar text i det angivna antalet textkolumner.

```csharp
public void SetCount(int newCount)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| newCount | Int32 | Antalet kolumner som texten ska ordnas i. |

## Anmärkningar

När[`EvenlySpaced`](../evenlyspaced/) är`falsk` och du ökar antalet kolumner, ny[`TextColumn`](../../textcolumn/) objekt skapas med noll bredd och avstånd. Du måste ange bredd och avstånd för de nya kolumnerna.

## Exempel

Visar hur man skapar flera jämnt fördelade kolumner i ett avsnitt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.Spacing = 100;
columns.SetCount(2);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

doc.Save(ArtifactsDir + "PageSetup.ColumnsSameWidth.docx");
```

### Se även

* class [TextColumnCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
