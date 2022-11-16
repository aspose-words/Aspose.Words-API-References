---
title: PageLayoutCallbackArgs
second_title: Справочник по API Aspose.Words для Java
description: Аргумент, переданный в
type: docs
weight: 435
url: /ru/java/com.aspose.words/pagelayoutcallbackargs/
---

**Наследование:**
java.lang.Object
```
public class PageLayoutCallbackArgs
```

 Аргумент, переданный в[IPageLayoutCallback.notify(com.aspose.words.PageLayoutCallbackArgs)](../../com.aspose.words/ipagelayoutcallback\#notify-com.aspose.words.PageLayoutCallbackArgs-)

 Чтобы узнать больше, посетите**Converting to Fixed-page Format** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDocument()](#getDocument--) | Получает документ. |
| [getEvent()](#getEvent--) | Получает событие. |
| [getPageIndex()](#getPageIndex--) | Получает отсчитываемый от 0 индекс страницы в документе, к которому относится это событие. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getDocument() {#getDocument--}
```
public Document getDocument()
```


Получает документ.

**Возвращает:**
[Document](../../com.aspose.words/document) - Документ.
### getEvent() {#getEvent--}
```
public int getEvent()
```


Получает событие.

**Возвращает:**
 int - Событие. Возвращаемое значение является одним из[PageLayoutEvent](../../com.aspose.words/pagelayoutevent) константы.
### getPageIndex() {#getPageIndex--}
```
public int getPageIndex()
```


Получает отсчитываемый от 0 индекс страницы в документе, к которому относится это событие. Возвращает отрицательное значение, если нет связанной страницы или страница была удалена во время перекомпоновки.

**Возвращает:**
int - отсчитываемый от 0 индекс страницы в документе, к которому относится это событие.
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
