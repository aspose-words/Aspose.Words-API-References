---
title: DocumentBuilder.StartBookmark
linktitle: StartBookmark
articleTitle: StartBookmark
second_title: Aspose.Words für .NET
description: DocumentBuilder StartBookmark methode. Markiert die aktuelle Position im Dokument als Lesezeichen start in C#.
type: docs
weight: 610
url: /de/net/aspose.words/documentbuilder/startbookmark/
---
## DocumentBuilder.StartBookmark method

Markiert die aktuelle Position im Dokument als Lesezeichen start.

```csharp
public BookmarkStart StartBookmark(string bookmarkName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| bookmarkName | String | Name des Lesezeichens. |

### Rückgabewert

Der gerade erstellte Lesezeichen-Startknoten.

## Bemerkungen

Lesezeichen in einem Dokument können sich überlappen und einen beliebigen Bereich umfassen. Um ein gültiges Lesezeichen zu erstellen, müssen Sie beide aufrufen`StartBookmark` Und[`EndBookmark`](../endbookmark/) mit dem gleichen*bookmarkName* -Parameter.

Falsch formatierte Lesezeichen oder Lesezeichen mit doppelten Namen werden beim Speichern des Dokuments ignoriert.

## Beispiele

Zeigt, wie ein Lesezeichen erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ein gültiges Lesezeichen muss den Dokumenttext enthalten
// BookmarkStart- und BookmarkEnd-Knoten, die mit einem passenden Lesezeichennamen erstellt wurden.
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

// Ein HYPERLINK-Feld einfügen, das auf das Lesezeichen verweist. Wir können Feldschalter passieren
// an die Methode „InsertHyperlink“ als Teil des Arguments, das den Namen des referenzierten Lesezeichens enthält.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Link to Bookmark1", @"Bookmark1"" \o ""Hyperlink Tip", true);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

### Siehe auch

* class [BookmarkStart](../../bookmarkstart/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
