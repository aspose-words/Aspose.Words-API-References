---
title: "PageLayoutEvent"
linktitle: "PageLayoutEvent"
second_title: "Aspose.Words для Java"
description: "Код события, вызываемого во время построения модели разметки страницы и её рендеринга в Java."
type: docs
weight: 515
url: /ru/java/com.aspose.words/pagelayoutevent/
---

**Inheritance:**
java.lang.Object
```
public class PageLayoutEvent
```

Код события, вызываемого во время построения и рендеринга модели разметки страниц.

Модель разметки страницы строится в два этапа. Сначала — «шаг преобразования», когда разметка страницы извлекает содержимое документа и создаёт граф объектов. Затем — «шаг перераспределения», когда структуры разбиваются, объединяются и размещаются по страницам.

В зависимости от операции, вызвавшей построение, модель разметки страницы может быть либо не будет дополнительно отрисована в фиксированный формат страницы. Например, подсчёт количества страниц в документе или обновление полей не требует рендеринга, тогда как экспорт в Pdf требует.

 **Examples:** 

Показывает, как отслеживать изменения макета с помощью обратного вызова макета.

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
## Поля

| Поле | Описание |
| --- | --- |
| [BUILD_FINISHED](#BUILD-FINISHED) | Построение разметки страницы завершено. |
| [BUILD_STARTED](#BUILD-STARTED) | Построение разметки страницы началось. |
| [CONVERSION_FINISHED](#CONVERSION-FINISHED) | Преобразование модели документа в разметку страницы завершено. |
| [CONVERSION_STARTED](#CONVERSION-STARTED) | Преобразование модели документа в разметку страницы началось. |
| [NONE](#NONE) | Значение по умолчанию |
| [PART_REFLOW_FINISHED](#PART-REFLOW-FINISHED) | Перераспределение страницы завершено. |
| [PART_REFLOW_STARTED](#PART-REFLOW-STARTED) | Перераспределение страницы началось. |
| [PART_RENDERING_FINISHED](#PART-RENDERING-FINISHED) | Отрисовка страницы завершена. |
| [PART_RENDERING_STARTED](#PART-RENDERING-STARTED) | Отрисовка страницы началась. |
| [REFLOW_FINISHED](#REFLOW-FINISHED) | Перепоток макета страницы завершён. |
| [REFLOW_STARTED](#REFLOW-STARTED) | Перепоток макета страницы начался. |
| [WATCH_DOG](#WATCH-DOG) | Соответствует контрольной точке в коде, которая часто посещается и подходит для прерывания процесса. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String pageLayoutEventName)](#fromName-java.lang.String) |  |
| [getName(int pageLayoutEvent)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pageLayoutEvent)](#toString-int) |  |
### BUILD_FINISHED {#BUILD-FINISHED}
```
public static int BUILD_FINISHED
```


Построение макета страницы завершено. Событие генерируется один раз. Это последнее событие, которое происходит при вызове [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout).

### BUILD_STARTED {#BUILD-STARTED}
```
public static int BUILD_STARTED
```


Построение макета страницы началось. Событие генерируется один раз. Это первое событие, которое происходит при вызове [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout).

### CONVERSION_FINISHED {#CONVERSION-FINISHED}
```
public static int CONVERSION_FINISHED
```


Преобразование модели документа в макет страницы завершено. Событие генерируется один раз. Это происходит, когда модель макета прекращает извлекать содержимое документа.

### CONVERSION_STARTED {#CONVERSION-STARTED}
```
public static int CONVERSION_STARTED
```


Преобразование модели документа в макет страницы началось. Событие генерируется один раз. Это происходит, когда модель макета начинает извлекать содержимое документа.

### NONE {#NONE}
```
public static int NONE
```


Значение по умолчанию

### PART_REFLOW_FINISHED {#PART-REFLOW-FINISHED}
```
public static int PART_REFLOW_FINISHED
```


Перепоток страницы завершён. Обратите внимание, что страница может перепотокаться несколько раз и процесс может перезапускаться до завершения.

### PART_REFLOW_STARTED {#PART-REFLOW-STARTED}
```
public static int PART_REFLOW_STARTED
```


Перепоток страницы начался. Обратите внимание, что страница может перепотокаться несколько раз и процесс может перезапускаться до завершения.

### PART_RENDERING_FINISHED {#PART-RENDERING-FINISHED}
```
public static int PART_RENDERING_FINISHED
```


Отрисовка страницы завершена. Событие генерируется один раз для каждой страницы.

### PART_RENDERING_STARTED {#PART-RENDERING-STARTED}
```
public static int PART_RENDERING_STARTED
```


Отрисовка страницы началась. Событие генерируется один раз для каждой страницы.

### REFLOW_FINISHED {#REFLOW-FINISHED}
```
public static int REFLOW_FINISHED
```


Перепоток макета страницы завершён. Событие генерируется один раз. Это происходит, когда модель макета прекращает перепоток содержимого документа.

### REFLOW_STARTED {#REFLOW-STARTED}
```
public static int REFLOW_STARTED
```


Перепоток макета страницы начался. Событие генерируется один раз. Это происходит, когда модель макета начинает перепоток содержимого документа.

### WATCH_DOG {#WATCH-DOG}
```
public static int WATCH_DOG
```


Соответствует контрольной точке в коде, которая часто посещается и подходит для прерывания процесса.

Во время выполнения [IPageLayoutCallback.notify(com.aspose.words.PageLayoutCallbackArgs)](../../com.aspose.words/ipagelayoutcallback/\#notify-com.aspose.words.PageLayoutCallbackArgs) бросайте пользовательское исключение, чтобы прервать процесс.

Вы можете бросать исключение при обработке любого события обратного вызова, чтобы прервать процесс.

Обратите внимание, что если процесс прерван, модель макета страницы остаётся в неопределённом состоянии. Однако, если процесс прерван во время перепотока полной страницы, модель макета должна быть доступна до конца этой страницы.

### length {#length}
```
public static int length
```


### fromName(String pageLayoutEventName) {#fromName-java.lang.String}
```
public static int fromName(String pageLayoutEventName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| pageLayoutEventName | java.lang.String |  |

**Returns:**
int
### getName(int pageLayoutEvent) {#getName-int}
```
public static String getName(int pageLayoutEvent)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| pageLayoutEvent | int |  |

**Returns:**
java.lang.String
