---
title: DocumentBuilder.EndBookmark
linktitle: EndBookmark
articleTitle: EndBookmark
second_title: Aspose.Words för .NET
description: Markera enkelt slutet på ett bokmärke i ditt dokument med DocumentBuilders EndBookmark-metod, vilket förbättrar din dokumentorganisation och navigering.
type: docs
weight: 210
url: /sv/net/aspose.words/documentbuilder/endbookmark/
---
## DocumentBuilder.EndBookmark method

Markerar den aktuella positionen i dokumentet som ett bokmärkesslut.

```csharp
public BookmarkEnd EndBookmark(string bookmarkName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| bookmarkName | String | Namn på bokmärket. |

### Returvärde

Bokmärkets slutnod som just skapades.

## Anmärkningar

Bokmärken i ett dokument kan överlappa varandra och omfatta vilket område som helst. För att skapa ett giltigt bokmärke måste du anropa båda.[`StartBookmark`](../startbookmark/) och`EndBookmark` med samma*bookmarkName* -parametern.

Felaktigt utformade bokmärken eller bokmärken med dubbletter av namn kommer att ignoreras när dokumentet sparas.

## Exempel

Visar hur man skapar ett bokmärke.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ett giltigt bokmärke måste ha dokumentets brödtext omgiven av
// Noderna BookmarkStart och BookmarkEnd skapade med ett matchande bokmärkesnamn.
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

// Infoga ett HYPERLINK-fält som länkar till bokmärket. Vi kan skicka fältväxlar
// till metoden "InsertHyperlink" som en del av argumentet som innehåller det refererade bokmärkets namn.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
FieldHyperlink hyperlink = (FieldHyperlink)builder.InsertHyperlink("Link to Bookmark1", "Bookmark1", true);
hyperlink.ScreenTip = "Hyperlink Tip";

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

### Se även

* class [BookmarkEnd](../../bookmarkend/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
