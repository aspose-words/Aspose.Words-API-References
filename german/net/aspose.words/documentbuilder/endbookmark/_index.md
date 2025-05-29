---
title: DocumentBuilder.EndBookmark
linktitle: EndBookmark
articleTitle: EndBookmark
second_title: Aspose.Words für .NET
description: Markieren Sie mühelos das Ende eines Lesezeichens in Ihrem Dokument mit der EndBookmark-Methode von DocumentBuilder und verbessern Sie so die Organisation und Navigation Ihres Dokuments.
type: docs
weight: 210
url: /de/net/aspose.words/documentbuilder/endbookmark/
---
## DocumentBuilder.EndBookmark method

Markiert die aktuelle Position im Dokument als Lesezeichenende.

```csharp
public BookmarkEnd EndBookmark(string bookmarkName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| bookmarkName | String | Name des Lesezeichens. |

### Rückgabewert

Der gerade erstellte Lesezeichen-Endknoten.

## Bemerkungen

Lesezeichen in einem Dokument können sich überlappen und einen beliebigen Bereich umfassen. Um ein gültiges Lesezeichen zu erstellen, müssen Sie beide aufrufen[`StartBookmark`](../startbookmark/) Und`EndBookmark` mit dem gleichen*bookmarkName* -Parameter.

Falsch formatierte Lesezeichen oder Lesezeichen mit doppelten Namen werden beim Speichern des Dokuments ignoriert.

## Beispiele

Zeigt, wie ein Lesezeichen erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ein gültiges Lesezeichen muss einen Dokumenttext enthalten, der von
// BookmarkStart- und BookmarkEnd-Knoten mit einem passenden Lesezeichennamen erstellt.
builder.StartBookmark("MyBookmark");
builder.Writeln("Hello world!");
builder.EndBookmark("MyBookmark");

Assert.AreEqual(1, doc.Range.Bookmarks.Count);
Assert.AreEqual("MyBookmark", doc.Range.Bookmarks[0].Name);
Assert.AreEqual("Hello world!", doc.Range.Bookmarks[0].Text.Trim());
```

Zeigt, wie ein Hyperlink eingefügt wird, der auf ein lokales Lesezeichen verweist.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("Bookmark1");
builder.Write("Bookmarked text. ");
builder.EndBookmark("Bookmark1");
builder.Writeln("Text outside of the bookmark.");

// Fügt ein HYPERLINK-Feld ein, das auf das Lesezeichen verweist. Wir können Feldschalter übergeben
// zur Methode „InsertHyperlink“ als Teil des Arguments, das den Namen des referenzierten Lesezeichens enthält.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
FieldHyperlink hyperlink = (FieldHyperlink)builder.InsertHyperlink("Link to Bookmark1", "Bookmark1", true);
hyperlink.ScreenTip = "Hyperlink Tip";

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

### Siehe auch

* class [BookmarkEnd](../../bookmarkend/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
