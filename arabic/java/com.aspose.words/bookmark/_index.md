---
title: "Bookmark"
linktitle: "Bookmark"
second_title: "Aspose.Words لـ Java"
description: "يمثل إشارة مرجعية واحدة في Java."
type: docs
weight: 41
url: /ar/java/com.aspose.words/bookmark/
---

**Inheritance:**
java.lang.Object
```
public class Bookmark
```

يمثل علامة مرجعية واحدة.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Bookmarks ][Working with Bookmarks].

 **Remarks:** 

[Bookmark](../../com.aspose.words/bookmark/) is a "facade" object that encapsulates two nodes [getBookmarkStart()](../../com.aspose.words/bookmark/\#getBookmarkStart) and [getBookmarkEnd()](../../com.aspose.words/bookmark/\#getBookmarkEnd) in a document tree and allows to work with a bookmark as a single object.

 **Examples:** 

يوضح كيفية إضافة العلامات المرجعية وتحديث محتوياتها.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getBookmarkEnd()](#getBookmarkEnd) | يحصل على العقدة التي تمثل نهاية الإشارة المرجعية. |
| [getBookmarkStart()](#getBookmarkStart) | يحصل على العقدة التي تمثل بداية الإشارة المرجعية. |
| [getFirstColumn()](#getFirstColumn) | يحصل على الفهرس الصفري للعمود الأول من نطاق أعمدة الجدول المرتبط بالإشارة المرجعية. |
| [getLastColumn()](#getLastColumn) | يحصل على الفهرس الصفري للعمود الأخير من نطاق أعمدة الجدول المرتبط بالإشارة المرجعية. |
| [getName()](#getName) | يحصل على اسم الإشارة المرجعية. |
| [getText()](#getText) | يحصل على النص الموجود داخل الإشارة المرجعية. |
| [isColumn()](#isColumn) | يرجع  true  إذا كانت هذه الإشارة المرجعية إشارة عمود جدول. |
| [remove()](#remove) | يزيل الإشارة المرجعية من المستند. |
| [setName(String value)](#setName-java.lang.String) | يضبط اسم الإشارة المرجعية. |
| [setText(String value)](#setText-java.lang.String) | يضبط النص المحاط داخل الإشارة المرجعية. |
### getBookmarkEnd() {#getBookmarkEnd}
```
public BookmarkEnd getBookmarkEnd()
```


يحصل على العقدة التي تمثل نهاية الإشارة المرجعية.

 **Examples:** 

يوضح كيفية إضافة العلامات المرجعية وتحديث محتوياتها.

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
[BookmarkEnd](../../com.aspose.words/bookmarkend/) - The node that represents the end of the bookmark.
### getBookmarkStart() {#getBookmarkStart}
```
public BookmarkStart getBookmarkStart()
```


يحصل على العقدة التي تمثل بداية الإشارة المرجعية.

 **Examples:** 

يوضح كيفية إضافة العلامات المرجعية وتحديث محتوياتها.

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
[BookmarkStart](../../com.aspose.words/bookmarkstart/) - The node that represents the start of the bookmark.
### getFirstColumn() {#getFirstColumn}
```
public int getFirstColumn()
```


يحصل على الفهرس الصفري للعمود الأول من نطاق أعمدة الجدول المرتبط بالإشارة المرجعية.

 **Remarks:** 

يعيد **-1** إذا لم تكن هذه الإشارة المرجعية إشارة مرجعية لعمود جدول.

 **Examples:** 

يوضح كيفية الحصول على معلومات حول إشارات مرجعية لأعمدة الجداول.

```

 Document doc = new Document(getMyDir() + "Table column bookmarks.doc");
 for (Bookmark bookmark : doc.getRange().getBookmarks()) {
     // If a bookmark encloses columns of a table, it is a table column bookmark, and its IsColumn flag set to true.
     System.out.println(MessageFormat.format("Bookmark: {0}{1}", bookmark.getName(), bookmark.isColumn() ? " (Column)" : ""));
     if (bookmark.isColumn()) {
         Row row = (Row) bookmark.getBookmarkStart().getAncestor(NodeType.ROW);
         if (row != null && bookmark.getFirstColumn() < row.getCells().getCount()) {
             // Print the contents of the first and last columns enclosed by the bookmark.
             System.out.println(row.getCells().get(bookmark.getFirstColumn()).getText().trim());
             System.out.println(row.getCells().get(bookmark.getLastColumn()).getText().trim());
         }
     }
 }
 
```

**Returns:**
int - الفهرس الصفري للعمود الأول من نطاق أعمدة الجدول المرتبط بالإشارة المرجعية.
### getLastColumn() {#getLastColumn}
```
public int getLastColumn()
```


يحصل على الفهرس الصفري للعمود الأخير من نطاق أعمدة الجدول المرتبط بالإشارة المرجعية.

 **Remarks:** 

يعيد **-1** إذا لم تكن هذه الإشارة المرجعية إشارة مرجعية لعمود جدول.

 **Examples:** 

يوضح كيفية الحصول على معلومات حول إشارات مرجعية لأعمدة الجداول.

```

 Document doc = new Document(getMyDir() + "Table column bookmarks.doc");
 for (Bookmark bookmark : doc.getRange().getBookmarks()) {
     // If a bookmark encloses columns of a table, it is a table column bookmark, and its IsColumn flag set to true.
     System.out.println(MessageFormat.format("Bookmark: {0}{1}", bookmark.getName(), bookmark.isColumn() ? " (Column)" : ""));
     if (bookmark.isColumn()) {
         Row row = (Row) bookmark.getBookmarkStart().getAncestor(NodeType.ROW);
         if (row != null && bookmark.getFirstColumn() < row.getCells().getCount()) {
             // Print the contents of the first and last columns enclosed by the bookmark.
             System.out.println(row.getCells().get(bookmark.getFirstColumn()).getText().trim());
             System.out.println(row.getCells().get(bookmark.getLastColumn()).getText().trim());
         }
     }
 }
 
```

**Returns:**
int - الفهرس الصفري للعمود الأخير من نطاق أعمدة الجدول المرتبط بالإشارة المرجعية.
### getName() {#getName}
```
public String getName()
```


يحصل على اسم الإشارة المرجعية.

 **Remarks:** 

لاحظ أنه إذا قمت بتغيير اسم إشارة مرجعية إلى اسم موجود بالفعل في المستند، لن يتم إعطاء أي خطأ وسيتم حفظ الإشارة المرجعية الأولى فقط عند حفظ المستند.

 **Examples:** 

يوضح كيفية إدراج إشارة مرجعية.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A valid bookmark has a name, a BookmarkStart, and a BookmarkEnd node.
 // Any whitespace in the names of bookmarks will be converted to underscores if we open the saved document with Microsoft Word.
 // If we highlight the bookmark's name in Microsoft Word via Insert -> Links -> Bookmark, and press "Go To",
 // the cursor will jump to the text enclosed between the BookmarkStart and BookmarkEnd nodes.
 builder.startBookmark("My Bookmark");
 builder.write("Contents of MyBookmark.");
 builder.endBookmark("My Bookmark");

 // Bookmarks are stored in this collection.
 Assert.assertEquals("My Bookmark", doc.getRange().getBookmarks().get(0).getName());

 doc.save(getArtifactsDir() + "Bookmarks.Insert.docx");
 
```

يوضح كيفية إضافة العلامات المرجعية وتحديث محتوياتها.

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
java.lang.String - اسم الإشارة المرجعية.
### getText() {#getText}
```
public String getText()
```


يحصل على النص الموجود داخل الإشارة المرجعية.

 **Examples:** 

يوضح كيفية إضافة العلامات المرجعية وتحديث محتوياتها.

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
java.lang.String - النص المحاط داخل الإشارة المرجعية.
### isColumn() {#isColumn}
```
public boolean isColumn()
```


يرجع  true  إذا كانت هذه الإشارة المرجعية إشارة عمود جدول.

 **Examples:** 

يوضح كيفية الحصول على معلومات حول إشارات مرجعية لأعمدة الجداول.

```

 Document doc = new Document(getMyDir() + "Table column bookmarks.doc");
 for (Bookmark bookmark : doc.getRange().getBookmarks()) {
     // If a bookmark encloses columns of a table, it is a table column bookmark, and its IsColumn flag set to true.
     System.out.println(MessageFormat.format("Bookmark: {0}{1}", bookmark.getName(), bookmark.isColumn() ? " (Column)" : ""));
     if (bookmark.isColumn()) {
         Row row = (Row) bookmark.getBookmarkStart().getAncestor(NodeType.ROW);
         if (row != null && bookmark.getFirstColumn() < row.getCells().getCount()) {
             // Print the contents of the first and last columns enclosed by the bookmark.
             System.out.println(row.getCells().get(bookmark.getFirstColumn()).getText().trim());
             System.out.println(row.getCells().get(bookmark.getLastColumn()).getText().trim());
         }
     }
 }
 
```

**Returns:**
boolean -  true  إذا كانت هذه الإشارة المرجعية إشارة مرجعية لعمود جدول.
### remove() {#remove}
```
public void remove()
```


يزيل الإشارة المرجعية من المستند. لا يزيل النص داخل الإشارة المرجعية.

 **Examples:** 

يوضح كيفية إزالة الإشارات المرجعية من المستند.

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

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


يضبط اسم الإشارة المرجعية.

 **Remarks:** 

لاحظ أنه إذا قمت بتغيير اسم إشارة مرجعية إلى اسم موجود بالفعل في المستند، لن يتم إعطاء أي خطأ وسيتم حفظ الإشارة المرجعية الأولى فقط عند حفظ المستند.

 **Examples:** 

يوضح كيفية إدراج إشارة مرجعية.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A valid bookmark has a name, a BookmarkStart, and a BookmarkEnd node.
 // Any whitespace in the names of bookmarks will be converted to underscores if we open the saved document with Microsoft Word.
 // If we highlight the bookmark's name in Microsoft Word via Insert -> Links -> Bookmark, and press "Go To",
 // the cursor will jump to the text enclosed between the BookmarkStart and BookmarkEnd nodes.
 builder.startBookmark("My Bookmark");
 builder.write("Contents of MyBookmark.");
 builder.endBookmark("My Bookmark");

 // Bookmarks are stored in this collection.
 Assert.assertEquals("My Bookmark", doc.getRange().getBookmarks().get(0).getName());

 doc.save(getArtifactsDir() + "Bookmarks.Insert.docx");
 
```

يوضح كيفية إضافة العلامات المرجعية وتحديث محتوياتها.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | اسم الإشارة المرجعية. |

### setText(String value) {#setText-java.lang.String}
```
public void setText(String value)
```


يضبط النص المحاط داخل الإشارة المرجعية.

 **Examples:** 

يوضح كيفية إضافة العلامات المرجعية وتحديث محتوياتها.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | النص المحاط داخل الإشارة المرجعية. |

