---
title: EmbeddedFontFormat
second_title: Справочник по API Aspose.Words для Java
description: Задает формат конкретного встроенного шрифта внутри объекта.
type: docs
weight: 141
url: /ru/java/com.aspose.words/embeddedfontformat/
---

**Наследование:**
java.lang.Object
```
public class EmbeddedFontFormat
```

 Определяет формат конкретного встроенного шрифта внутри[FontInfo](../../com.aspose.words/fontinfo) объект.

При сохранении документа в файл записываются только встроенные шрифты соответствующего формата.
## Поля

| Поле | Описание |
| --- | --- |
| [EMBEDDED_OPEN_TYPE](#EMBEDDED-OPEN-TYPE) | Указывает встроенный формат файла OpenType (EOT). |
| [OPEN_TYPE](#OPEN-TYPE) | Определяет шрифт, встроенный как обычная копия файла шрифта OpenType (TrueType). |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String embeddedFontFormatName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int embeddedFontFormat)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int embeddedFontFormat)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### EMBEDDED_OPEN_TYPE {#EMBEDDED-OPEN-TYPE}
```
public static int EMBEDDED_OPEN_TYPE
```


Указывает встроенный формат файла OpenType (EOT).

Этот формат встроенных шрифтов используется в файлах DOC.

См. http://www.w3.org/Submission/EOT для описания формата.

### OPEN_TYPE {#OPEN-TYPE}
```
public static int OPEN_TYPE
```


Определяет шрифт, встроенный как обычная копия файла шрифта OpenType (TrueType).

Этот формат встроенных шрифтов используется в формате Open Office XML, включая файлы DOCX.

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
### fromName(String embeddedFontFormatName) {#fromName-java.lang.String-}
```
public static int fromName(String embeddedFontFormatName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| embeddedFontFormatName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int embeddedFontFormat) {#getName-int-}
```
public static String getName(int embeddedFontFormat)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| embeddedFontFormat | int |  |

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
### toString(int embeddedFontFormat) {#toString-int-}
```
public static String toString(int embeddedFontFormat)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| embeddedFontFormat | int |  |

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
