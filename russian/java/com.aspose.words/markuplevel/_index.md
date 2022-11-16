---
title: MarkupLevel
second_title: Справочник по API Aspose.Words для Java
description: Указывает уровень в дереве документов, на котором может произойти то или иное.
type: docs
weight: 390
url: /ru/java/com.aspose.words/markuplevel/
---

**Наследование:**
java.lang.Object
```
public class MarkupLevel
```

 Определяет уровень в дереве документа, на котором[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) может возникнуть.
## Поля

| Поле | Описание |
| --- | --- |
| [BLOCK](#BLOCK) | Элемент встречается на уровне блока (например, |
| [CELL](#CELL) | Элемент встречается среди ячеек подряд. |
| [INLINE](#INLINE) | Элемент встречается на встроенном уровне (например, |
| [ROW](#ROW) | Элемент встречается среди строк в таблице. |
| [UNKNOWN](#UNKNOWN) | Указывает неизвестное или недопустимое значение. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String markupLevelName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int markupLevel)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int markupLevel)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### BLOCK {#BLOCK}
```
public static int BLOCK
```


Элемент встречается на уровне блока (например, среди таблиц и абзацев).

### CELL {#CELL}
```
public static int CELL
```


Элемент встречается среди ячеек подряд.

### INLINE {#INLINE}
```
public static int INLINE
```


Элемент встречается на встроенном уровне (например, среди фрагментов текста).

### ROW {#ROW}
```
public static int ROW
```


Элемент встречается среди строк в таблице.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Указывает неизвестное или недопустимое значение.

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
### fromName(String markupLevelName) {#fromName-java.lang.String-}
```
public static int fromName(String markupLevelName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| markupLevelName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int markupLevel) {#getName-int-}
```
public static String getName(int markupLevel)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| markupLevel | int |  |

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
### toString(int markupLevel) {#toString-int-}
```
public static String toString(int markupLevel)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| markupLevel | int |  |

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
