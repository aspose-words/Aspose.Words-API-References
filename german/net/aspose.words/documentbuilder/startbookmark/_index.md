---
title: DocumentBuilder.StartBookmark
linktitle: StartBookmark
articleTitle: StartBookmark
second_title: Aspose.Words für .NET
description: Nutzen Sie die StartBookmark-Methode von DocumentBuilder, um wichtige Positionen in Ihrem Dokument mühelos zu markieren und zu verwalten und so die Organisation und Navigation zu verbessern.
type: docs
weight: 650
url: /de/net/aspose.words/documentbuilder/startbookmark/
---
## DocumentBuilder.StartBookmark method

Markiert die aktuelle Position im Dokument als Lesezeichenanfang.

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

* class [BookmarkStart](../../bookmarkstart/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
