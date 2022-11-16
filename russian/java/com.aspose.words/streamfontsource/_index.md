---
title: StreamFontSource
second_title: Справочник по API Aspose.Words для Java
description: Базовый класс для пользовательского источника потокового шрифта.
type: docs
weight: 530
url: /ru/java/com.aspose.words/streamfontsource/
---

**Наследование:**
java.lang.Object, [com.aspose.words.FontSourceBase](../../com.aspose.words/fontsourcebase)
```
public abstract class StreamFontSource extends FontSourceBase
```

Базовый класс для пользовательского источника потокового шрифта.

 Чтобы узнать больше, посетите**Working with Fonts** документальная статья.

 Чтобы использовать источник шрифта потока, вы должны создать производный класс от[StreamFontSource](../../com.aspose.words/streamfontsource) и обеспечить реализацию[openFontDataStream()](../../com.aspose.words/streamfontsource\#openFontDataStream--) метод.

[openFontDataStream()](../../com.aspose.words/streamfontsource\#openFontDataStream--) метод может вызываться несколько раз. Впервые он будет вызван, когда Aspose.Words просканирует предоставленные источники шрифтов, чтобы получить список доступных шрифтов. Позже он может быть вызван, если шрифт используется в документе для анализа данных шрифта и внедрения данных шрифта в некоторые форматы вывода.

[StreamFontSource](../../com.aspose.words/streamfontsource)может быть полезным, поскольку позволяет загружать данные шрифта только тогда, когда это требуется, а не хранить их в памяти для[FontSettings](../../com.aspose.words/fontsettings) продолжительность жизни.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAvailableFonts()](#getAvailableFonts--) | Возвращает список шрифтов, доступных через этот источник. |
| [getCacheKey()](#getCacheKey--) | Ключ этого источника в кеше. |
| [getCacheKeyInternal()](#getCacheKeyInternal--) |  |
| [getClass()](#getClass--) |  |
| [getFilePath()](#getFilePath--) |  |
| [getFontDataInternal()](#getFontDataInternal--) |  |
| [getPriority()](#getPriority--) | Возвращает приоритет источника шрифта. |
| [getPriorityInternal()](#getPriorityInternal--) |  |
| [getSize()](#getSize--) |  |
| [getType()](#getType--) | Возвращает тип источника шрифта. |
| [getWarningCallback()](#getWarningCallback--) | Вызывается во время обработки источника шрифта при обнаружении проблемы, которая может привести к потере точности форматирования. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [openFontDataStream()](#openFontDataStream--) | Этот метод должен открывать поток с данными шрифта по требованию. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback-) | Вызывается во время обработки источника шрифта при обнаружении проблемы, которая может привести к потере точности форматирования. |
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
### getAvailableFonts() {#getAvailableFonts--}
```
public ArrayList getAvailableFonts()
```


Возвращает список шрифтов, доступных через этот источник.

**Возвращает:**
java.util.ArrayList
### getCacheKey() {#getCacheKey--}
```
public String getCacheKey()
```


Ключ этого источника в кеше. Этот ключ используется для идентификации элемента кеша при сохранении/загрузке кеша поиска шрифтов с помощью методов и .

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getCacheKeyInternal() {#getCacheKeyInternal--}
```
public String getCacheKeyInternal()
```




**Возвращает:**
java.lang.String
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getFilePath() {#getFilePath--}
```
public String getFilePath()
```




**Возвращает:**
java.lang.String
### getFontDataInternal() {#getFontDataInternal--}
```
public Iterable getFontDataInternal()
```




**Возвращает:**
java.lang.Iterable
### getPriority() {#getPriority--}
```
public int getPriority()
```


Возвращает приоритет источника шрифта.

Это значение используется при наличии шрифтов с одинаковым именем семейства и стилем в разных источниках шрифтов. В этом случае Aspose.Words выбирает шрифт из источника с более высоким значением приоритета.

Значение по умолчанию — 0.

**Возвращает:**
int - приоритет источника шрифта.
### getPriorityInternal() {#getPriorityInternal--}
```
public int getPriorityInternal()
```




**Возвращает:**
инт
### getSize() {#getSize--}
```
public int getSize()
```




**Возвращает:**
инт
### getType() {#getType--}
```
public int getType()
```


Возвращает тип источника шрифта.

**Возвращает:**
 int - Тип источника шрифта. Возвращаемое значение является одним из[FontSourceType](../../com.aspose.words/fontsourcetype) константы.
### getWarningCallback() {#getWarningCallback--}
```
public IWarningCallback getWarningCallback()
```


Вызывается во время обработки источника шрифта при обнаружении проблемы, которая может привести к потере точности форматирования.

**Возвращает:**
[IWarningCallback](../../com.aspose.words/iwarningcallback) - соответствующий[IWarningCallback](../../com.aspose.words/iwarningcallback) ценность.
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




### openFontDataStream() {#openFontDataStream--}
```
public abstract InputStream openFontDataStream()
```


Этот метод должен открывать поток с данными шрифта по требованию.

**Возвращает:**
java.io.InputStream — поток данных шрифта. Поток будет закрыт после прочтения. Нет необходимости закрывать его явно.
### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback-}
```
public void setWarningCallback(IWarningCallback value)
```


Вызывается во время обработки источника шрифта при обнаружении проблемы, которая может привести к потере точности форматирования.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback) |  Соответствующий[IWarningCallback](../../com.aspose.words/iwarningcallback) ценность. |

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
