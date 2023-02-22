---
title: DocumentBuilder.StartBookmark
second_title: Aspose.Words för .NET API Referens
description: DocumentBuilder metod. Markerar den aktuella positionen i dokumentet som en bokmärkesstart.
type: docs
weight: 580
url: /sv/net/aspose.words/documentbuilder/startbookmark/
---
## DocumentBuilder.StartBookmark method

Markerar den aktuella positionen i dokumentet som en bokmärkesstart.

```csharp
public BookmarkStart StartBookmark(string bookmarkName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| bookmarkName | String | Bokmärkets namn. |

### Returvärde

Bokmärkets startnod som just skapades.

### Anmärkningar

Bokmärken i ett dokument kan överlappa och sträcka sig över alla områden. För att skapa ett giltigt bokmärke måste du anropa båda`StartBookmark` och[`EndBookmark`](../endbookmark/) med samma **bokmärkeNamn** parameter.

Dåligt utformade bokmärken eller bokmärken med dubbletter av namn kommer att ignoreras när dokumentet sparas.

### Exempel

Visar hur du skapar ett bokmärke.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ett giltigt bokmärke måste ha dokumentets brödtext omsluten av
// BookmarkStart- och BookmarkEnd-noder skapade med ett matchande bokmärkesnamn.
builder.StartBookmark("MyBookmark");
builder.Writeln("Hello world!");
builder.EndBookmark("MyBookmark");

Assert.AreEqual(1, doc.Range.Bookmarks.Count);
Assert.AreEqual("MyBookmark", doc.Range.Bookmarks[0].Name);
Assert.AreEqual("Hello world!", doc.Range.Bookmarks[0].Text.Trim());
```

Visar hur man infogar en hyperlänk som refererar till ett lokalt bokmärke.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("Bookmark1");
builder.Write("Bookmarked text. ");
builder.EndBookmark("Bookmark1");
builder.Writeln("Text outside of the bookmark.");

// Infoga ett HYPERLÄNK-fält som länkar till bokmärket. Vi kan passera fältväxlar
// till metoden "InsertHyperlink" som en del av argumentet som innehåller det refererade bokmärkets namn.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Link to Bookmark1", @"Bookmark1"" \o ""Hyperlink Tip", true);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

### Se även

* class [BookmarkStart](../../bookmarkstart/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../documentbuilder/)
* hopsättning [Aspose.Words](../../../)


