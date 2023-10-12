---
title: DocumentBuilder.StartColumnBookmark
second_title: Aspose.Words für .NET-API-Referenz
description: DocumentBuilder methode. Markiert die aktuelle Position im Dokument als Spaltenanfang eines Lesezeichens. Die Position muss in einer Tabellenzelle liegen.
type: docs
weight: 630
url: /de/net/aspose.words/documentbuilder/startcolumnbookmark/
---
## DocumentBuilder.StartColumnBookmark method

Markiert die aktuelle Position im Dokument als Spaltenanfang eines Lesezeichens. Die Position muss in einer Tabellenzelle liegen.

```csharp
public BookmarkStart StartColumnBookmark(string bookmarkName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| bookmarkName | String | Name des Lesezeichens. |

### Rückgabewert

Der gerade erstellte Lesezeichen-Startknoten.

### Bemerkungen

Ein Spaltenlesezeichen deckt eine oder mehrere Spalten in einem Zeilenbereich ab. Um ein gültiges Lesezeichen zu erstellen, müssen Sie beide aufrufen`StartColumnBookmark` Und[`EndColumnBookmark`](../endcolumnbookmark/) mit dem gleichen *bookmarkName*Parameter.

Falsch formatierte Lesezeichen oder Lesezeichen mit doppelten Namen werden beim Speichern des Dokuments ignoriert.

Die tatsächliche Position des eingefügten[`BookmarkStart`](../../bookmarkstart/) Der Knoten kann von der aktuellen document Builder-Position abweichen.

### Beispiele

Zeigt, wie ein Spaltenlesezeichen erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

builder.InsertCell();
// Zellen 1,2,4,5 werden mit einem Lesezeichen versehen.
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
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)


