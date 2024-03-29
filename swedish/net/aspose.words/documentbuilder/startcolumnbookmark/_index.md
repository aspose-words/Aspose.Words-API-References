---
title: DocumentBuilder.StartColumnBookmark
linktitle: StartColumnBookmark
articleTitle: StartColumnBookmark
second_title: Aspose.Words för .NET
description: DocumentBuilder StartColumnBookmark metod. Markerar den aktuella positionen i dokumentet som en kolumnbokmärkesstart. Positionen måste vara i en tabellcell i C#.
type: docs
weight: 620
url: /sv/net/aspose.words/documentbuilder/startcolumnbookmark/
---
## DocumentBuilder.StartColumnBookmark method

Markerar den aktuella positionen i dokumentet som en kolumnbokmärkesstart. Positionen måste vara i en tabellcell.

```csharp
public BookmarkStart StartColumnBookmark(string bookmarkName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| bookmarkName | String | Bokmärkets namn. |

### Returvärde

Bokmärkets startnod som just skapades.

## Anmärkningar

Ett kolumnbokmärke täcker en eller flera kolumner i ett radintervall. För att skapa ett giltigt bokmärke måste du anropa båda`StartColumnBookmark` och[`EndColumnBookmark`](../endcolumnbookmark/) med samma *bookmarkName*parameter.

Dåligt utformade bokmärken eller bokmärken med dubbletter av namn kommer att ignoreras när dokumentet sparas.

Den faktiska positionen för den infogade[`BookmarkStart`](../../bookmarkstart/) noden kan skilja sig från den aktuella dokument -byggarens position.

## Exempel

Visar hur man skapar ett kolumnbokmärke.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

builder.InsertCell();
// Cellerna 1,2,4,5 kommer att bokmärkas.
builder.StartColumnBookmark("MyBookmark_1");
// Dåligt utformade bokmärken eller bokmärken med dubbletter av namn kommer att ignoreras när dokumentet sparas.
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
