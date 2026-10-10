---
title: "PageLayoutEvent"
linktitle: "PageLayoutEvent"
second_title: "Aspose.Words لـ Java"
description: "رمز الحدث الذي يُثار أثناء بناء نموذج تخطيط الصفحة وتصييره في Java."
type: docs
weight: 515
url: /ar/java/com.aspose.words/pagelayoutevent/
---

**Inheritance:**
java.lang.Object
```
public class PageLayoutEvent
```

رمز الحدث الذي يُثار أثناء بناء نموذج تخطيط الصفحة وتصييره.

يتم بناء نموذج تخطيط الصفحة على خطوتين. الأولى، "خطوة التحويل"، وهي عندما يقوم تخطيط الصفحة بسحب محتوى المستند وإنشاء رسم بياني للكائنات. الثانية، "خطوة إعادة التدفق"، وهي عندما تُقسم الهياكل وتُدمج وتُرتب في صفحات.

اعتمادًا على العملية التي أثارت البناء، قد يتم أو لا يتم تصيير نموذج تخطيط الصفحة إلى تنسيق صفحة ثابت. على سبيل المثال، حساب عدد الصفحات في المستند أو تحديث الحقول لا يتطلب تصييرًا، بينما تصدير إلى PDF يتطلب ذلك.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [BUILD_FINISHED](#BUILD-FINISHED) | انتهى بناء تخطيط الصفحة. |
| [BUILD_STARTED](#BUILD-STARTED) | بدأ بناء تخطيط الصفحة. |
| [CONVERSION_FINISHED](#CONVERSION-FINISHED) | انتهى تحويل نموذج المستند إلى تخطيط الصفحة. |
| [CONVERSION_STARTED](#CONVERSION-STARTED) | بدأ تحويل نموذج المستند إلى تخطيط الصفحة. |
| [NONE](#NONE) | القيمة الافتراضية |
| [PART_REFLOW_FINISHED](#PART-REFLOW-FINISHED) | انتهى إعادة تدفق الصفحة. |
| [PART_REFLOW_STARTED](#PART-REFLOW-STARTED) | بدأت إعادة تدفق الصفحة. |
| [PART_RENDERING_FINISHED](#PART-RENDERING-FINISHED) | انتهى تصيير الصفحة. |
| [PART_RENDERING_STARTED](#PART-RENDERING-STARTED) | تم بدء عرض الصفحة. |
| [REFLOW_FINISHED](#REFLOW-FINISHED) | انتهى إعادة تدفق تخطيط الصفحة. |
| [REFLOW_STARTED](#REFLOW-STARTED) | تم بدء إعادة تدفق تخطيط الصفحة. |
| [WATCH_DOG](#WATCH-DOG) | يتوافق مع نقطة تفتيش في الشيفرة يتم زيارتها غالبًا وتناسب إلغاء العملية. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String pageLayoutEventName)](#fromName-java.lang.String) |  |
| [getName(int pageLayoutEvent)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pageLayoutEvent)](#toString-int) |  |
### BUILD_FINISHED {#BUILD-FINISHED}
```
public static int BUILD_FINISHED
```


انتهى بناء تخطيط الصفحة. يُطلق مرة واحدة. هذا هو الحدث الأخير الذي يحدث عند استدعاء [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout).

### BUILD_STARTED {#BUILD-STARTED}
```
public static int BUILD_STARTED
```


تم بدء بناء تخطيط الصفحة. يُطلق مرة واحدة. هذا هو الحدث الأول الذي يحدث عند استدعاء [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout).

### CONVERSION_FINISHED {#CONVERSION-FINISHED}
```
public static int CONVERSION_FINISHED
```


انتهى تحويل نموذج المستند إلى تخطيط الصفحة. يُطلق مرة واحدة. يحدث ذلك عندما يتوقف نموذج التخطيط عن سحب محتوى المستند.

### CONVERSION_STARTED {#CONVERSION-STARTED}
```
public static int CONVERSION_STARTED
```


تم بدء تحويل نموذج المستند إلى تخطيط الصفحة. يُطلق مرة واحدة. يحدث ذلك عندما يبدأ نموذج التخطيط بسحب محتوى المستند.

### NONE {#NONE}
```
public static int NONE
```


القيمة الافتراضية

### PART_REFLOW_FINISHED {#PART-REFLOW-FINISHED}
```
public static int PART_REFLOW_FINISHED
```


انتهى إعادة تدفق الصفحة. لاحظ أن الصفحة قد تعيد التدفق عدة مرات وقد يعاد تشغيل التدفق قبل الانتهاء.

### PART_REFLOW_STARTED {#PART-REFLOW-STARTED}
```
public static int PART_REFLOW_STARTED
```


تم بدء إعادة تدفق الصفحة. لاحظ أن الصفحة قد تعيد التدفق عدة مرات وقد يعاد تشغيل التدفق قبل الانتهاء.

### PART_RENDERING_FINISHED {#PART-RENDERING-FINISHED}
```
public static int PART_RENDERING_FINISHED
```


انتهى عرض الصفحة. يُطلق هذا مرة واحدة لكل صفحة.

### PART_RENDERING_STARTED {#PART-RENDERING-STARTED}
```
public static int PART_RENDERING_STARTED
```


تم بدء عرض الصفحة. يُطلق هذا مرة واحدة لكل صفحة.

### REFLOW_FINISHED {#REFLOW-FINISHED}
```
public static int REFLOW_FINISHED
```


انتهى إعادة تدفق تخطيط الصفحة. يُطلق مرة واحدة. يحدث ذلك عندما يتوقف نموذج التخطيط عن إعادة تدفق محتوى المستند.

### REFLOW_STARTED {#REFLOW-STARTED}
```
public static int REFLOW_STARTED
```


تم بدء إعادة تدفق تخطيط الصفحة. يُطلق مرة واحدة. يحدث ذلك عندما يبدأ نموذج التخطيط في إعادة تدفق محتوى المستند.

### WATCH_DOG {#WATCH-DOG}
```
public static int WATCH_DOG
```


يتوافق مع نقطة تفتيش في الشيفرة يتم زيارتها غالبًا وتناسب إلغاء العملية.

أثناء وجودك داخل [IPageLayoutCallback.notify(com.aspose.words.PageLayoutCallbackArgs)](../../com.aspose.words/ipagelayoutcallback/\#notify-com.aspose.words.PageLayoutCallbackArgs) ارمي استثناءً مخصصًا لإلغاء العملية.

يمكنك الرمي عند معالجة أي حدث رد نداء لإلغاء العملية.

لاحظ أنه إذا تم إلغاء العملية يبقى نموذج تخطيط الصفحة في حالة غير معرفة. إذا تم إلغاء العملية أثناء إعادة تدفق صفحة كاملة، يجب أن يكون من الممكن استخدام نموذج التخطيط حتى نهاية تلك الصفحة.

### length {#length}
```
public static int length
```


### fromName(String pageLayoutEventName) {#fromName-java.lang.String}
```
public static int fromName(String pageLayoutEventName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pageLayoutEventName | java.lang.String |  |

**Returns:**
int
### getName(int pageLayoutEvent) {#getName-int}
```
public static String getName(int pageLayoutEvent)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| pageLayoutEvent | int |  |

**Returns:**
java.lang.String
