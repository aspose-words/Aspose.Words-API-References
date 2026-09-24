---
title: "PageLayoutEvent"
linktitle: "PageLayoutEvent"
second_title: "Aspose.Words Java için"
description: "Java'da sayfa düzeni modeli oluşturulması ve işlenmesi sırasında tetiklenen bir olay kodu."
type: docs
weight: 515
url: /tr/java/com.aspose.words/pagelayoutevent/
---

**Inheritance:**
java.lang.Object
```
public class PageLayoutEvent
```

Sayfa düzeni modeli oluşturulması ve renderleme sırasında yükseltilen bir olay kodu.

Sayfa düzeni modeli iki adımda oluşturulur. İlk olarak, "dönüştürme adımı", bu aşamada sayfa düzeni belge içeriğini alır ve nesne grafiği oluşturur. İkinci olarak, "yeniden akış adımı", bu aşamada yapılar bölünür, birleştirilir ve sayfalara düzenlenir.

Oluşturmayı tetikleyen işleme bağlı olarak, sayfa düzeni modeli sabit sayfa formatına daha fazla işlenebilir ya da işlenmeyebilir. Örneğin, belgede sayfa sayısını hesaplamak veya alanları güncellemek işleme gerek duymaz, ancak PDF'ye dışa aktarma gerektirir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [BUILD_FINISHED](#BUILD-FINISHED) | Sayfa düzeni oluşturulması tamamlandı. |
| [BUILD_STARTED](#BUILD-STARTED) | Sayfa düzeni oluşturulması başladı. |
| [CONVERSION_FINISHED](#CONVERSION-FINISHED) | Belge modelinin sayfa düzenine dönüştürülmesi tamamlandı. |
| [CONVERSION_STARTED](#CONVERSION-STARTED) | Belge modelinin sayfa düzenine dönüştürülmesi başladı. |
| [NONE](#NONE) | Varsayılan değer |
| [PART_REFLOW_FINISHED](#PART-REFLOW-FINISHED) | Sayfanın yeniden akışı tamamlandı. |
| [PART_REFLOW_STARTED](#PART-REFLOW-STARTED) | Sayfanın yeniden akışı başladı. |
| [PART_RENDERING_FINISHED](#PART-RENDERING-FINISHED) | Sayfanın işlenmesi tamamlandı. |
| [PART_RENDERING_STARTED](#PART-RENDERING-STARTED) | Sayfanın işlenmesi başladı. |
| [REFLOW_FINISHED](#REFLOW-FINISHED) | Sayfa düzeninin yeniden akışı tamamlandı. |
| [REFLOW_STARTED](#REFLOW-STARTED) | Sayfa düzeninin yeniden akışı başladı. |
| [WATCH_DOG](#WATCH-DOG) | Kod içinde sıkça ziyaret edilen ve işlemi iptal etmek için uygun bir kontrol noktasına karşılık gelir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String pageLayoutEventName)](#fromName-java.lang.String) |  |
| [getName(int pageLayoutEvent)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pageLayoutEvent)](#toString-int) |  |
### BUILD_FINISHED {#BUILD-FINISHED}
```
public static int BUILD_FINISHED
```


Sayfa düzeninin oluşturulması tamamlandı. Bir kez tetiklenir. Bu, [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout) çağrıldığında gerçekleşen son olaydır.

### BUILD_STARTED {#BUILD-STARTED}
```
public static int BUILD_STARTED
```


Sayfa düzeninin oluşturulması başladı. Bir kez tetiklenir. Bu, [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout) çağrıldığında gerçekleşen ilk olaydır.

### CONVERSION_FINISHED {#CONVERSION-FINISHED}
```
public static int CONVERSION_FINISHED
```


Belge modelinin sayfa düzenine dönüştürülmesi tamamlandı. Bir kez tetiklenir. Bu, düzen modelinin belge içeriğini çekmeyi durdurduğu zaman gerçekleşir.

### CONVERSION_STARTED {#CONVERSION-STARTED}
```
public static int CONVERSION_STARTED
```


Belge modelinin sayfa düzenine dönüştürülmesi başladı. Bir kez tetiklenir. Bu, düzen modelinin belge içeriğini çekmeye başladığı zaman gerçekleşir.

### NONE {#NONE}
```
public static int NONE
```


Varsayılan değer

### PART_REFLOW_FINISHED {#PART-REFLOW-FINISHED}
```
public static int PART_REFLOW_FINISHED
```


Sayfanın yeniden akışı tamamlandı. Sayfanın birden fazla kez yeniden akabileceğini ve akışın tamamlanmadan yeniden başlayabileceğini unutmayın.

### PART_REFLOW_STARTED {#PART-REFLOW-STARTED}
```
public static int PART_REFLOW_STARTED
```


Sayfanın yeniden akışı başladı. Sayfanın birden fazla kez yeniden akabileceğini ve akışın tamamlanmadan yeniden başlayabileceğini unutmayın.

### PART_RENDERING_FINISHED {#PART-RENDERING-FINISHED}
```
public static int PART_RENDERING_FINISHED
```


Sayfanın işlenmesi tamamlandı. Bu, sayfa başına bir kez tetiklenir.

### PART_RENDERING_STARTED {#PART-RENDERING-STARTED}
```
public static int PART_RENDERING_STARTED
```


Sayfanın işlenmesi başladı. Bu, sayfa başına bir kez tetiklenir.

### REFLOW_FINISHED {#REFLOW-FINISHED}
```
public static int REFLOW_FINISHED
```


Sayfa düzeninin yeniden akışı tamamlandı. Bir kez tetiklenir. Bu, düzen modelinin belge içeriğinin yeniden akışını durdurduğu zaman gerçekleşir.

### REFLOW_STARTED {#REFLOW-STARTED}
```
public static int REFLOW_STARTED
```


Sayfa düzeninin yeniden akışı başladı. Bir kez tetiklenir. Bu, düzen modelinin belge içeriğinin yeniden akışına başladığı zaman gerçekleşir.

### WATCH_DOG {#WATCH-DOG}
```
public static int WATCH_DOG
```


Kod içinde sıkça ziyaret edilen ve işlemi iptal etmek için uygun bir kontrol noktasına karşılık gelir.

İçinde [IPageLayoutCallback.notify(com.aspose.words.PageLayoutCallbackArgs)](../../com.aspose.words/ipagelayoutcallback/\#notify-com.aspose.words.PageLayoutCallbackArgs) iken işlemi iptal etmek için özel bir istisna fırlatın.

Herhangi bir geri çağırma olayını işlerken işlemi iptal etmek için fırlatabilirsiniz.

İşlem iptal edilirse sayfa düzeni modelinin tanımsız bir durumda kalacağını unutmayın. Ancak, işlem tam bir sayfanın yeniden akışı sırasında iptal edilirse, o sayfanın sonuna kadar düzen modelini kullanmak mümkün olmalıdır.

### length {#length}
```
public static int length
```


### fromName(String pageLayoutEventName) {#fromName-java.lang.String}
```
public static int fromName(String pageLayoutEventName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pageLayoutEventName | java.lang.String |  |

**Returns:**
int
### getName(int pageLayoutEvent) {#getName-int}
```
public static String getName(int pageLayoutEvent)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pageLayoutEvent | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pageLayoutEvent) {#toString-int}
```
public static String toString(int pageLayoutEvent)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pageLayoutEvent | int |  |

**Returns:**
java.lang.String
