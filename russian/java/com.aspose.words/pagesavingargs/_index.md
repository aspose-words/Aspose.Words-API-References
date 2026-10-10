---
title: "PageSavingArgs"
linktitle: "PageSavingArgs"
second_title: "Aspose.Words для Java"
description: "Предоставляет данные для события IPageSavingCallback.pageSavingcom.aspose.words.PageSavingArgs в Java."
type: docs
weight: 517
url: /ru/java/com.aspose.words/pagesavingargs/
---

**Inheritance:**
java.lang.Object
```
public class PageSavingArgs
```

Предоставляет данные для события [IPageSavingCallback.pageSaving(com.aspose.words.PageSavingArgs)](../../com.aspose.words/ipagesavingcallback/\#pageSaving-com.aspose.words.PageSavingArgs).

Чтобы узнать больше, посетите статью документации [ Programming with Documents ][Programming with Documents].

 **Examples:** 

Показывает, как использовать обратный вызов для сохранения документа в HTML постранично.

```

 public void pageFileNames() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.writeln("Page 1.");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 2.");
     builder.insertImage(getImageDir() + "Logo.jpg");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 3.");

     // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we convert the document to HTML.
     HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

     // We will save each page in this document to a separate HTML file in the local file system.
     // Set a callback that allows us to name each output HTML document.
     htmlFixedSaveOptions.setPageSavingCallback(new CustomFileNamePageSavingCallback());

     doc.save(getArtifactsDir() + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

     String[] filePaths = DocumentHelper.directoryGetFiles(getArtifactsDir(), "SavingCallback.PageFileNames.Page_*").toArray(new String[0]);

     Assert.assertEquals(3, filePaths.length);
 }

 /// 
 /// Saves all pages to a file and directory specified within.
 /// 
 private static class CustomFileNamePageSavingCallback implements IPageSavingCallback {
     public void pageSaving(PageSavingArgs args) throws Exception {
         String outFileName = MessageFormat.format("{0}SavingCallback.PageFileNames.Page_{1}.html", getArtifactsDir(), args.getPageIndex());

         // Below are two ways of specifying where Aspose.Words will save each page of the document.
         // 1 -  Set a filename for the output page file:
         args.setPageFileName(outFileName);

         // 2 -  Create a custom stream for the output page file:
         try (FileOutputStream outputStream = new FileOutputStream(outFileName)) {
             args.setPageStream(outputStream);
         }

         Assert.assertFalse(args.getKeepPageStreamOpen());
     }
 }
 
```


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Методы

| Метод | Описание |
| --- | --- |
| [getKeepPageStreamOpen()](#getKeepPageStreamOpen) | Указывает, должен ли Aspose.Words оставлять поток открытым или закрывать его после сохранения страницы документа. |
| [getPageFileName()](#getPageFileName) | Получает имя файла, в который будет сохранена страница документа. |
| [getPageIndex()](#getPageIndex) | Текущий индекс страницы. |
| [getPageStream()](#getPageStream) |  |
| [setKeepPageStreamOpen(boolean value)](#setKeepPageStreamOpen-boolean) | Указывает, должен ли Aspose.Words оставлять поток открытым или закрывать его после сохранения страницы документа. |
| [setPageFileName(String value)](#setPageFileName-java.lang.String) | Устанавливает имя файла, в который будет сохранена страница документа. |
| [setPageStream(OutputStream value)](#setPageStream-java.io.OutputStream) |  |
### getKeepPageStreamOpen() {#getKeepPageStreamOpen}
```
public boolean getKeepPageStreamOpen()
```


Указывает, должен ли Aspose.Words оставлять поток открытым или закрывать его после сохранения страницы документа.

 **Remarks:** 

По умолчанию значение  false , и Aspose.Words закроет поток, предоставленный в свойстве **P:Aspose.Words.Saving.PageSavingArgs.PageStream**, после записи в него страницы документа. Укажите  true , чтобы оставить поток открытым.

 **Examples:** 

Показывает, как использовать обратный вызов для сохранения документа в HTML постранично.

```

 public void pageFileNames() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.writeln("Page 1.");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 2.");
     builder.insertImage(getImageDir() + "Logo.jpg");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 3.");

     // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we convert the document to HTML.
     HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

     // We will save each page in this document to a separate HTML file in the local file system.
     // Set a callback that allows us to name each output HTML document.
     htmlFixedSaveOptions.setPageSavingCallback(new CustomFileNamePageSavingCallback());

     doc.save(getArtifactsDir() + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

     String[] filePaths = DocumentHelper.directoryGetFiles(getArtifactsDir(), "SavingCallback.PageFileNames.Page_*").toArray(new String[0]);

     Assert.assertEquals(3, filePaths.length);
 }

 /// 
 /// Saves all pages to a file and directory specified within.
 /// 
 private static class CustomFileNamePageSavingCallback implements IPageSavingCallback {
     public void pageSaving(PageSavingArgs args) throws Exception {
         String outFileName = MessageFormat.format("{0}SavingCallback.PageFileNames.Page_{1}.html", getArtifactsDir(), args.getPageIndex());

         // Below are two ways of specifying where Aspose.Words will save each page of the document.
         // 1 -  Set a filename for the output page file:
         args.setPageFileName(outFileName);

         // 2 -  Create a custom stream for the output page file:
         try (FileOutputStream outputStream = new FileOutputStream(outFileName)) {
             args.setPageStream(outputStream);
         }

         Assert.assertFalse(args.getKeepPageStreamOpen());
     }
 }
 
```

**P:Aspose.Words.Saving.PageSavingArgs.PageStream**

**Returns:**
boolean - Соответствующее  boolean  значение.
### getPageFileName() {#getPageFileName}
```
public String getPageFileName()
```


Получает имя файла, в который будет сохранена страница документа.

 **Remarks:** 

Если не указано, имя файла и путь страницы будут сгенерированы автоматически на основе оригинального имени файла.

 **Examples:** 

Показывает, как использовать обратный вызов для сохранения документа в HTML постранично.

```

 public void pageFileNames() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.writeln("Page 1.");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 2.");
     builder.insertImage(getImageDir() + "Logo.jpg");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 3.");

     // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we convert the document to HTML.
     HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

     // We will save each page in this document to a separate HTML file in the local file system.
     // Set a callback that allows us to name each output HTML document.
     htmlFixedSaveOptions.setPageSavingCallback(new CustomFileNamePageSavingCallback());

     doc.save(getArtifactsDir() + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

     String[] filePaths = DocumentHelper.directoryGetFiles(getArtifactsDir(), "SavingCallback.PageFileNames.Page_*").toArray(new String[0]);

     Assert.assertEquals(3, filePaths.length);
 }

 /// 
 /// Saves all pages to a file and directory specified within.
 /// 
 private static class CustomFileNamePageSavingCallback implements IPageSavingCallback {
     public void pageSaving(PageSavingArgs args) throws Exception {
         String outFileName = MessageFormat.format("{0}SavingCallback.PageFileNames.Page_{1}.html", getArtifactsDir(), args.getPageIndex());

         // Below are two ways of specifying where Aspose.Words will save each page of the document.
         // 1 -  Set a filename for the output page file:
         args.setPageFileName(outFileName);

         // 2 -  Create a custom stream for the output page file:
         try (FileOutputStream outputStream = new FileOutputStream(outFileName)) {
             args.setPageStream(outputStream);
         }

         Assert.assertFalse(args.getKeepPageStreamOpen());
     }
 }
 
```

**Returns:**
java.lang.String - Имя файла, в который будет сохранена страница документа.
### getPageIndex() {#getPageIndex}
```
public int getPageIndex()
```


Текущий индекс страницы.

 **Examples:** 

Показывает, как использовать обратный вызов для сохранения документа в HTML постранично.

```

 public void pageFileNames() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.writeln("Page 1.");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 2.");
     builder.insertImage(getImageDir() + "Logo.jpg");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 3.");

     // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we convert the document to HTML.
     HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

     // We will save each page in this document to a separate HTML file in the local file system.
     // Set a callback that allows us to name each output HTML document.
     htmlFixedSaveOptions.setPageSavingCallback(new CustomFileNamePageSavingCallback());

     doc.save(getArtifactsDir() + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

     String[] filePaths = DocumentHelper.directoryGetFiles(getArtifactsDir(), "SavingCallback.PageFileNames.Page_*").toArray(new String[0]);

     Assert.assertEquals(3, filePaths.length);
 }

 /// 
 /// Saves all pages to a file and directory specified within.
 /// 
 private static class CustomFileNamePageSavingCallback implements IPageSavingCallback {
     public void pageSaving(PageSavingArgs args) throws Exception {
         String outFileName = MessageFormat.format("{0}SavingCallback.PageFileNames.Page_{1}.html", getArtifactsDir(), args.getPageIndex());

         // Below are two ways of specifying where Aspose.Words will save each page of the document.
         // 1 -  Set a filename for the output page file:
         args.setPageFileName(outFileName);

         // 2 -  Create a custom stream for the output page file:
         try (FileOutputStream outputStream = new FileOutputStream(outFileName)) {
             args.setPageStream(outputStream);
         }

         Assert.assertFalse(args.getKeepPageStreamOpen());
     }
 }
 
```

**Returns:**
int — соответствующее значение  int .
### getPageStream() {#getPageStream}
```
public OutputStream getPageStream()
```




**Returns:**
java.io.OutputStream
### setKeepPageStreamOpen(boolean value) {#setKeepPageStreamOpen-boolean}
```
public void setKeepPageStreamOpen(boolean value)
```


Указывает, должен ли Aspose.Words оставлять поток открытым или закрывать его после сохранения страницы документа.

 **Remarks:** 

По умолчанию значение  false , и Aspose.Words закроет поток, предоставленный в свойстве **P:Aspose.Words.Saving.PageSavingArgs.PageStream**, после записи в него страницы документа. Укажите  true , чтобы оставить поток открытым.

 **Examples:** 

Показывает, как использовать обратный вызов для сохранения документа в HTML постранично.

```

 public void pageFileNames() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.writeln("Page 1.");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 2.");
     builder.insertImage(getImageDir() + "Logo.jpg");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 3.");

     // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we convert the document to HTML.
     HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

     // We will save each page in this document to a separate HTML file in the local file system.
     // Set a callback that allows us to name each output HTML document.
     htmlFixedSaveOptions.setPageSavingCallback(new CustomFileNamePageSavingCallback());

     doc.save(getArtifactsDir() + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

     String[] filePaths = DocumentHelper.directoryGetFiles(getArtifactsDir(), "SavingCallback.PageFileNames.Page_*").toArray(new String[0]);

     Assert.assertEquals(3, filePaths.length);
 }

 /// 
 /// Saves all pages to a file and directory specified within.
 /// 
 private static class CustomFileNamePageSavingCallback implements IPageSavingCallback {
     public void pageSaving(PageSavingArgs args) throws Exception {
         String outFileName = MessageFormat.format("{0}SavingCallback.PageFileNames.Page_{1}.html", getArtifactsDir(), args.getPageIndex());

         // Below are two ways of specifying where Aspose.Words will save each page of the document.
         // 1 -  Set a filename for the output page file:
         args.setPageFileName(outFileName);

         // 2 -  Create a custom stream for the output page file:
         try (FileOutputStream outputStream = new FileOutputStream(outFileName)) {
             args.setPageStream(outputStream);
         }

         Assert.assertFalse(args.getKeepPageStreamOpen());
     }
 }
 
```

**P:Aspose.Words.Saving.PageSavingArgs.PageStream**

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setPageFileName(String value) {#setPageFileName-java.lang.String}
```
public void setPageFileName(String value)
```


Устанавливает имя файла, в который будет сохранена страница документа.

 **Remarks:** 

Если не указано, имя файла и путь страницы будут сгенерированы автоматически на основе оригинального имени файла.

 **Examples:** 

Показывает, как использовать обратный вызов для сохранения документа в HTML постранично.

```

 public void pageFileNames() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.writeln("Page 1.");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 2.");
     builder.insertImage(getImageDir() + "Logo.jpg");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 3.");

     // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we convert the document to HTML.
     HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

     // We will save each page in this document to a separate HTML file in the local file system.
     // Set a callback that allows us to name each output HTML document.
     htmlFixedSaveOptions.setPageSavingCallback(new CustomFileNamePageSavingCallback());

     doc.save(getArtifactsDir() + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

     String[] filePaths = DocumentHelper.directoryGetFiles(getArtifactsDir(), "SavingCallback.PageFileNames.Page_*").toArray(new String[0]);

     Assert.assertEquals(3, filePaths.length);
 }

 /// 
 /// Saves all pages to a file and directory specified within.
 /// 
 private static class CustomFileNamePageSavingCallback implements IPageSavingCallback {
     public void pageSaving(PageSavingArgs args) throws Exception {
         String outFileName = MessageFormat.format("{0}SavingCallback.PageFileNames.Page_{1}.html", getArtifactsDir(), args.getPageIndex());

         // Below are two ways of specifying where Aspose.Words will save each page of the document.
         // 1 -  Set a filename for the output page file:
         args.setPageFileName(outFileName);

         // 2 -  Create a custom stream for the output page file:
         try (FileOutputStream outputStream = new FileOutputStream(outFileName)) {
             args.setPageStream(outputStream);
         }

         Assert.assertFalse(args.getKeepPageStreamOpen());
     }
 }
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Имя файла, в который будет сохранена страница документа. |

### setPageStream(OutputStream value) {#setPageStream-java.io.OutputStream}
```
public void setPageStream(OutputStream value)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.io.OutputStream |  |

