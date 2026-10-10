---
title: "BookmarksOutlineLevelCollection"
linktitle: "BookmarksOutlineLevelCollection"
second_title: "Aspose.Words für Java"
description: "Eine Sammlung von einzelnen Lesezeichen-Gliederungsebenen in Java."
type: docs
weight: 45
url: /de/java/com.aspose.words/bookmarksoutlinelevelcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class BookmarksOutlineLevelCollection implements Iterable
```

Eine Sammlung von einzelnen Lesezeichen-Gliederungsebenen.

Um mehr zu erfahren, besuchen Sie die [ Working with Bookmarks ][Working with Bookmarks] Dokumentationsartikel.

 **Remarks:** 

Der Schlüssel ist ein case-insensitiver Zeichenketten-Lesezeichename. Der Wert ist ein int-Lesezeichen-Gliederungslevel.

Der Lesezeichen-Gliederungslevel kann einen Wert von 0 bis 9 haben. Gibt man 0 an, wird das Word-Lesezeichen nicht in der Dokumenten-Gliederung angezeigt. Gibt man 1 an, wird das Word-Lesezeichen in der Dokumenten-Gliederung auf Ebene 1 angezeigt; 2 für Ebene 2 und so weiter.

 **Examples:** 

Zeigt, wie man Gliederungsebenen für Lesezeichen festlegt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a bookmark with another bookmark nested inside it.
 builder.startBookmark("Bookmark 1");
 builder.writeln("Text inside Bookmark 1.");

 builder.startBookmark("Bookmark 2");
 builder.writeln("Text inside Bookmark 1 and 2.");
 builder.endBookmark("Bookmark 2");

 builder.writeln("Text inside Bookmark 1.");
 builder.endBookmark("Bookmark 1");

 // Insert another bookmark.
 builder.startBookmark("Bookmark 3");
 builder.writeln("Text inside Bookmark 3.");
 builder.endBookmark("Bookmark 3");

 // When saving to .pdf, bookmarks can be accessed via a drop-down menu and used as anchors by most readers.
 // Bookmarks can also have numeric values for outline levels,
 // enabling lower level outline entries to hide higher-level child entries when collapsed in the reader.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.getOutlineOptions().getBookmarksOutlineLevels();

 outlineLevels.add("Bookmark 1", 1);
 outlineLevels.add("Bookmark 2", 2);
 outlineLevels.add("Bookmark 3", 3);

 Assert.assertEquals(outlineLevels.getCount(), 3);
 Assert.assertTrue(outlineLevels.contains("Bookmark 1"));
 Assert.assertEquals(outlineLevels.get(0), 1);
 Assert.assertEquals(outlineLevels.get("Bookmark 2"), 2);
 Assert.assertEquals(outlineLevels.indexOfKey("Bookmark 3"), 2);

 // We can remove two elements so that only the outline level designation for "Bookmark 1" is left.
 outlineLevels.removeAt(2);
 outlineLevels.remove("Bookmark 2");

 // There are nine outline levels. Their numbering will be optimized during the save operation.
 // In this case, levels "5" and "9" will become "2" and "3".
 outlineLevels.add("Bookmark 2", 5);
 outlineLevels.add("Bookmark 3", 9);

 doc.save(getArtifactsDir() + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

 // Emptying this collection will preserve the bookmarks and put them all on the same outline level.
 outlineLevels.clear();
 
```


