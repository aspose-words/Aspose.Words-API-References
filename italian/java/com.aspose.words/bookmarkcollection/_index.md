---
title: "BookmarkCollection"
linktitle: "BookmarkCollection"
second_title: "Aspose.Words per Java"
description: "Una raccolta di oggetti Bookmark che rappresentano i segnalibri nell'intervallo specificato in Java."
type: docs
weight: 42
url: /it/java/com.aspose.words/bookmarkcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class BookmarkCollection implements Iterable
```

Una raccolta di oggetti [Bookmark](../../com.aspose.words/bookmark/) che rappresentano i segnalibri nell'intervallo specificato.

Per saperne di più, visita l'articolo della documentazione [ Working with Bookmarks ][Working with Bookmarks].

 **Examples:** 

Mostra come aggiungere segnalibri e aggiornare i loro contenuti.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [clear()](#clear) | Rimuove tutti i segnalibri da questa raccolta e dal documento. |
| [get(int index)](#get-int) | Restituisce un segnalibro all'indice specificato. |
| [get(String bookmarkName)](#get-java.lang.String) | Restituisce un segnalibro per nome. |
| [getCount()](#getCount) | Restituisce il numero di segnalibri nella collezione. |
| [iterator()](#iterator) | Restituisce un oggetto enumeratore. |
| [remove(Bookmark bookmark)](#remove-com.aspose.words.Bookmark) | Rimuove il segnalibro specificato dal documento. |
| [remove(String bookmarkName)](#remove-java.lang.String) | Rimuove un segnalibro con il nome specificato. |
| [removeAt(int index)](#removeAt-int) | Rimuove un segnalibro all'indice specificato. |
### clear() {#clear}
```
public void clear()
```


Rimuove tutti i segnalibri da questa raccolta e dal documento.

 **Examples:** 

Mostra come rimuovere i segnalibri da un documento.

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


Restituisce un segnalibro all'indice specificato.

 **Remarks:** 

L'indice è basato su zero.

Gli indici negativi sono consentiti e indicano l'accesso dalla fine della collezione. Per esempio, -1 indica l'ultimo elemento, -2 indica il penultimo e così via.

Se l'indice è maggiore o uguale al numero di elementi nella lista, questo restituisce un riferimento nullo.

Se l'indice è negativo e il suo valore assoluto è maggiore del numero di elementi nella lista, questo restituisce un riferimento nullo.

 **Examples:** 

Mostra come aggiungere segnalibri e aggiornare i loro contenuti.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | Un indice nella collezione. |

**Returns:**
[Bookmark](../../com.aspose.words/bookmark/) - A bookmark at the specified index.
### get(String bookmarkName) {#get-java.lang.String}
```
public Bookmark get(String bookmarkName)
```


Restituisce un segnalibro per nome.

 **Remarks:** 

Restituisce  null  se il segnalibro con il nome specificato non può essere trovato.

 **Examples:** 

Mostra come aggiungere segnalibri e aggiornare i loro contenuti.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| bookmarkName | java.lang.String | Nome non sensibile al maiuscolo/minuscolo del segnalibro. |

**Returns:**
[Bookmark](../../com.aspose.words/bookmark/) - A bookmark by name.
### getCount() {#getCount}
```
public int getCount()
```


Restituisce il numero di segnalibri nella collezione.

 **Examples:** 

Mostra come rimuovere i segnalibri da un documento.

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
int - Il numero di segnalibri nella collezione.
### iterator() {#iterator}
```
public Iterator iterator()
```


Restituisce un oggetto enumeratore.

 **Examples:** 

Mostra come aggiungere segnalibri e aggiornare i loro contenuti.

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


Rimuove il segnalibro specificato dal documento.

 **Examples:** 

Mostra come rimuovere i segnalibri da un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| bookmark | [Bookmark](../../com.aspose.words/bookmark/) | Il segnalibro da rimuovere. |

### remove(String bookmarkName) {#remove-java.lang.String}
```
public void remove(String bookmarkName)
```


Rimuove un segnalibro con il nome specificato.

 **Examples:** 

Mostra come rimuovere i segnalibri da un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| bookmarkName | java.lang.String | Il nome non sensibile a maiuscole/minuscole del segnalibro da rimuovere. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Rimuove un segnalibro all'indice specificato.

 **Examples:** 

Mostra come rimuovere i segnalibri da un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | L'indice basato su zero del segnalibro da rimuovere. |

