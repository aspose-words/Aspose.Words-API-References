---
title: "BookmarkCollection"
linktitle: "BookmarkCollection"
second_title: "Aspose.Words für Java"
description: "Eine Sammlung von Bookmark-Objekten, die die Lesezeichen im angegebenen Bereich in Java darstellen."
type: docs
weight: 42
url: /de/java/com.aspose.words/bookmarkcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class BookmarkCollection implements Iterable
```

Eine Sammlung von [Bookmark](../../com.aspose.words/bookmark/) Objekten, die die Lesezeichen im angegebenen Bereich darstellen.

Um mehr zu erfahren, besuchen Sie die [ Working with Bookmarks ][Working with Bookmarks] Dokumentationsartikel.

 **Examples:** 

Zeigt, wie man Lesezeichen hinzufügt und deren Inhalte aktualisiert.

```

 public void createUpdateAndPrintBookmarks() throws Exception {
     // Create a document with three bookmarks, then use a custom document visitor implementation to print their contents.
     Document doc = createDocumentWithBookmarks(3);
     BookmarkCollection bookmarks = doc.getRange().getBookmarks();
     printAllBookmarkInfo(bookmarks);

     // Bookmarks can be accessed in the bookmark collection by index or name, and their names can be updated.
     bookmarks.get(0).setName("{bookmarks[0].Name}_NewName");
     bookmarks.get("MyBookmark_2").setText("Updated text contents of {bookmarks[1].Name}");

     // Print all bookmarks again to see updated values.
     printAllBookmarkInfo(bookmarks);
 }

 /// 
 /// Create a document with a given number of bookmarks.
 /// 
 private static Document createDocumentWithBookmarks(int numberOfBookmarks) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     for (int i = 1; i <= numberOfBookmarks; i++) {
         String bookmarkName = "MyBookmark_" + i;

         builder.write("Text before bookmark.");
         builder.startBookmark(bookmarkName);
         builder.write(MessageFormat.format("Text inside {0}.", bookmarkName));
         builder.endBookmark(bookmarkName);
         builder.writeln("Text after bookmark.");
     }

     return doc;
 }

 /// 
 /// Use an iterator and a visitor to print info of every bookmark in the collection.
 /// 
 private static void printAllBookmarkInfo(BookmarkCollection bookmarks) throws Exception {
     BookmarkInfoPrinter bookmarkVisitor = new BookmarkInfoPrinter();

     // Get each bookmark in the collection to accept a visitor that will print its contents.
     Iterator enumerator = bookmarks.iterator();

     while (enumerator.hasNext()) {
         Bookmark currentBookmark = enumerator.next();

         if (currentBookmark != null) {
             currentBookmark.getBookmarkStart().accept(bookmarkVisitor);
             currentBookmark.getBookmarkEnd().accept(bookmarkVisitor);

             System.out.println(currentBookmark.getBookmarkStart().getText());
         }
     }
 }

 /// 
 /// Prints contents of every visited bookmark to the console.
 /// 
 public static class BookmarkInfoPrinter extends DocumentVisitor {
     public int visitBookmarkStart(BookmarkStart bookmarkStart) throws Exception {
         System.out.println(MessageFormat.format("BookmarkStart name: \"{0}\", Content: \"{1}\"", bookmarkStart.getName(),
                 bookmarkStart.getBookmark().getText()));
         return VisitorAction.CONTINUE;
     }

     public int visitBookmarkEnd(BookmarkEnd bookmarkEnd) {
         System.out.println(MessageFormat.format("BookmarkEnd name: \"{0}\"", bookmarkEnd.getName()));
         return VisitorAction.CONTINUE;
     }
 }
 
