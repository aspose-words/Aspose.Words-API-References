---
title: FileFontSource
second_title: Справочник по API Aspose.Words для Java
description: Представляет один файл шрифта TrueType, хранящийся в файловой системе.
type: docs
weight: 264
url: /ru/java/com.aspose.words/filefontsource/
---

**Наследование:**
java.lang.Object, [com.aspose.words.FontSourceBase](../../com.aspose.words/fontsourcebase)
```
public class FileFontSource extends FontSourceBase
```

Представляет один файл шрифта TrueType, хранящийся в файловой системе.

 Чтобы узнать больше, посетите**Working with Fonts** документальная статья.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [FileFontSource(String filePath)](#FileFontSource-java.lang.String-) | Стор. |
| [FileFontSource(String filePath, int priority)](#FileFontSource-java.lang.String-int-) | Стор. |
| [FileFontSource(String filePath, int priority, String cacheKey)](#FileFontSource-java.lang.String-int-java.lang.String-) | Стор. |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAvailableFonts()](#getAvailableFonts--) | Возвращает список шрифтов, доступных через этот источник. |
| [getCacheKey()](#getCacheKey--) | Ключ этого источника в кеше. |
| [getClass()](#getClass--) |  |
| [getFilePath()](#getFilePath--) | Путь к файлу шрифта. |
| [getFontDataInternal()](#getFontDataInternal--) |  |
| [getPriority()](#getPriority--) | Возвращает приоритет источника шрифта. |
| [getPriorityInternal()](#getPriorityInternal--) |  |
| [getType()](#getType--) | Возвращает тип источника шрифта. |
| [getWarningCallback()](#getWarningCallback--) | Вызывается во время обработки источника шрифта при обнаружении проблемы, которая может привести к потере точности форматирования. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback-) | Вызывается во время обработки источника шрифта при обнаружении проблемы, которая может привести к потере точности форматирования. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### FileFontSource(String filePath) {#FileFontSource-java.lang.String-}
```
public FileFontSource(String filePath)
```


Стор.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| filePath | java.lang.String | Путь к файлу шрифта. |

### FileFontSource(String filePath, int priority) {#FileFontSource-java.lang.String-int-}
```
public FileFontSource(String filePath, int priority)
```


Стор.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| filePath | java.lang.String | Путь к файлу шрифта. |
| priority | int |  Приоритет источника шрифта. См.[FontSourceBase.getPriority()](../../com.aspose.words/fontsourcebase\#getPriority--) описание свойства для получения дополнительной информации. |

### FileFontSource(String filePath, int priority, String cacheKey) {#FileFontSource-java.lang.String-int-java.lang.String-}
```
public FileFontSource(String filePath, int priority, String cacheKey)
```


Стор.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| filePath | java.lang.String | Путь к файлу шрифта. |
| priority | int |  Приоритет источника шрифта. См.[FontSourceBase.getPriority()](../../com.aspose.words/fontsourcebase\#getPriority--) описание свойства для получения дополнительной информации. |
| cacheKey | java.lang.String |  Ключ этого источника в кеше. Видеть[getCacheKey()](../../com.aspose.words/filefontsource\#getCacheKey--) описание свойства для получения дополнительной информации. |

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


Ключ этого источника в кеше.

Этот ключ используется для идентификации элемента кеша при сохранении/загрузке кеша поиска шрифтов с помощью методов и .

 Если ключ не указан, то[getFilePath()](../../com.aspose.words/filefontsource\#getFilePath--) вместо этого будет использоваться в качестве ключа.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
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


Путь к файлу шрифта.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
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
