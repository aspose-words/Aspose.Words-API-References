---
title: Class BookmarksOutlineLevelCollection
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.BookmarksOutlineLevelCollection klas. Eine Sammlung einzelner Lesezeichen auf Gliederungsebene.
type: docs
weight: 4850
url: /de/net/aspose.words.saving/bookmarksoutlinelevelcollection/
---
## BookmarksOutlineLevelCollection class

Eine Sammlung einzelner Lesezeichen auf Gliederungsebene.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Lesezeichen](https://docs.aspose.com/words/net/working-with-bookmarks/) Dokumentationsartikel.

```csharp
public class BookmarksOutlineLevelCollection : IEnumerable<KeyValuePair<string, int>>
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [BookmarksOutlineLevelCollection](bookmarksoutlinelevelcollection/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.saving/bookmarksoutlinelevelcollection/count/) { get; } | Ruft die Anzahl der in der Sammlung enthaltenen Elemente ab. |
| [Item](../../aspose.words.saving/bookmarksoutlinelevelcollection/item/) { get; set; } | Ruft eine Lesezeichen-Gliederungsebene anhand des Lesezeichennamens ab oder legt diese fest. (2 indexers) |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words.saving/bookmarksoutlinelevelcollection/add/)(string, int) | Fügt der Sammlung ein Lesezeichen hinzu. |
| [Clear](../../aspose.words.saving/bookmarksoutlinelevelcollection/clear/)() | Entfernt alle Elemente aus der Sammlung. |
| [Contains](../../aspose.words.saving/bookmarksoutlinelevelcollection/contains/)(string) | Ermittelt, ob die Sammlung ein Lesezeichen mit dem angegebenen Namen enthält. |
| [GetEnumerator](../../aspose.words.saving/bookmarksoutlinelevelcollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück, das zum Durchlaufen aller Elemente in der Sammlung verwendet werden kann. |
| [IndexOfKey](../../aspose.words.saving/bookmarksoutlinelevelcollection/indexofkey/)(string) | Gibt den nullbasierten Index des angegebenen Lesezeichens in der Sammlung zurück. |
| [Remove](../../aspose.words.saving/bookmarksoutlinelevelcollection/remove/)(string) | Entfernt ein Lesezeichen mit dem angegebenen Namen aus der Sammlung. |
| [RemoveAt](../../aspose.words.saving/bookmarksoutlinelevelcollection/removeat/)(int) | Entfernt ein Lesezeichen am angegebenen Index. |

### Bemerkungen

Der Schlüssel ist ein Lesezeichenname mit Zeichenkette, bei dem die Groß-/Kleinschreibung nicht beachtet wird. Der Wert ist eine int-Lesezeichen-Gliederungsebene.

Die Lesezeichen-Gliederungsebene kann ein Wert zwischen 0 und 9 sein. Geben Sie 0 an, und das Word-Lesezeichen wird nicht in der Dokumentgliederung angezeigt. Geben Sie 1 an, und das Word-Lesezeichen wird in der Dokumentgliederung auf Ebene 1 angezeigt. 2 für Level 2 und so weiter.

### Beispiele

Zeigt, wie Gliederungsebenen für Lesezeichen festgelegt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein Lesezeichen mit einem anderen darin verschachtelten Lesezeichen ein.
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

// Es gibt neun Gliederungsebenen. Ihre Nummerierung wird während des Speichervorgangs optimiert.
// In diesem Fall werden die Stufen „5“ und „9“ zu „2“ und „3“.
outlineLevels.Add("Bookmark 2", 5);
outlineLevels.Add("Bookmark 3", 9);

doc.Save(ArtifactsDir + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// Durch das Leeren dieser Sammlung bleiben die Lesezeichen erhalten und werden alle auf derselben Gliederungsebene platziert.
outlineLevels.Clear();
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)


