---
title: PdfFontEmbeddingMode
second_title: Справочник по API Aspose.Words для Java
description: Указывает, как Aspose.Words должен встраивать шрифты.
type: docs
weight: 455
url: /ru/java/com.aspose.words/pdffontembeddingmode/
---

**Наследование:**
java.lang.Object
```
public class PdfFontEmbeddingMode
```

Указывает, как Aspose.Words должен встраивать шрифты.
## Поля

| Поле | Описание |
| --- | --- |
| [EMBED_ALL](#EMBED-ALL) | Aspose.Words встраивает все шрифты. |
| [EMBED_NONE](#EMBED-NONE) | Aspose.Words не встраивает никаких шрифтов. |
| [EMBED_NONSTANDARD](#EMBED-NONSTANDARD) | Aspose.Words встраивает все шрифты, кроме стандартных шрифтов Windows Arial и Times New Roman. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String pdfFontEmbeddingModeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int pdfFontEmbeddingMode)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int pdfFontEmbeddingMode)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### EMBED_ALL {#EMBED-ALL}
```
public static int EMBED_ALL
```


Aspose.Words встраивает все шрифты.

### EMBED_NONE {#EMBED-NONE}
```
public static int EMBED_NONE
```


Aspose.Words не встраивает никаких шрифтов.

### EMBED_NONSTANDARD {#EMBED-NONSTANDARD}
```
public static int EMBED_NONSTANDARD
```


Aspose.Words встраивает все шрифты, кроме стандартных шрифтов Windows Arial и Times New Roman. В этом режиме затрагиваются только шрифты Arial и Times New Roman, поскольку MS Word не встраивает только эти шрифты при сохранении документа в PDF.

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
### fromName(String pdfFontEmbeddingModeName) {#fromName-java.lang.String-}
```
public static int fromName(String pdfFontEmbeddingModeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfFontEmbeddingModeName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int pdfFontEmbeddingMode) {#getName-int-}
```
public static String getName(int pdfFontEmbeddingMode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfFontEmbeddingMode | int |  |

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
### toString(int pdfFontEmbeddingMode) {#toString-int-}
```
public static String toString(int pdfFontEmbeddingMode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfFontEmbeddingMode | int |  |

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
