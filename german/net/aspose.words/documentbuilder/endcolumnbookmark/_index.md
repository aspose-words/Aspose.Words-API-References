---
title: DocumentBuilder.EndColumnBookmark
linktitle: EndColumnBookmark
articleTitle: EndColumnBookmark
second_title: Aspose.Words für .NET
description: Verwenden Sie die EndColumnBookmark-Methode von DocumentBuilder, um das Ende einer Spalte in Ihrem Dokument einfach zu markieren. Verbessern Sie die Tabellenverwaltung mit Präzision!
type: docs
weight: 220
url: /de/net/aspose.words/documentbuilder/endcolumnbookmark/
---
## DocumentBuilder.EndColumnBookmark method

Markiert die aktuelle Position im Dokument als Spaltenlesezeichenende. Die Position muss in einer Tabellenzelle liegen.

```csharp
public BookmarkEnd EndColumnBookmark(string bookmarkName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| bookmarkName | String | Name des Lesezeichens. |

### Rückgabewert

Der gerade erstellte Lesezeichen-Endknoten.

## Bemerkungen

Ein Spaltenlesezeichen umfasst eine oder mehrere Spalten in einem Zeilenbereich. Um ein gültiges Lesezeichen zu erstellen, müssen Sie beide aufrufen[`StartColumnBookmark`](../startcolumnbookmark/) Und`EndColumnBookmark` mit dem gleichen *bookmarkName* Parameter.

Falsch formatierte Lesezeichen oder Lesezeichen mit doppelten Namen werden beim Speichern des Dokuments ignoriert.

Die tatsächliche Position des eingefügten[`BookmarkEnd`](../../bookmarkend/) Knoten kann von der aktuellen Position des document builder abweichen.

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

* class [BookmarkEnd](../../bookmarkend/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
