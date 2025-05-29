---
title: DocumentBuilder.StartColumnBookmark
linktitle: StartColumnBookmark
articleTitle: StartColumnBookmark
second_title: Aspose.Words för .NET
description: Använd DocumentBuilders StartColumnBookmark-metod för att enkelt markera tabellcellspositioner som kolumnbokmärken, vilket förbättrar dokumentnavigering och organisation.
type: docs
weight: 660
url: /sv/net/aspose.words/documentbuilder/startcolumnbookmark/
---
## DocumentBuilder.StartColumnBookmark method

Markerar den aktuella positionen i dokumentet som en kolumnbokmärkesstart. Positionen måste finnas i en tabellcell.

```csharp
public BookmarkStart StartColumnBookmark(string bookmarkName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| bookmarkName | String | Namn på bokmärket. |

### Returvärde

Bokmärkets startnod som just skapades.

## Anmärkningar

Ett kolumnbokmärke täcker en eller flera kolumner i ett radintervall. För att skapa ett giltigt bokmärke måste du anropa båda`StartColumnBookmark` och[`EndColumnBookmark`](../endcolumnbookmark/) med samma *bookmarkName* parameter.

Felaktigt utformade bokmärken eller bokmärken med dubbletter av namn kommer att ignoreras när dokumentet sparas.

Den faktiska positionen för det insatta[`BookmarkStart`](../../bookmarkstart/) Noden kan skilja sig från den aktuella positionen i document -byggaren.

## Exempel

Visar hur man skapar ett bokmärke för en kolumn.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

builder.InsertCell();
// Cellerna 1, 2, 4, 5 kommer att bokmärkas.
builder.StartColumnBookmark("MyBookmark_1");
// Felaktigt utformade bokmärken eller bokmärken med dubbla namn ignoreras när dokumentet sparas.
builder.StartColumnBookmark("MyBookmark_1");
builder.StartColumnBookmark("BadStartBookmark");
builder.Write("Cell 1");

builder.InsertCell();
builder.Write("Cell 2");

builder.InsertCell();
builder.Write("Cell 3");

builder.EndRow();

builder.InsertCell();
builder.Write("Cell 4");

builder.InsertCell();
builder.Write("Cell 5");
builder.EndColumnBookmark("MyBookmark_1");
builder.EndColumnBookmark("MyBookmark_1");

builder.InsertCell();
builder.Write("Cell 6");

builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "Bookmarks.CreateColumnBookmark.docx");
```

### Se även

* class [BookmarkStart](../../bookmarkstart/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