```


[Working with Bookmarks]: https://docs.aspose.com/words/java/working-with-bookmarks/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [clear()](#clear) | Entfernt alle Lesezeichen aus dieser Sammlung und aus dem Dokument. |
| [get(int index)](#get-int) | Gibt ein Lesezeichen am angegebenen Index zurück. |
| [get(String bookmarkName)](#get-java.lang.String) | Gibt ein Lesezeichen nach Namen zurück. |
| [getCount()](#getCount) | Gibt die Anzahl der Lesezeichen in der Sammlung zurück. |
| [iterator()](#iterator) | Gibt ein Enumerator‑Objekt zurück. |
| [remove(Bookmark bookmark)](#remove-com.aspose.words.Bookmark) | Entfernt das angegebene Lesezeichen aus dem Dokument. |
| [remove(String bookmarkName)](#remove-java.lang.String) | Entfernt ein Lesezeichen mit dem angegebenen Namen. |
| [removeAt(int index)](#removeAt-int) | Entfernt ein Lesezeichen am angegebenen Index. |
### clear() {#clear}
```
public void clear()
```


Entfernt alle Lesezeichen aus dieser Sammlung und aus dem Dokument.

 **Examples:** 

Zeigt, wie Lesezeichen aus einem Dokument entfernt werden.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert five bookmarks with text inside their boundaries.
 for (int i = 1; i <= 5; i++) {
     String bookmarkName = "MyBookmark_" + i;

     builder.startBookmark(bookmarkName);
     builder.write(MessageFormat.format("Text inside {0}.", bookmarkName));
     builder.endBookmark(bookmarkName);
     builder.insertBreak(BreakType.PARAGRAPH_BREAK);
 }

 // This collection stores bookmarks.
 BookmarkCollection bookmarks = doc.getRange().getBookmarks();

 Assert.assertEquals(5, bookmarks.getCount());

 // There are several ways of removing bookmarks.
 // 1 -  Calling the bookmark's Remove method:
 bookmarks.get("MyBookmark_1").remove();

 Assert.assertFalse(IterableUtils.matchesAny(bookmarks, b -> b.getName() == "MyBookmark_1"));

 // 2 -  Passing the bookmark to the collection's Remove method:
 Bookmark bookmark = doc.getRange().getBookmarks().get(0);
 doc.getRange().getBookmarks().remove(bookmark);

 Assert.assertFalse(IterableUtils.matchesAny(bookmarks, b -> b.getName() == "MyBookmark_2"));

 // 3 -  Removing a bookmark from the collection by name:
 doc.getRange().getBookmarks().remove("MyBookmark_3");

 Assert.assertFalse(IterableUtils.matchesAny(bookmarks, b -> b.getName() == "MyBookmark_3"));

 // 4 -  Removing a bookmark at an index in the bookmark collection:
 doc.getRange().getBookmarks().removeAt(0);

 Assert.assertFalse(IterableUtils.matchesAny(bookmarks, b -> b.getName() == "MyBookmark_4"));

 // We can clear the entire bookmark collection.
 bookmarks.clear();

 // The text that was inside the bookmarks is still present in the document.
 Assert.assertEquals(bookmarks.getCount(), 0);
 Assert.assertEquals("Text inside MyBookmark_1.\r" +
         "Text inside MyBookmark_2.\r" +
         "Text inside MyBookmark_3.\r" +
         "Text inside MyBookmark_4.\r" +
         "Text inside MyBookmark_5.", doc.getText().trim());
 
```

### get(int index) {#get-int}
```
public Bookmark get(int index)
```


Gibt ein Lesezeichen am angegebenen Index zurück.

 **Remarks:** 

Der Index ist nullbasiert.

Negative Indizes sind zulässig und bedeuten Zugriff vom Ende der Sammlung. Zum Beispiel bedeutet -1 das letzte Element, -2 das vorletzte und so weiter.

Wenn der Index größer oder gleich der Anzahl der Elemente in der Liste ist, gibt dies eine Nullreferenz zurück.

Wenn der Index negativ ist und sein absoluter Wert größer als die Anzahl der Elemente in der Liste ist, gibt dies eine Nullreferenz zurück.

 **Examples:** 

