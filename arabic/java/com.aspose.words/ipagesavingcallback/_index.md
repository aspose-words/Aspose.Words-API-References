---
title: "IPageSavingCallback"
linktitle: "IPageSavingCallback"
second_title: "Aspose.Words لـ Java"
description: "نفّذ هذه الواجهة إذا كنت تريد التحكم في طريقة حفظ Aspose.Words للصفحات المنفصلة عند حفظ المستند إلى صيغ صفحات ثابتة في Java."
type: docs
weight: 780
url: /ar/java/com.aspose.words/ipagesavingcallback/
---
```
public interface IPageSavingCallback
```

قم بتنفيذ هذه الواجهة إذا كنت تريد التحكم في طريقة حفظ Aspose.Words للصفحات المنفصلة عند حفظ مستند إلى صيغ صفحات ثابتة.

 **Examples:** 

يوضح كيفية استخدام رد نداء لحفظ المستند إلى HTML صفحة بصفحة.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [pageSaving(PageSavingArgs args)](#pageSaving-com.aspose.words.PageSavingArgs) | يُستدعى عندما يقوم Aspose.Words بحفظ صفحة منفصلة إلى صيغ صفحات ثابتة. |
### pageSaving(PageSavingArgs args) {#pageSaving-com.aspose.words.PageSavingArgs}
```
public abstract void pageSaving(PageSavingArgs args)
```


يُستدعى عندما يقوم Aspose.Words بحفظ صفحة منفصلة إلى صيغ صفحات ثابتة.

 **Examples:** 

يوضح كيفية استخدام رد نداء لحفظ المستند إلى HTML صفحة بصفحة.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| args | [PageSavingArgs](../../com.aspose.words/pagesavingargs/) |  |

