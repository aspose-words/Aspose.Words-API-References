---
title: PageLayoutEvent
second_title: Справочник по API Aspose.Words для Java
description: Код события, возникающего во время построения и рендеринга модели макета страницы.
type: docs
weight: 436
url: /ru/java/com.aspose.words/pagelayoutevent/
---

**Наследование:**
java.lang.Object
```
public class PageLayoutEvent
```

Код события, возникающего во время построения и рендеринга модели макета страницы.

Модель макета страницы строится в два этапа. Во-первых, «этап преобразования», когда макет страницы извлекает содержимое документа и создает граф объектов. Во-вторых, «шаг перекомпоновки», когда структуры разделяются, объединяются и объединяются в страницы.

В зависимости от операции, вызвавшей сборку, модель макета страницы может быть преобразована в фиксированный формат страницы, а может и нет. Например, вычисление количества страниц в документе или обновление полей не требует рендеринга, тогда как экспорт в Pdf требует.
## Поля

| Поле | Описание |
| --- | --- |
| [BUILD_FINISHED](#BUILD-FINISHED) | Сборка макета страницы завершена. |
| [BUILD_STARTED](#BUILD-STARTED) | Начата сборка макета страницы. |
| [CONVERSION_FINISHED](#CONVERSION-FINISHED) | Преобразование модели документа в макет страницы завершено. |
| [CONVERSION_STARTED](#CONVERSION-STARTED) | Начато преобразование модели документа в макет страницы. |
| [NONE](#NONE) | Значение по умолчанию |
| [PART_REFLOW_FINISHED](#PART-REFLOW-FINISHED) | Перекомпоновка страницы завершена. |
| [PART_REFLOW_STARTED](#PART-REFLOW-STARTED) | Переформатирование страницы началось. |
| [PART_RENDERING_FINISHED](#PART-RENDERING-FINISHED) | Рендеринг страницы завершен. |
| [PART_RENDERING_STARTED](#PART-RENDERING-STARTED) | Рендеринг страницы начался. |
| [REFLOW_FINISHED](#REFLOW-FINISHED) | Перекомпоновка макета страницы завершена. |
| [REFLOW_STARTED](#REFLOW-STARTED) | Началась перекомпоновка макета страницы. |
| [WATCH_DOG](#WATCH-DOG) | Соответствует контрольной точке в коде, которую часто посещают и которая подходит для прерывания процесса. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String pageLayoutEventName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int pageLayoutEvent)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int pageLayoutEvent)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### BUILD_FINISHED {#BUILD-FINISHED}
```
public static int BUILD_FINISHED
```


 Сборка макета страницы завершена. Выстрелил один раз. Это последнее событие, которое происходит, когда[Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--) называется.

### BUILD_STARTED {#BUILD-STARTED}
```
public static int BUILD_STARTED
```


 Начата сборка макета страницы. Выстрелил один раз. Это первое событие, которое происходит, когда[Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--) называется.

### CONVERSION_FINISHED {#CONVERSION-FINISHED}
```
public static int CONVERSION_FINISHED
```


Преобразование модели документа в макет страницы завершено. Выстрелил один раз. Это происходит, когда модель макета перестает извлекать содержимое документа.

### CONVERSION_STARTED {#CONVERSION-STARTED}
```
public static int CONVERSION_STARTED
```


Начато преобразование модели документа в макет страницы. Выстрелил один раз. Это происходит, когда модель макета начинает извлекать содержимое документа.

### NONE {#NONE}
```
public static int NONE
```


Значение по умолчанию

### PART_REFLOW_FINISHED {#PART-REFLOW-FINISHED}
```
public static int PART_REFLOW_FINISHED
```


Перекомпоновка страницы завершена. Обратите внимание, что страница может переформатироваться несколько раз, и эта перекомпоновка может перезапуститься до того, как она будет завершена.

### PART_REFLOW_STARTED {#PART-REFLOW-STARTED}
```
public static int PART_REFLOW_STARTED
```


Переформатирование страницы началось. Обратите внимание, что страница может переформатироваться несколько раз, и эта перекомпоновка может перезапуститься до того, как она будет завершена.

### PART_RENDERING_FINISHED {#PART-RENDERING-FINISHED}
```
public static int PART_RENDERING_FINISHED
```


Рендеринг страницы завершен. Это запускается один раз на странице.

### PART_RENDERING_STARTED {#PART-RENDERING-STARTED}
```
public static int PART_RENDERING_STARTED
```


Рендеринг страницы начался. Это запускается один раз на странице.

### REFLOW_FINISHED {#REFLOW-FINISHED}
```
public static int REFLOW_FINISHED
```


Перекомпоновка макета страницы завершена. Выстрелил один раз. Это происходит, когда модель макета перестает перекомпоновывать содержимое документа.

### REFLOW_STARTED {#REFLOW-STARTED}
```
public static int REFLOW_STARTED
```


Началась перекомпоновка макета страницы. Выстрелил один раз. Это происходит, когда модель макета начинает переформатировать содержимое документа.

### WATCH_DOG {#WATCH-DOG}
```
public static int WATCH_DOG
```


Соответствует контрольной точке в коде, которую часто посещают и которая подходит для прерывания процесса.

 Пока внутри[IPageLayoutCallback.notify(com.aspose.words.PageLayoutCallbackArgs)](../../com.aspose.words/ipagelayoutcallback\#notify-com.aspose.words.PageLayoutCallbackArgs-) выдать пользовательское исключение, чтобы прервать процесс.

Вы можете бросить при обработке любого события обратного вызова, чтобы прервать процесс.

Обратите внимание, что если процесс прерывается, модель макета страницы остается в неопределенном состоянии. Однако, если процесс прерывается при перекомпоновке всей страницы, должна быть возможность использовать модель макета до конца этой страницы.

### length {#length}
```
public static int length
```


### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Возвращает:**
логический
### fromName(String pageLayoutEventName) {#fromName-java.lang.String-}
```
public static int fromName(String pageLayoutEventName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pageLayoutEventName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int pageLayoutEvent) {#getName-int-}
```
public static String getName(int pageLayoutEvent)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pageLayoutEvent | int |  |

**Возвращает:**
java.lang.String
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Возвращает:**
инт[]
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### toString() {#toString--}
```
public String toString()
```




**Возвращает:**
java.lang.String
### toString(int pageLayoutEvent) {#toString-int-}
```
public static String toString(int pageLayoutEvent)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pageLayoutEvent | int |  |

**Возвращает:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