Zeigt, wie man Lesezeichen hinzufügt und deren Inhalte aktualisiert.

```

 public void createUpdateAndPrintBookmarks() throws Exception {
     // Create a document with three bookmarks, then use a custom document visitor implementation to print their contents.
     Document doc = createDocumentWithBookmarks(3);
     BookmarkCollection bookmarks = doc.getRange().getBookmarks();
     printAllBookmarkInfo(bookmarks);

     // Bookmarks can be accessed in the bookmark collection by index or name, and their names can be updated.
     bookmarks.get(0).setName("{bookmarks[0].Name}_NewName");
     bookmarks.get("MyBookmark_2").setText("Updated text contents of {bookmarks[1].Name}");

     // Print all bookmarks again to see updated values.
     printAllBookmarkInfo(bookmarks);
 }

 /// 
 /// Create a document with a given number of bookmarks.
 /// 
 private static Document createDocumentWithBookmarks(int numberOfBookmarks) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     for (int i = 1; i <= numberOfBookmarks; i++) {
         String bookmarkName = "MyBookmark_" + i;

         builder.write("Text before bookmark.");
         builder.startBookmark(bookmarkName);
         builder.write(MessageFormat.format("Text inside {0}.", bookmarkName));
         builder.endBookmark(bookmarkName);
         builder.writeln("Text after bookmark.");
     }

     return doc;
 }

 /// 
 /// Use an iterator and a visitor to print info of every bookmark in the collection.
 /// 
 private static void printAllBookmarkInfo(BookmarkCollection bookmarks) throws Exception {
     BookmarkInfoPrinter bookmarkVisitor = new BookmarkInfoPrinter();

     // Get each bookmark in the collection to accept a visitor that will print its contents.
     Iterator enumerator = bookmarks.iterator();

     while (enumerator.hasNext()) {
         Bookmark currentBookmark = enumerator.next();

         if (currentBookmark != null) {
             currentBookmark.getBookmarkStart().accept(bookmarkVisitor);
             currentBookmark.getBookmarkEnd().accept(bookmarkVisitor);

             System.out.println(currentBookmark.getBookmarkStart().getText());
         }
     }
 }

 /// 
 /// Prints contents of every visited bookmark to the console.
 /// 
 public static class BookmarkInfoPrinter extends DocumentVisitor {
     public int visitBookmarkStart(BookmarkStart bookmarkStart) throws Exception {
         System.out.println(MessageFormat.format("BookmarkStart name: \"{0}\", Content: \"{1}\"", bookmarkStart.getName(),
                 bookmarkStart.getBookmark().getText()));
         return VisitorAction.CONTINUE;
     }

     public int visitBookmarkEnd(BookmarkEnd bookmarkEnd) {
         System.out.println(MessageFormat.format("BookmarkEnd name: \"{0}\"", bookmarkEnd.getName()));
         return VisitorAction.CONTINUE;
     }
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Ein Index in die Sammlung. |

**Returns:**
[Bookmark](../../com.aspose.words/bookmark/) - A bookmark at the specified index.
### get(String bookmarkName) {#get-java.lang.String}
```
public Bookmark get(String bookmarkName)
```


Gibt ein Lesezeichen nach Namen zurück.

 **Remarks:** 

Gibt  null  zurück, wenn das Lesezeichen mit dem angegebenen Namen nicht gefunden werden kann.

 **Examples:** 

Zeigt, wie man Lesezeichen hinzufügt und deren Inhalte aktualisiert.

```

 public void createUpdateAndPrintBookmarks() throws Exception {
     // Create a document with three bookmarks, then use a custom document visitor implementation to print their contents.
     Document doc = createDocumentWithBookmarks(3);
     BookmarkCollection bookmarks = doc.getRange().getBookmarks();
     printAllBookmarkInfo(bookmarks);

     // Bookmarks can be accessed in the bookmark collection by index or name, and their names can be updated.
     bookmarks.get(0).setName("{bookmarks[0].Name}_NewName");
     bookmarks.get("MyBookmark_2").setText("Updated text contents of {bookmarks[1].Name}");

     // Print all bookmarks again to see updated values.
     printAllBookmarkInfo(bookmarks);
 }

 /// 
 /// Create a document with a given number of bookmarks.
 /// 
 private static Document createDocumentWithBookmarks(int numberOfBookmarks) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     for (int i = 1; i <= numberOfBookmarks; i++) {
         String bookmarkName = "MyBookmark_" + i;

         builder.write("Text before bookmark.");
         builder.startBookmark(bookmarkName);
         builder.write(MessageFormat.format("Text inside {0}.", bookmarkName));
         builder.endBookmark(bookmarkName);
         builder.writeln("Text after bookmark.");
     }

     return doc;
 }

 /// 
 /// Use an iterator and a visitor to print info of every bookmark in the collection.
 /// 
 private static void printAllBookmarkInfo(BookmarkCollection bookmarks) throws Exception {
     BookmarkInfoPrinter bookmarkVisitor = new BookmarkInfoPrinter();

     // Get each bookmark in the collection to accept a visitor that will print its contents.
     Iterator enumerator = bookmarks.iterator();

     while (enumerator.hasNext()) {
         Bookmark currentBookmark = enumerator.next();

         if (currentBookmark != null) {
             currentBookmark.getBookmarkStart().accept(bookmarkVisitor);
             currentBookmark.getBookmarkEnd().accept(bookmarkVisitor);

             System.out.println(currentBookmark.getBookmarkStart().getText());
         }
     }
 }

 /// 
 /// Prints contents of every visited bookmark to the console.
 /// 
 public static class BookmarkInfoPrinter extends DocumentVisitor {
     public int visitBookmarkStart(BookmarkStart bookmarkStart) throws Exception {
         System.out.println(MessageFormat.format("BookmarkStart name: \"{0}\", Content: \"{1}\"", bookmarkStart.getName(),
                 bookmarkStart.getBookmark().getText()));
         return VisitorAction.CONTINUE;
     }

     public int visitBookmarkEnd(BookmarkEnd bookmarkEnd) {
         System.out.println(MessageFormat.format("BookmarkEnd name: \"{0}\"", bookmarkEnd.getName()));
         return VisitorAction.CONTINUE;
     }
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| bookmarkName | java.lang.String | Nicht groß-/kleinschreibungssensitiver Name des Lesezeichens. |

**Returns:**
[Bookmark](../../com.aspose.words/bookmark/) - A bookmark by name.
### getCount() {#getCount}
```
public int getCount()
```


Gibt die Anzahl der Lesezeichen in der Sammlung zurück.

 **Examples:** 

Zeigt, wie Lesezeichen aus einem Dokument entfernt werden.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert five bookmarks with text inside their boundaries.
 for (int i = 1; i <= 5; i++) {
     String bookmarkName = "MyBookmark_" + i;

     builder.startBookmark(bookmarkName);
     builder.write(MessageFormat.format("Text inside {0}.", bookmarkName));
     builder.endBookmark(bookmarkName);
     builder.insertBreak(BreakType.PARAGRAPH_BREAK);
 }

 // This collection stores bookmarks.
 BookmarkCollection bookmarks = doc.getRange().getBookmarks();

 Assert.assertEquals(5, bookmarks.getCount());

 // There are several ways of removing bookmarks.
 // 1 -  Calling the bookmark's Remove method:
 bookmarks.get("MyBookmark_1").remove();

 Assert.assertFalse(IterableUtils.matchesAny(bookmarks, b -> b.getName() == "MyBookmark_1"));

 // 2 -  Passing the bookmark to the collection's Remove method:
 Bookmark bookmark = doc.getRange().getBookmarks().get(0);
 doc.getRange().getBookmarks().remove(bookmark);

 Assert.assertFalse(IterableUtils.matchesAny(bookmarks, b -> b.getName() == "MyBookmark_2"));

 // 3 -  Removing a bookmark from the collection by name:
 doc.getRange().getBookmarks().remove("MyBookmark_3");

 Assert.assertFalse(IterableUtils.matchesAny(bookmarks, b -> b.getName() == "MyBookmark_3"));

 // 4 -  Removing a bookmark at an index in the bookmark collection:
 doc.getRange().getBookmarks().removeAt(0);

 Assert.assertFalse(IterableUtils.matchesAny(bookmarks, b -> b.getName() == "MyBookmark_4"));

 // We can clear the entire bookmark collection.
 bookmarks.clear();

 // The text that was inside the bookmarks is still present in the document.
 Assert.assertEquals(bookmarks.getCount(), 0);
 Assert.assertEquals("Text inside MyBookmark_1.\r" +
         "Text inside MyBookmark_2.\r" +
         "Text inside MyBookmark_3.\r" +
         "Text inside MyBookmark_4.\r" +
         "Text inside MyBookmark_5.", doc.getText().trim());
 
```

**Returns:**
int - Die Anzahl der Lesezeichen in der Sammlung.
### iterator() {#iterator}
```
public Iterator iterator()
```


Gibt ein Enumerator‑Objekt zurück.

 **Examples:** 

Zeigt, wie man Lesezeichen hinzufügt und deren Inhalte aktualisiert.

```

 public void createUpdateAndPrintBookmarks() throws Exception {
     // Create a document with three bookmarks, then use a custom document visitor implementation to print their contents.
     Document doc = createDocumentWithBookmarks(3);
     BookmarkCollection bookmarks = doc.getRange().getBookmarks();
     printAllBookmarkInfo(bookmarks);

     // Bookmarks can be accessed in the bookmark collection by index or name, and their names can be updated.
     bookmarks.get(0).setName("{bookmarks[0].Name}_NewName");
     bookmarks.get("MyBookmark_2").setText("Updated text contents of {bookmarks[1].Name}");

     // Print all bookmarks again to see updated values.
     printAllBookmarkInfo(bookmarks);
 }

 /// 
 /// Create a document with a given number of bookmarks.
 /// 
 private static Document createDocumentWithBookmarks(int numberOfBookmarks) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     for (int i = 1; i <= numberOfBookmarks; i++) {
         String bookmarkName = "MyBookmark_" + i;

         builder.write("Text before bookmark.");
         builder.startBookmark(bookmarkName);
         builder.write(MessageFormat.format("Text inside {0}.", bookmarkName));
         builder.endBookmark(bookmarkName);
         builder.writeln("Text after bookmark.");
     }

     return doc;
 }

 /// 
 /// Use an iterator and a visitor to print info of every bookmark in the collection.
 /// 
 private static void printAllBookmarkInfo(BookmarkCollection bookmarks) throws Exception {
     BookmarkInfoPrinter bookmarkVisitor = new BookmarkInfoPrinter();

     // Get each bookmark in the collection to accept a visitor that will print its contents.
     Iterator enumerator = bookmarks.iterator();

     while (enumerator.hasNext()) {
         Bookmark currentBookmark = enumerator.next();

         if (currentBookmark != null) {
             currentBookmark.getBookmarkStart().accept(bookmarkVisitor);
             currentBookmark.getBookmarkEnd().accept(bookmarkVisitor);

             System.out.println(currentBookmark.getBookmarkStart().getText());
         }
     }
 }

 /// 
 /// Prints contents of every visited bookmark to the console.
 /// 
 public static class BookmarkInfoPrinter extends DocumentVisitor {
     public int visitBookmarkStart(BookmarkStart bookmarkStart) throws Exception {
         System.out.println(MessageFormat.format("BookmarkStart name: \"{0}\", Content: \"{1}\"", bookmarkStart.getName(),
                 bookmarkStart.getBookmark().getText()));
         return VisitorAction.CONTINUE;
     }

     public int visitBookmarkEnd(BookmarkEnd bookmarkEnd) {
         System.out.println(MessageFormat.format("BookmarkEnd name: \"{0}\"", bookmarkEnd.getName()));
         return VisitorAction.CONTINUE;
     }
 }
 
