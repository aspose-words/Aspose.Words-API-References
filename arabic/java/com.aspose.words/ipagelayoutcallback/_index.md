---
title: "IPageLayoutCallback"
linktitle: "IPageLayoutCallback"
second_title: "Aspose.Words لـ Java"
description: "قم بتنفيذ هذه الواجهة إذا كنت ترغب في الحصول على طريقة مخصصة خاصة بك تُستدعى أثناء بناء وعرض نموذج تخطيط الصفحة في جافا."
type: docs
weight: 779
url: /ar/java/com.aspose.words/ipagelayoutcallback/
---
```
public interface IPageLayoutCallback
```

قم بتنفيذ هذه الواجهة إذا كنت تريد استدعاء طريقتك المخصصة الخاصة أثناء بناء وعرض نموذج تخطيط الصفحة.

 **Remarks:** 

الاستخدام الأساسي لهذه الواجهة هو السماح لكود التطبيق بإلغاء عملية البناء.

يمكن بناء نموذج تخطيط الصفحة لعدد قليل فقط من الصفحات في بداية المستند ثم إلغاء العملية وعرض ما تم بناؤه بالفعل فقط.

مع ذلك، لاحظ أن نتائج العرض قد لا تتطابق مع ما كان سيُعرض لكل صفحة إذا انتهت العملية.

قد لا تعمل هذه التقنية مع كل مستند أو قد تفشل تمامًا.

 **Examples:** 

يوضح كيفية تتبع تغييرات التخطيط باستخدام layout callback.

```

 public void pageLayoutCallback() throws Exception {
     Document doc = new Document();
     doc.getBuiltInDocumentProperties().setTitle("My Document");

     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.writeln("Hello world!");

     doc.getLayoutOptions().setCallback(new RenderPageLayoutCallback());
     doc.updatePageLayout();

     doc.save(getArtifactsDir() + "Layout.PageLayoutCallback.pdf");
 }

 /// 
 /// Notifies us when we save the document to a fixed page format
 /// and renders a page that we perform a page reflow on to an image in the local file system.
 /// 
 private static class RenderPageLayoutCallback implements IPageLayoutCallback {
     public void notify(PageLayoutCallbackArgs a) throws Exception {
         switch (a.getEvent()) {
             case PageLayoutEvent.PART_REFLOW_FINISHED:
                 notifyPartFinished(a);
                 break;
             case PageLayoutEvent.CONVERSION_FINISHED:
                 notifyConversionFinished(a);
                 break;
         }
     }

     private void notifyPartFinished(PageLayoutCallbackArgs a) throws Exception {
         System.out.println(MessageFormat.format("Part at page {0} reflow.", a.getPageIndex() + 1));
         renderPage(a, a.getPageIndex());
     }

     private void notifyConversionFinished(PageLayoutCallbackArgs a) {
         System.out.println(MessageFormat.format("Document \"{0}\" converted to page format.", a.getDocument().getBuiltInDocumentProperties().getTitle()));
     }

     private void renderPage(PageLayoutCallbackArgs a, int pageIndex) throws Exception {
         ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.PNG);
         {
             saveOptions.setPageSet(new PageSet(pageIndex));
         }

         try (FileOutputStream stream = new FileOutputStream(getArtifactsDir() + MessageFormat.format("PageLayoutCallback.page-{0} {1}.png", pageIndex + 1, ++mNum))) {
             a.getDocument().save(stream, saveOptions);
         }
     }

     private int mNum;
 }
 
```
## الطرق

| طريقة | الوصف |
| --- | --- |
| [notify(PageLayoutCallbackArgs args)](#notify-com.aspose.words.PageLayoutCallbackArgs) | يتم استدعاؤه لإبلاغ عن تقدم بناء التخطيط وعرضه. |
### notify(PageLayoutCallbackArgs args) {#notify-com.aspose.words.PageLayoutCallbackArgs}
```
public abstract void notify(PageLayoutCallbackArgs args)
```


يتم استدعاؤه لإبلاغ عن تقدم بناء التخطيط وعرضه.

 **Remarks:** 

الاستثناء عند إلقائه من قبل التنفيذ يلغي عملية بناء التخطيط.

 **Examples:** 

يوضح كيفية تتبع تغييرات التخطيط باستخدام layout callback.

```

 public void pageLayoutCallback() throws Exception {
     Document doc = new Document();
     doc.getBuiltInDocumentProperties().setTitle("My Document");

     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.writeln("Hello world!");

     doc.getLayoutOptions().setCallback(new RenderPageLayoutCallback());
     doc.updatePageLayout();

     doc.save(getArtifactsDir() + "Layout.PageLayoutCallback.pdf");
 }

 /// 
 /// Notifies us when we save the document to a fixed page format
 /// and renders a page that we perform a page reflow on to an image in the local file system.
 /// 
 private static class RenderPageLayoutCallback implements IPageLayoutCallback {
     public void notify(PageLayoutCallbackArgs a) throws Exception {
         switch (a.getEvent()) {
             case PageLayoutEvent.PART_REFLOW_FINISHED:
                 notifyPartFinished(a);
                 break;
             case PageLayoutEvent.CONVERSION_FINISHED:
                 notifyConversionFinished(a);
                 break;
         }
     }

     private void notifyPartFinished(PageLayoutCallbackArgs a) throws Exception {
         System.out.println(MessageFormat.format("Part at page {0} reflow.", a.getPageIndex() + 1));
         renderPage(a, a.getPageIndex());
     }

     private void notifyConversionFinished(PageLayoutCallbackArgs a) {
         System.out.println(MessageFormat.format("Document \"{0}\" converted to page format.", a.getDocument().getBuiltInDocumentProperties().getTitle()));
     }

     private void renderPage(PageLayoutCallbackArgs a, int pageIndex) throws Exception {
         ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.PNG);
         {
             saveOptions.setPageSet(new PageSet(pageIndex));
         }

         try (FileOutputStream stream = new FileOutputStream(getArtifactsDir() + MessageFormat.format("PageLayoutCallback.page-{0} {1}.png", pageIndex + 1, ++mNum))) {
             a.getDocument().save(stream, saveOptions);
         }
     }

     private int mNum;
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| args | [PageLayoutCallbackArgs](../../com.aspose.words/pagelayoutcallbackargs/) | معامل الحدث. |

