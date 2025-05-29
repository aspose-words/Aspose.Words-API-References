---
title: BookmarksOutlineLevelCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „BookmarksOutlineLevelCollection Count“, um für eine effiziente Datenverwaltung einfach auf die Gesamtzahl der Elemente in Ihrer Sammlung zuzugreifen.
type: docs
weight: 20
url: /de/net/aspose.words.saving/bookmarksoutlinelevelcollection/count/
---
## BookmarksOutlineLevelCollection.Count property

Ruft die Anzahl der in der Sammlung enthaltenen Elemente ab.

```csharp
public int Count { get; }
```

## Beispiele

Zeigt, wie Gliederungsebenen für Lesezeichen festgelegt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügt ein Lesezeichen ein, in dem ein weiteres Lesezeichen verschachtelt ist.
builder.StartBookmark("Bookmark 1");
builder.Writeln("Text inside Bookmark 1.");

builder.StartBookmark("Bookmark 2");
builder.Writeln("Text inside Bookmark 1 and 2.");
builder.EndBookmark("Bookmark 2");

builder.Writeln("Text inside Bookmark 1.");
builder.EndBookmark("Bookmark 1");

// Ein weiteres Lesezeichen einfügen.
builder.StartBookmark("Bookmark 3");
builder.Writeln("Text inside Bookmark 3.");
builder.EndBookmark("Bookmark 3");

// Beim Speichern im PDF-Format können Lesezeichen über ein Dropdown-Menü aufgerufen und von den meisten Lesern als Anker verwendet werden.
// Lesezeichen können auch numerische Werte für Gliederungsebenen haben,
// Aktivieren von Gliederungseinträgen auf niedrigerer Ebene, um untergeordnete Einträge auf höherer Ebene auszublenden, wenn sie im Reader reduziert werden.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.OutlineOptions.BookmarksOutlineLevels;

outlineLevels.Add("Bookmark 1", 1);
outlineLevels.Add("Bookmark 2", 2);
outlineLevels.Add("Bookmark 3", 3);

Assert.AreEqual(3, outlineLevels.Count);
Assert.True(outlineLevels.Contains("Bookmark 1"));
Assert.AreEqual(1, outlineLevels[0]);
Assert.AreEqual(2, outlineLevels["Bookmark 2"]);
Assert.AreEqual(2, outlineLevels.IndexOfKey("Bookmark 3"));

// Wir können zwei Elemente entfernen, sodass nur noch die Gliederungsebenenbezeichnung für „Lesezeichen 1“ übrig bleibt.
outlineLevels.RemoveAt(2);
outlineLevels.Remove("Bookmark 2");

// Es gibt neun Gliederungsebenen. Ihre Nummerierung wird beim Speichern optimiert.
// In diesem Fall werden die Ebenen „5“ und „9“ zu „2“ und „3“.
outlineLevels.Add("Bookmark 2", 5);
outlineLevels.Add("Bookmark 3", 9);

doc.Save(ArtifactsDir + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// Durch das Leeren dieser Sammlung bleiben die Lesezeichen erhalten und werden alle auf die gleiche Gliederungsebene gesetzt.
outlineLevels.Clear();
```

### Siehe auch

* class [BookmarksOutlineLevelCollection](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
