---
title: "IPageLayoutCallback"
linktitle: "IPageLayoutCallback"
second_title: "Aspose.Words Java için"
description: "Java'da sayfa düzeni modelinin oluşturulması ve işlenmesi sırasında çağrılan kendi özel yönteminizi sahip olmak istiyorsanız bu arayüzü uygulayın."
type: docs
weight: 779
url: /tr/java/com.aspose.words/ipagelayoutcallback/
---
```
public interface IPageLayoutCallback
```

Sayfa yerleşim modeli oluşturulurken ve işlenirken kendi özel yönteminizi çağırmak istiyorsanız bu arabirimi uygulayın.

 **Remarks:** 

Bu arayüzün temel kullanımı, uygulama kodunun oluşturma sürecini iptal etmesine izin vermektir.

Belgenin başlangıcında yalnızca birkaç sayfa için sayfa düzeni modeli oluşturmak, ardından süreci iptal edip sadece zaten oluşturulanları işlemek mümkündür.

Ancak, işleme sonuçlarının süreç tamamlanmış olsaydı her sayfa için işlenecek sonuçlarla eşleşmeyebileceğini unutmayın.

Bu teknik her belge için çalışmayabilir veya tamamen başarısız olabilir.

 **Examples:** 

Bir düzen geri çağrısı ile düzen değişikliklerini nasıl izleneceğini gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [notify(PageLayoutCallbackArgs args)](#notify-com.aspose.words.PageLayoutCallbackArgs) | Bu, düzen oluşturma ve işleme ilerlemesini bildirmek için çağrılır. |
### notify(PageLayoutCallbackArgs args) {#notify-com.aspose.words.PageLayoutCallbackArgs}
```
public abstract void notify(PageLayoutCallbackArgs args)
```


Bu, düzen oluşturma ve işleme ilerlemesini bildirmek için çağrılır.

 **Remarks:** 

Uygulama tarafından fırlatıldığında istisna, düzen oluşturma sürecini iptal eder.

 **Examples:** 

Bir düzen geri çağrısı ile düzen değişikliklerini nasıl izleneceğini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| args | [PageLayoutCallbackArgs](../../com.aspose.words/pagelayoutcallbackargs/) | Olayın bir argümanı. |

