---
title: "BookmarkCollection"
linktitle: "BookmarkCollection"
second_title: "Aspose.Words pour Java"
description: "Une collection d'objets Bookmark qui représentent les signets dans la plage spécifiée en Java."
type: docs
weight: 42
url: /fr/java/com.aspose.words/bookmarkcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class BookmarkCollection implements Iterable
```

Une collection d'objets [Bookmark](../../com.aspose.words/bookmark/) qui représentent les signets dans la plage spécifiée.

Pour en savoir plus, consultez l'article de documentation [ Working with Bookmarks ][Working with Bookmarks].

 **Examples:** 

Montre comment ajouter des signets et mettre à jour leur contenu.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [clear()](#clear) | Supprime tous les signets de cette collection et du document. |
| [get(int index)](#get-int) | Renvoie un signet à l'index spécifié. |
| [get(String bookmarkName)](#get-java.lang.String) | Renvoie un signet par son nom. |
| [getCount()](#getCount) | Renvoie le nombre de signets dans la collection. |
| [iterator()](#iterator) | Renvoie un objet énumérateur. |
| [remove(Bookmark bookmark)](#remove-com.aspose.words.Bookmark) | Supprime le signet spécifié du document. |
| [remove(String bookmarkName)](#remove-java.lang.String) | Supprime un signet avec le nom spécifié. |
| [removeAt(int index)](#removeAt-int) | Supprime un signet à l'index spécifié. |
### clear() {#clear}
```
public void clear()
```


Supprime tous les signets de cette collection et du document.

 **Examples:** 

Montre comment supprimer des signets d'un document.

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


Renvoie un signet à l'index spécifié.

 **Remarks:** 

L'index est basé sur zéro.

Les index négatifs sont autorisés et indiquent un accès depuis la fin de la collection. Par exemple, -1 signifie le dernier élément, -2 signifie l'avant-dernier et ainsi de suite.

Si l'index est supérieur ou égal au nombre d'éléments dans la liste, cela renvoie une référence nulle.

Si l'index est négatif et que sa valeur absolue est supérieure au nombre d'éléments dans la liste, cela renvoie une référence nulle.

 **Examples:** 

Montre comment ajouter des signets et mettre à jour leur contenu.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | Un index dans la collection. |

**Returns:**
[Bookmark](../../com.aspose.words/bookmark/) - A bookmark at the specified index.
### get(String bookmarkName) {#get-java.lang.String}
```
public Bookmark get(String bookmarkName)
```


Renvoie un signet par son nom.

 **Remarks:** 

Renvoie  null  si le signet avec le nom spécifié ne peut pas être trouvé.

 **Examples:** 

Montre comment ajouter des signets et mettre à jour leur contenu.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| bookmarkName | java.lang.String | Nom insensible à la casse du signet. |

**Returns:**
[Bookmark](../../com.aspose.words/bookmark/) - A bookmark by name.
### getCount() {#getCount}
```
public int getCount()
```


Renvoie le nombre de signets dans la collection.

 **Examples:** 

Montre comment supprimer des signets d'un document.

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
int - Le nombre de signets dans la collection.
### iterator() {#iterator}
```
public Iterator iterator()
```


Renvoie un objet énumérateur.

 **Examples:** 

Montre comment ajouter des signets et mettre à jour leur contenu.

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


Supprime le signet spécifié du document.

 **Examples:** 

Montre comment supprimer des signets d'un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| bookmark | [Bookmark](../../com.aspose.words/bookmark/) | Le signet à supprimer. |

### remove(String bookmarkName) {#remove-java.lang.String}
```
public void remove(String bookmarkName)
```


Supprime un signet avec le nom spécifié.

 **Examples:** 

Montre comment supprimer des signets d'un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| bookmarkName | java.lang.String | Le nom insensible à la casse du signet à supprimer. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Supprime un signet à l'index spécifié.

 **Examples:** 

Montre comment supprimer des signets d'un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | L'index basé sur zéro du signet à supprimer. |