[Working with Bookmarks]: https://docs.aspose.com/words/java/working-with-bookmarks/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [add(String name, int outlineLevel)](#add-java.lang.String-int) | Fügt ein Lesezeichen zur Sammlung hinzu. |
| [clear()](#clear) | Entfernt alle Elemente aus der Sammlung. |
| [contains(String name)](#contains-java.lang.String) | Bestimmt, ob die Sammlung ein Lesezeichen mit dem angegebenen Namen enthält. |
| [get(int index)](#get-int) | Liest den Lesezeichen-Gliederungslevel am angegebenen Index. |
| [get(String name)](#get-java.lang.String) | Stellt Zugriff auf die Elemente der Sammlung bereit. |
| [getCount()](#getCount) | Ermittelt die Anzahl der im Sammelobjekt enthaltenen Elemente. |
| [indexOfKey(String name)](#indexOfKey-java.lang.String) | Gibt den nullbasierten Index des angegebenen Lesezeichens in der Sammlung zurück. |
| [iterator()](#iterator) | Gibt ein Iterator-Objekt zurück, das verwendet werden kann, um über alle Elemente in der Sammlung zu iterieren. |
| [remove(String name)](#remove-java.lang.String) | Entfernt ein Lesezeichen mit dem angegebenen Namen aus der Sammlung. |
| [removeAt(int index)](#removeAt-int) | Entfernt ein Lesezeichen am angegebenen Index. |
| [set(int index, int value)](#set-int-int) | Setzt den Lesezeichen-Gliederungslevel am angegebenen Index. |
| [set(String name, int value)](#set-java.lang.String-int) | Stellt Zugriff auf die Elemente der Sammlung bereit. |
### add(String name, int outlineLevel) {#add-java.lang.String-int}
```
public void add(String name, int outlineLevel)
```


Fügt ein Lesezeichen zur Sammlung hinzu.

 **Examples:** 

Zeigt, wie man Gliederungsebenen für Lesezeichen festlegt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a bookmark with another bookmark nested inside it.
 builder.startBookmark("Bookmark 1");
 builder.writeln("Text inside Bookmark 1.");

 builder.startBookmark("Bookmark 2");
 builder.writeln("Text inside Bookmark 1 and 2.");
 builder.endBookmark("Bookmark 2");

 builder.writeln("Text inside Bookmark 1.");
 builder.endBookmark("Bookmark 1");

 // Insert another bookmark.
 builder.startBookmark("Bookmark 3");
 builder.writeln("Text inside Bookmark 3.");
 builder.endBookmark("Bookmark 3");

 // When saving to .pdf, bookmarks can be accessed via a drop-down menu and used as anchors by most readers.
 // Bookmarks can also have numeric values for outline levels,
 // enabling lower level outline entries to hide higher-level child entries when collapsed in the reader.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.getOutlineOptions().getBookmarksOutlineLevels();

 outlineLevels.add("Bookmark 1", 1);
 outlineLevels.add("Bookmark 2", 2);
 outlineLevels.add("Bookmark 3", 3);

 Assert.assertEquals(outlineLevels.getCount(), 3);
 Assert.assertTrue(outlineLevels.contains("Bookmark 1"));
 Assert.assertEquals(outlineLevels.get(0), 1);
 Assert.assertEquals(outlineLevels.get("Bookmark 2"), 2);
 Assert.assertEquals(outlineLevels.indexOfKey("Bookmark 3"), 2);

 // We can remove two elements so that only the outline level designation for "Bookmark 1" is left.
 outlineLevels.removeAt(2);
 outlineLevels.remove("Bookmark 2");

 // There are nine outline levels. Their numbering will be optimized during the save operation.
 // In this case, levels "5" and "9" will become "2" and "3".
 outlineLevels.add("Bookmark 2", 5);
 outlineLevels.add("Bookmark 3", 9);

 doc.save(getArtifactsDir() + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

 // Emptying this collection will preserve the bookmarks and put them all on the same outline level.
 outlineLevels.clear();
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der nicht groß-/kleinschreibungssensible Name des Lesezeichens, das hinzugefügt werden soll. |
| outlineLevel | int | Die Gliederungsebene des Lesezeichens. Gültiger Bereich ist 0 bis 9. |

### clear() {#clear}
```
public void clear()
```


Entfernt alle Elemente aus der Sammlung.

 **Examples:** 

Zeigt, wie man Gliederungsebenen für Lesezeichen festlegt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a bookmark with another bookmark nested inside it.
 builder.startBookmark("Bookmark 1");
 builder.writeln("Text inside Bookmark 1.");

 builder.startBookmark("Bookmark 2");
 builder.writeln("Text inside Bookmark 1 and 2.");
 builder.endBookmark("Bookmark 2");

 builder.writeln("Text inside Bookmark 1.");
 builder.endBookmark("Bookmark 1");

 // Insert another bookmark.
 builder.startBookmark("Bookmark 3");
 builder.writeln("Text inside Bookmark 3.");
 builder.endBookmark("Bookmark 3");

 // When saving to .pdf, bookmarks can be accessed via a drop-down menu and used as anchors by most readers.
 // Bookmarks can also have numeric values for outline levels,
 // enabling lower level outline entries to hide higher-level child entries when collapsed in the reader.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.getOutlineOptions().getBookmarksOutlineLevels();

 outlineLevels.add("Bookmark 1", 1);
 outlineLevels.add("Bookmark 2", 2);
 outlineLevels.add("Bookmark 3", 3);

 Assert.assertEquals(outlineLevels.getCount(), 3);
 Assert.assertTrue(outlineLevels.contains("Bookmark 1"));
 Assert.assertEquals(outlineLevels.get(0), 1);
 Assert.assertEquals(outlineLevels.get("Bookmark 2"), 2);
 Assert.assertEquals(outlineLevels.indexOfKey("Bookmark 3"), 2);

 // We can remove two elements so that only the outline level designation for "Bookmark 1" is left.
 outlineLevels.removeAt(2);
 outlineLevels.remove("Bookmark 2");

 // There are nine outline levels. Their numbering will be optimized during the save operation.
 // In this case, levels "5" and "9" will become "2" and "3".
 outlineLevels.add("Bookmark 2", 5);
 outlineLevels.add("Bookmark 3", 9);

 doc.save(getArtifactsDir() + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

 // Emptying this collection will preserve the bookmarks and put them all on the same outline level.
 outlineLevels.clear();
 
```

### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


Bestimmt, ob die Sammlung ein Lesezeichen mit dem angegebenen Namen enthält.

 **Examples:** 

Zeigt, wie man Gliederungsebenen für Lesezeichen festlegt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a bookmark with another bookmark nested inside it.
 builder.startBookmark("Bookmark 1");
 builder.writeln("Text inside Bookmark 1.");

 builder.startBookmark("Bookmark 2");
 builder.writeln("Text inside Bookmark 1 and 2.");
 builder.endBookmark("Bookmark 2");

 builder.writeln("Text inside Bookmark 1.");
 builder.endBookmark("Bookmark 1");

 // Insert another bookmark.
 builder.startBookmark("Bookmark 3");
 builder.writeln("Text inside Bookmark 3.");
 builder.endBookmark("Bookmark 3");

 // When saving to .pdf, bookmarks can be accessed via a drop-down menu and used as anchors by most readers.
 // Bookmarks can also have numeric values for outline levels,
 // enabling lower level outline entries to hide higher-level child entries when collapsed in the reader.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.getOutlineOptions().getBookmarksOutlineLevels();

 outlineLevels.add("Bookmark 1", 1);
 outlineLevels.add("Bookmark 2", 2);
 outlineLevels.add("Bookmark 3", 3);

 Assert.assertEquals(outlineLevels.getCount(), 3);
 Assert.assertTrue(outlineLevels.contains("Bookmark 1"));
 Assert.assertEquals(outlineLevels.get(0), 1);
 Assert.assertEquals(outlineLevels.get("Bookmark 2"), 2);
 Assert.assertEquals(outlineLevels.indexOfKey("Bookmark 3"), 2);

 // We can remove two elements so that only the outline level designation for "Bookmark 1" is left.
 outlineLevels.removeAt(2);
 outlineLevels.remove("Bookmark 2");

 // There are nine outline levels. Their numbering will be optimized during the save operation.
 // In this case, levels "5" and "9" will become "2" and "3".
 outlineLevels.add("Bookmark 2", 5);
 outlineLevels.add("Bookmark 3", 9);

 doc.save(getArtifactsDir() + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

 // Emptying this collection will preserve the bookmarks and put them all on the same outline level.
 outlineLevels.clear();
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Nicht groß-/kleinschreibungssensitiver Name des Lesezeichens, das zu finden ist. |

**Returns:**
boolean - true, wenn das Element in der Sammlung gefunden wird; andernfalls false.
### get(int index) {#get-int}
```
public int get(int index)
```


Liest den Lesezeichen-Gliederungslevel am angegebenen Index.

 **Examples:** 

Zeigt, wie man Gliederungsebenen für Lesezeichen festlegt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a bookmark with another bookmark nested inside it.
 builder.startBookmark("Bookmark 1");
 builder.writeln("Text inside Bookmark 1.");

 builder.startBookmark("Bookmark 2");
 builder.writeln("Text inside Bookmark 1 and 2.");
 builder.endBookmark("Bookmark 2");

 builder.writeln("Text inside Bookmark 1.");
 builder.endBookmark("Bookmark 1");

 // Insert another bookmark.
 builder.startBookmark("Bookmark 3");
 builder.writeln("Text inside Bookmark 3.");
 builder.endBookmark("Bookmark 3");

 // When saving to .pdf, bookmarks can be accessed via a drop-down menu and used as anchors by most readers.
 // Bookmarks can also have numeric values for outline levels,
 // enabling lower level outline entries to hide higher-level child entries when collapsed in the reader.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.getOutlineOptions().getBookmarksOutlineLevels();

 outlineLevels.add("Bookmark 1", 1);
 outlineLevels.add("Bookmark 2", 2);
 outlineLevels.add("Bookmark 3", 3);

 Assert.assertEquals(outlineLevels.getCount(), 3);
 Assert.assertTrue(outlineLevels.contains("Bookmark 1"));
 Assert.assertEquals(outlineLevels.get(0), 1);
 Assert.assertEquals(outlineLevels.get("Bookmark 2"), 2);
 Assert.assertEquals(outlineLevels.indexOfKey("Bookmark 3"), 2);

 // We can remove two elements so that only the outline level designation for "Bookmark 1" is left.
 outlineLevels.removeAt(2);
 outlineLevels.remove("Bookmark 2");

 // There are nine outline levels. Their numbering will be optimized during the save operation.
 // In this case, levels "5" and "9" will become "2" and "3".
 outlineLevels.add("Bookmark 2", 5);
 outlineLevels.add("Bookmark 3", 9);

 doc.save(getArtifactsDir() + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

 // Emptying this collection will preserve the bookmarks and put them all on the same outline level.
 outlineLevels.clear();
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Nullbasierter Index des Lesezeichens. |

**Returns:**
int – Die Gliederungsebene des Lesezeichens. Gültiger Bereich ist 0 bis 9.
### get(String name) {#get-java.lang.String}
```
public int get(String name)
```


Stellt Zugriff auf die Sammlungs‑Elemente bereit. Ruft die Gliederungsebene eines Lesezeichens anhand des Lesezeichennamens ab oder setzt sie.

 **Examples:** 

Zeigt, wie man Gliederungsebenen für Lesezeichen festlegt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a bookmark with another bookmark nested inside it.
 builder.startBookmark("Bookmark 1");
 builder.writeln("Text inside Bookmark 1.");

 builder.startBookmark("Bookmark 2");
 builder.writeln("Text inside Bookmark 1 and 2.");
 builder.endBookmark("Bookmark 2");

 builder.writeln("Text inside Bookmark 1.");
 builder.endBookmark("Bookmark 1");

 // Insert another bookmark.
 builder.startBookmark("Bookmark 3");
 builder.writeln("Text inside Bookmark 3.");
 builder.endBookmark("Bookmark 3");

 // When saving to .pdf, bookmarks can be accessed via a drop-down menu and used as anchors by most readers.
 // Bookmarks can also have numeric values for outline levels,
 // enabling lower level outline entries to hide higher-level child entries when collapsed in the reader.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.getOutlineOptions().getBookmarksOutlineLevels();

 outlineLevels.add("Bookmark 1", 1);
 outlineLevels.add("Bookmark 2", 2);
 outlineLevels.add("Bookmark 3", 3);

 Assert.assertEquals(outlineLevels.getCount(), 3);
 Assert.assertTrue(outlineLevels.contains("Bookmark 1"));
 Assert.assertEquals(outlineLevels.get(0), 1);
 Assert.assertEquals(outlineLevels.get("Bookmark 2"), 2);
 Assert.assertEquals(outlineLevels.indexOfKey("Bookmark 3"), 2);

 // We can remove two elements so that only the outline level designation for "Bookmark 1" is left.
 outlineLevels.removeAt(2);
 outlineLevels.remove("Bookmark 2");

 // There are nine outline levels. Their numbering will be optimized during the save operation.
 // In this case, levels "5" and "9" will become "2" and "3".
 outlineLevels.add("Bookmark 2", 5);
 outlineLevels.add("Bookmark 3", 9);

 doc.save(getArtifactsDir() + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

 // Emptying this collection will preserve the bookmarks and put them all on the same outline level.
 outlineLevels.clear();
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Nicht groß-/kleinschreibungssensitiver Name des Lesezeichens. |

**Returns:**
int – Die Gliederungsebene des Lesezeichens. Gültiger Bereich ist 0 bis 9.
### getCount() {#getCount}
```
public int getCount()
```


Ermittelt die Anzahl der im Sammelobjekt enthaltenen Elemente.

 **Examples:** 

Zeigt, wie man Gliederungsebenen für Lesezeichen festlegt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a bookmark with another bookmark nested inside it.
 builder.startBookmark("Bookmark 1");
 builder.writeln("Text inside Bookmark 1.");

 builder.startBookmark("Bookmark 2");
 builder.writeln("Text inside Bookmark 1 and 2.");
 builder.endBookmark("Bookmark 2");

 builder.writeln("Text inside Bookmark 1.");
 builder.endBookmark("Bookmark 1");

 // Insert another bookmark.
 builder.startBookmark("Bookmark 3");
 builder.writeln("Text inside Bookmark 3.");
 builder.endBookmark("Bookmark 3");

 // When saving to .pdf, bookmarks can be accessed via a drop-down menu and used as anchors by most readers.
 // Bookmarks can also have numeric values for outline levels,
 // enabling lower level outline entries to hide higher-level child entries when collapsed in the reader.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.getOutlineOptions().getBookmarksOutlineLevels();

 outlineLevels.add("Bookmark 1", 1);
 outlineLevels.add("Bookmark 2", 2);
 outlineLevels.add("Bookmark 3", 3);

 Assert.assertEquals(outlineLevels.getCount(), 3);
 Assert.assertTrue(outlineLevels.contains("Bookmark 1"));
 Assert.assertEquals(outlineLevels.get(0), 1);
 Assert.assertEquals(outlineLevels.get("Bookmark 2"), 2);
 Assert.assertEquals(outlineLevels.indexOfKey("Bookmark 3"), 2);

 // We can remove two elements so that only the outline level designation for "Bookmark 1" is left.
 outlineLevels.removeAt(2);
 outlineLevels.remove("Bookmark 2");

 // There are nine outline levels. Their numbering will be optimized during the save operation.
 // In this case, levels "5" and "9" will become "2" and "3".
 outlineLevels.add("Bookmark 2", 5);
 outlineLevels.add("Bookmark 3", 9);

 doc.save(getArtifactsDir() + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

 // Emptying this collection will preserve the bookmarks and put them all on the same outline level.
 outlineLevels.clear();
 
```

**Returns:**
int – Die Anzahl der im Sammelobjekt enthaltenen Elemente.
### indexOfKey(String name) {#indexOfKey-java.lang.String}
```
public int indexOfKey(String name)
```


Gibt den nullbasierten Index des angegebenen Lesezeichens in der Sammlung zurück.

 **Examples:** 

Zeigt, wie man Gliederungsebenen für Lesezeichen festlegt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a bookmark with another bookmark nested inside it.
 builder.startBookmark("Bookmark 1");
 builder.writeln("Text inside Bookmark 1.");

 builder.startBookmark("Bookmark 2");
 builder.writeln("Text inside Bookmark 1 and 2.");
 builder.endBookmark("Bookmark 2");

 builder.writeln("Text inside Bookmark 1.");
 builder.endBookmark("Bookmark 1");

 // Insert another bookmark.
 builder.startBookmark("Bookmark 3");
 builder.writeln("Text inside Bookmark 3.");
 builder.endBookmark("Bookmark 3");

 // When saving to .pdf, bookmarks can be accessed via a drop-down menu and used as anchors by most readers.
 // Bookmarks can also have numeric values for outline levels,
 // enabling lower level outline entries to hide higher-level child entries when collapsed in the reader.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.getOutlineOptions().getBookmarksOutlineLevels();

 outlineLevels.add("Bookmark 1", 1);
 outlineLevels.add("Bookmark 2", 2);
 outlineLevels.add("Bookmark 3", 3);

 Assert.assertEquals(outlineLevels.getCount(), 3);
 Assert.assertTrue(outlineLevels.contains("Bookmark 1"));
 Assert.assertEquals(outlineLevels.get(0), 1);
 Assert.assertEquals(outlineLevels.get("Bookmark 2"), 2);
 Assert.assertEquals(outlineLevels.indexOfKey("Bookmark 3"), 2);

 // We can remove two elements so that only the outline level designation for "Bookmark 1" is left.
 outlineLevels.removeAt(2);
 outlineLevels.remove("Bookmark 2");

 // There are nine outline levels. Their numbering will be optimized during the save operation.
 // In this case, levels "5" and "9" will become "2" and "3".
 outlineLevels.add("Bookmark 2", 5);
 outlineLevels.add("Bookmark 3", 9);

 doc.save(getArtifactsDir() + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

 // Emptying this collection will preserve the bookmarks and put them all on the same outline level.
 outlineLevels.clear();
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der nicht groß-/kleinschreibungssensible Name des Lesezeichens. |

**Returns:**
int - Der nullbasierte Index. Negativer Wert, wenn nicht gefunden.
### iterator() {#iterator}
```
public Iterator iterator()
```


Gibt ein Iterator-Objekt zurück, das verwendet werden kann, um über alle Elemente in der Sammlung zu iterieren.

**Returns:**
java.util.Iterator
### remove(String name) {#remove-java.lang.String}
```
public void remove(String name)
```


Entfernt ein Lesezeichen mit dem angegebenen Namen aus der Sammlung.

 **Examples:** 

Zeigt, wie man Gliederungsebenen für Lesezeichen festlegt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a bookmark with another bookmark nested inside it.
 builder.startBookmark("Bookmark 1");
 builder.writeln("Text inside Bookmark 1.");

 builder.startBookmark("Bookmark 2");
 builder.writeln("Text inside Bookmark 1 and 2.");
 builder.endBookmark("Bookmark 2");

 builder.writeln("Text inside Bookmark 1.");
 builder.endBookmark("Bookmark 1");

 // Insert another bookmark.
 builder.startBookmark("Bookmark 3");
 builder.writeln("Text inside Bookmark 3.");
 builder.endBookmark("Bookmark 3");

 // When saving to .pdf, bookmarks can be accessed via a drop-down menu and used as anchors by most readers.
 // Bookmarks can also have numeric values for outline levels,
 // enabling lower level outline entries to hide higher-level child entries when collapsed in the reader.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.getOutlineOptions().getBookmarksOutlineLevels();

 outlineLevels.add("Bookmark 1", 1);
 outlineLevels.add("Bookmark 2", 2);
 outlineLevels.add("Bookmark 3", 3);

 Assert.assertEquals(outlineLevels.getCount(), 3);
 Assert.assertTrue(outlineLevels.contains("Bookmark 1"));
 Assert.assertEquals(outlineLevels.get(0), 1);
 Assert.assertEquals(outlineLevels.get("Bookmark 2"), 2);
 Assert.assertEquals(outlineLevels.indexOfKey("Bookmark 3"), 2);

 // We can remove two elements so that only the outline level designation for "Bookmark 1" is left.
 outlineLevels.removeAt(2);
 outlineLevels.remove("Bookmark 2");

 // There are nine outline levels. Their numbering will be optimized during the save operation.
 // In this case, levels "5" and "9" will become "2" and "3".
 outlineLevels.add("Bookmark 2", 5);
 outlineLevels.add("Bookmark 3", 9);

 doc.save(getArtifactsDir() + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

 // Emptying this collection will preserve the bookmarks and put them all on the same outline level.
 outlineLevels.clear();
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der nicht groß-/kleinschreibungssensible Name des Lesezeichens. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Entfernt ein Lesezeichen am angegebenen Index.

 **Examples:** 

Zeigt, wie man Gliederungsebenen für Lesezeichen festlegt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a bookmark with another bookmark nested inside it.
 builder.startBookmark("Bookmark 1");
 builder.writeln("Text inside Bookmark 1.");

 builder.startBookmark("Bookmark 2");
 builder.writeln("Text inside Bookmark 1 and 2.");
 builder.endBookmark("Bookmark 2");

 builder.writeln("Text inside Bookmark 1.");
 builder.endBookmark("Bookmark 1");

 // Insert another bookmark.
 builder.startBookmark("Bookmark 3");
 builder.writeln("Text inside Bookmark 3.");
 builder.endBookmark("Bookmark 3");

 // When saving to .pdf, bookmarks can be accessed via a drop-down menu and used as anchors by most readers.
 // Bookmarks can also have numeric values for outline levels,
 // enabling lower level outline entries to hide higher-level child entries when collapsed in the reader.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.getOutlineOptions().getBookmarksOutlineLevels();

 outlineLevels.add("Bookmark 1", 1);
 outlineLevels.add("Bookmark 2", 2);
 outlineLevels.add("Bookmark 3", 3);

 Assert.assertEquals(outlineLevels.getCount(), 3);
 Assert.assertTrue(outlineLevels.contains("Bookmark 1"));
 Assert.assertEquals(outlineLevels.get(0), 1);
 Assert.assertEquals(outlineLevels.get("Bookmark 2"), 2);
 Assert.assertEquals(outlineLevels.indexOfKey("Bookmark 3"), 2);

 // We can remove two elements so that only the outline level designation for "Bookmark 1" is left.
 outlineLevels.removeAt(2);
 outlineLevels.remove("Bookmark 2");

 // There are nine outline levels. Their numbering will be optimized during the save operation.
 // In this case, levels "5" and "9" will become "2" and "3".
 outlineLevels.add("Bookmark 2", 5);
 outlineLevels.add("Bookmark 3", 9);

 doc.save(getArtifactsDir() + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

 // Emptying this collection will preserve the bookmarks and put them all on the same outline level.
 outlineLevels.clear();
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Der nullbasierte Index. |

### set(int index, int value) {#set-int-int}
```
public void set(int index, int value)
```


Setzt den Lesezeichen-Gliederungslevel am angegebenen Index.

 **Examples:** 

Zeigt, wie man Gliederungsebenen für Lesezeichen festlegt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a bookmark with another bookmark nested inside it.
 builder.startBookmark("Bookmark 1");
 builder.writeln("Text inside Bookmark 1.");

 builder.startBookmark("Bookmark 2");
 builder.writeln("Text inside Bookmark 1 and 2.");
 builder.endBookmark("Bookmark 2");

 builder.writeln("Text inside Bookmark 1.");
 builder.endBookmark("Bookmark 1");

 // Insert another bookmark.
 builder.startBookmark("Bookmark 3");
 builder.writeln("Text inside Bookmark 3.");
 builder.endBookmark("Bookmark 3");

 // When saving to .pdf, bookmarks can be accessed via a drop-down menu and used as anchors by most readers.
 // Bookmarks can also have numeric values for outline levels,
 // enabling lower level outline entries to hide higher-level child entries when collapsed in the reader.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.getOutlineOptions().getBookmarksOutlineLevels();

 outlineLevels.add("Bookmark 1", 1);
 outlineLevels.add("Bookmark 2", 2);
 outlineLevels.add("Bookmark 3", 3);

 Assert.assertEquals(outlineLevels.getCount(), 3);
 Assert.assertTrue(outlineLevels.contains("Bookmark 1"));
 Assert.assertEquals(outlineLevels.get(0), 1);
 Assert.assertEquals(outlineLevels.get("Bookmark 2"), 2);
 Assert.assertEquals(outlineLevels.indexOfKey("Bookmark 3"), 2);

 // We can remove two elements so that only the outline level designation for "Bookmark 1" is left.
 outlineLevels.removeAt(2);
 outlineLevels.remove("Bookmark 2");

 // There are nine outline levels. Their numbering will be optimized during the save operation.
 // In this case, levels "5" and "9" will become "2" and "3".
 outlineLevels.add("Bookmark 2", 5);
 outlineLevels.add("Bookmark 3", 9);

 doc.save(getArtifactsDir() + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

 // Emptying this collection will preserve the bookmarks and put them all on the same outline level.
 outlineLevels.clear();
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Nullbasierter Index des Lesezeichens. |
| Wert | int | Die Gliederungsebene des Lesezeichens. Gültiger Bereich ist 0 bis 9. |

### set(String name, int value) {#set-java.lang.String-int}
```
public void set(String name, int value)
```


Stellt Zugriff auf die Sammlungs‑Elemente bereit. Ruft die Gliederungsebene eines Lesezeichens anhand des Lesezeichennamens ab oder setzt sie.

 **Examples:** 

Zeigt, wie man Gliederungsebenen für Lesezeichen festlegt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a bookmark with another bookmark nested inside it.
 builder.startBookmark("Bookmark 1");
 builder.writeln("Text inside Bookmark 1.");

 builder.startBookmark("Bookmark 2");
 builder.writeln("Text inside Bookmark 1 and 2.");
 builder.endBookmark("Bookmark 2");

 builder.writeln("Text inside Bookmark 1.");
 builder.endBookmark("Bookmark 1");

 // Insert another bookmark.
 builder.startBookmark("Bookmark 3");
 builder.writeln("Text inside Bookmark 3.");
 builder.endBookmark("Bookmark 3");

 // When saving to .pdf, bookmarks can be accessed via a drop-down menu and used as anchors by most readers.
 // Bookmarks can also have numeric values for outline levels,
 // enabling lower level outline entries to hide higher-level child entries when collapsed in the reader.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.getOutlineOptions().getBookmarksOutlineLevels();

 outlineLevels.add("Bookmark 1", 1);
 outlineLevels.add("Bookmark 2", 2);
 outlineLevels.add("Bookmark 3", 3);

 Assert.assertEquals(outlineLevels.getCount(), 3);
 Assert.assertTrue(outlineLevels.contains("Bookmark 1"));
 Assert.assertEquals(outlineLevels.get(0), 1);
 Assert.assertEquals(outlineLevels.get("Bookmark 2"), 2);
 Assert.assertEquals(outlineLevels.indexOfKey("Bookmark 3"), 2);

 // We can remove two elements so that only the outline level designation for "Bookmark 1" is left.
 outlineLevels.removeAt(2);
 outlineLevels.remove("Bookmark 2");

 // There are nine outline levels. Their numbering will be optimized during the save operation.
 // In this case, levels "5" and "9" will become "2" and "3".
 outlineLevels.add("Bookmark 2", 5);
 outlineLevels.add("Bookmark 3", 9);

 doc.save(getArtifactsDir() + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

 // Emptying this collection will preserve the bookmarks and put them all on the same outline level.
 outlineLevels.clear();
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Nicht groß-/kleinschreibungssensitiver Name des Lesezeichens. |
| Wert | int | Die Gliederungsebene des Lesezeichens. Gültiger Bereich ist 0 bis 9. |

