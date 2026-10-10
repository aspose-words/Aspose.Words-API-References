---
title: "IPageSavingCallback"
linktitle: "IPageSavingCallback"
second_title: "Aspose.Words для Java"
description: "Реализуйте этот интерфейс, если хотите контролировать, как Aspose.Words сохраняет отдельные страницы при сохранении документа в фиксированные форматы страниц в Java."
type: docs
weight: 780
url: /ru/java/com.aspose.words/ipagesavingcallback/
---
```
public interface IPageSavingCallback
```

Реализуйте этот интерфейс, если вы хотите контролировать, как Aspose.Words сохраняет отдельные страницы при сохранении документа в фиксированные форматы страниц.

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
## Методы

| Метод | Описание |
| --- | --- |
| [pageSaving(PageSavingArgs args)](#pageSaving-com.aspose.words.PageSavingArgs) | Вызывается, когда Aspose.Words сохраняет отдельную страницу в фиксированные форматы страниц. |
### pageSaving(PageSavingArgs args) {#pageSaving-com.aspose.words.PageSavingArgs}
```
public abstract void pageSaving(PageSavingArgs args)
```


Вызывается, когда Aspose.Words сохраняет отдельную страницу в фиксированные форматы страниц.

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
| args | [PageSavingArgs](../../com.aspose.words/pagesavingargs/) |  |

