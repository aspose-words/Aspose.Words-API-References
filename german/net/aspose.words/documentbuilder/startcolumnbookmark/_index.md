---
title: DocumentBuilder.StartColumnBookmark
linktitle: StartColumnBookmark
articleTitle: StartColumnBookmark
second_title: Aspose.Words für .NET
description: Verwenden Sie die StartColumnBookmark-Methode von DocumentBuilder, um Tabellenzellenpositionen einfach als Spaltenlesezeichen zu markieren und so die Dokumentnavigation und -organisation zu verbessern.
type: docs
weight: 660
url: /de/net/aspose.words/documentbuilder/startcolumnbookmark/
---
## DocumentBuilder.StartColumnBookmark method

Markiert die aktuelle Position im Dokument als Spaltenanfang. Die Position muss in einer Tabellenzelle liegen.

```csharp
public BookmarkStart StartColumnBookmark(string bookmarkName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| bookmarkName | String | Name des Lesezeichens. |

### Rückgabewert

Der gerade erstellte Lesezeichen-Startknoten.

## Bemerkungen

Ein Spaltenlesezeichen umfasst eine oder mehrere Spalten in einem Zeilenbereich. Um ein gültiges Lesezeichen zu erstellen, müssen Sie beide aufrufen`StartColumnBookmark` Und[`EndColumnBookmark`](../endcolumnbookmark/) mit dem gleichen *bookmarkName* Parameter.

Falsch formatierte Lesezeichen oder Lesezeichen mit doppelten Namen werden beim Speichern des Dokuments ignoriert.

Die tatsächliche Position des eingefügten[`BookmarkStart`](../../bookmarkstart/) Knoten kann von der aktuellen Position des document builder abweichen.

## Beispiele

Zeigt, wie ein Spaltenlesezeichen erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

builder.InsertCell();
// Die Zellen 1, 2, 4 und 5 werden mit einem Lesezeichen versehen.
builder.StartColumnBookmark("MyBookmark_1");
// Falsch formatierte Lesezeichen oder Lesezeichen mit doppelten Namen werden beim Speichern des Dokuments ignoriert.
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

### Siehe auch

* class [BookmarkStart](../../bookmarkstart/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