```

**Returns:**
java.util.Iterator
### remove(Bookmark bookmark) {#remove-com.aspose.words.Bookmark}
```
public void remove(Bookmark bookmark)
```


Entfernt das angegebene Lesezeichen aus dem Dokument.

 **Examples:** 

Zeigt, wie Lesezeichen aus einem Dokument entfernt werden.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert five bookmarks with text inside their boundaries.
 for (int i = 1; i <= 5; i++) {
     String bookmarkName = "MyBookmark_" + i;

     builder.startBookmark(bookmarkName);
     builder.write(MessageFormat.format("Text inside {0}.", bookmarkName));
     builder.endBookmark(bookmarkName);
     builder.insertBreak(BreakType.PARAGRAPH_BREAK);
 }

 // This collection stores bookmarks.
 BookmarkCollection bookmarks = doc.getRange().getBookmarks();

 Assert.assertEquals(5, bookmarks.getCount());

 // There are several ways of removing bookmarks.
 // 1 -  Calling the bookmark's Remove method:
 bookmarks.get("MyBookmark_1").remove();

 Assert.assertFalse(IterableUtils.matchesAny(bookmarks, b -> b.getName() == "MyBookmark_1"));

 // 2 -  Passing the bookmark to the collection's Remove method:
 Bookmark bookmark = doc.getRange().getBookmarks().get(0);
 doc.getRange().getBookmarks().remove(bookmark);

 Assert.assertFalse(IterableUtils.matchesAny(bookmarks, b -> b.getName() == "MyBookmark_2"));

 // 3 -  Removing a bookmark from the collection by name:
 doc.getRange().getBookmarks().remove("MyBookmark_3");

 Assert.assertFalse(IterableUtils.matchesAny(bookmarks, b -> b.getName() == "MyBookmark_3"));

 // 4 -  Removing a bookmark at an index in the bookmark collection:
 doc.getRange().getBookmarks().removeAt(0);

 Assert.assertFalse(IterableUtils.matchesAny(bookmarks, b -> b.getName() == "MyBookmark_4"));

 // We can clear the entire bookmark collection.
 bookmarks.clear();

 // The text that was inside the bookmarks is still present in the document.
 Assert.assertEquals(bookmarks.getCount(), 0);
 Assert.assertEquals("Text inside MyBookmark_1.\r" +
         "Text inside MyBookmark_2.\r" +
         "Text inside MyBookmark_3.\r" +
         "Text inside MyBookmark_4.\r" +
         "Text inside MyBookmark_5.", doc.getText().trim());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| bookmark | [Bookmark](../../com.aspose.words/bookmark/) | Das zu entfernende Lesezeichen. |

### remove(String bookmarkName) {#remove-java.lang.String}
```
public void remove(String bookmarkName)
```


Entfernt ein Lesezeichen mit dem angegebenen Namen.

 **Examples:** 

Zeigt, wie Lesezeichen aus einem Dokument entfernt werden.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert five bookmarks with text inside their boundaries.
 for (int i = 1; i <= 5; i++) {
     String bookmarkName = "MyBookmark_" + i;

     builder.startBookmark(bookmarkName);
     builder.write(MessageFormat.format("Text inside {0}.", bookmarkName));
     builder.endBookmark(bookmarkName);
     builder.insertBreak(BreakType.PARAGRAPH_BREAK);
 }

 // This collection stores bookmarks.
 BookmarkCollection bookmarks = doc.getRange().getBookmarks();

 Assert.assertEquals(5, bookmarks.getCount());

 // There are several ways of removing bookmarks.
 // 1 -  Calling the bookmark's Remove method:
 bookmarks.get("MyBookmark_1").remove();

 Assert.assertFalse(IterableUtils.matchesAny(bookmarks, b -> b.getName() == "MyBookmark_1"));

 // 2 -  Passing the bookmark to the collection's Remove method:
 Bookmark bookmark = doc.getRange().getBookmarks().get(0);
 doc.getRange().getBookmarks().remove(bookmark);

 Assert.assertFalse(IterableUtils.matchesAny(bookmarks, b -> b.getName() == "MyBookmark_2"));

 // 3 -  Removing a bookmark from the collection by name:
 doc.getRange().getBookmarks().remove("MyBookmark_3");

 Assert.assertFalse(IterableUtils.matchesAny(bookmarks, b -> b.getName() == "MyBookmark_3"));

 // 4 -  Removing a bookmark at an index in the bookmark collection:
 doc.getRange().getBookmarks().removeAt(0);

 Assert.assertFalse(IterableUtils.matchesAny(bookmarks, b -> b.getName() == "MyBookmark_4"));

 // We can clear the entire bookmark collection.
 bookmarks.clear();

 // The text that was inside the bookmarks is still present in the document.
 Assert.assertEquals(bookmarks.getCount(), 0);
 Assert.assertEquals("Text inside MyBookmark_1.\r" +
         "Text inside MyBookmark_2.\r" +
         "Text inside MyBookmark_3.\r" +
         "Text inside MyBookmark_4.\r" +
         "Text inside MyBookmark_5.", doc.getText().trim());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| bookmarkName | java.lang.String | Der case-insensitive Name des zu entfernenden Lesezeichens. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Entfernt ein Lesezeichen am angegebenen Index.

 **Examples:** 

Zeigt, wie Lesezeichen aus einem Dokument entfernt werden.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert five bookmarks with text inside their boundaries.
 for (int i = 1; i <= 5; i++) {
     String bookmarkName = "MyBookmark_" + i;

     builder.startBookmark(bookmarkName);
     builder.write(MessageFormat.format("Text inside {0}.", bookmarkName));
     builder.endBookmark(bookmarkName);
     builder.insertBreak(BreakType.PARAGRAPH_BREAK);
 }

 // This collection stores bookmarks.
 BookmarkCollection bookmarks = doc.getRange().getBookmarks();

 Assert.assertEquals(5, bookmarks.getCount());

 // There are several ways of removing bookmarks.
 // 1 -  Calling the bookmark's Remove method:
 bookmarks.get("MyBookmark_1").remove();

 Assert.assertFalse(IterableUtils.matchesAny(bookmarks, b -> b.getName() == "MyBookmark_1"));

 // 2 -  Passing the bookmark to the collection's Remove method:
 Bookmark bookmark = doc.getRange().getBookmarks().get(0);
 doc.getRange().getBookmarks().remove(bookmark);

 Assert.assertFalse(IterableUtils.matchesAny(bookmarks, b -> b.getName() == "MyBookmark_2"));

 // 3 -  Removing a bookmark from the collection by name:
 doc.getRange().getBookmarks().remove("MyBookmark_3");

 Assert.assertFalse(IterableUtils.matchesAny(bookmarks, b -> b.getName() == "MyBookmark_3"));

 // 4 -  Removing a bookmark at an index in the bookmark collection:
 doc.getRange().getBookmarks().removeAt(0);

 Assert.assertFalse(IterableUtils.matchesAny(bookmarks, b -> b.getName() == "MyBookmark_4"));

 // We can clear the entire bookmark collection.
 bookmarks.clear();

 // The text that was inside the bookmarks is still present in the document.
 Assert.assertEquals(bookmarks.getCount(), 0);
 Assert.assertEquals("Text inside MyBookmark_1.\r" +
         "Text inside MyBookmark_2.\r" +
         "Text inside MyBookmark_3.\r" +
         "Text inside MyBookmark_4.\r" +
         "Text inside MyBookmark_5.", doc.getText().trim());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Der nullbasierte Index des zu entfernenden Lesezeichens. |

