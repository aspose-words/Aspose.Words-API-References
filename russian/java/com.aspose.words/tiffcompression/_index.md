---
title: TiffCompression
second_title: Справочник по API Aspose.Words для Java
description: Указывает, какой тип сжатия следует применять при сохранении изображений страниц в файл TIFF.
type: docs
weight: 579
url: /ru/java/com.aspose.words/tiffcompression/
---

**Наследование:**
java.lang.Object
```
public class TiffCompression
```

Указывает, какой тип сжатия следует применять при сохранении изображений страниц в файл TIFF.
## Поля

| Поле | Описание |
| --- | --- |
| [CCITT_3](#CCITT-3) | Указывает схему сжатия CCITT3. |
| [CCITT_4](#CCITT-4) | Указывает схему сжатия CCITT4. |
| [LZW](#LZW) | Указывает схему сжатия LZW. |
| [NONE](#NONE) | Указывает отсутствие сжатия. |
| [RLE](#RLE) | Указывает схему сжатия RLE. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String tiffCompressionName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int tiffCompression)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int tiffCompression)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### CCITT_3 {#CCITT-3}
```
public static int CCITT_3
```


Указывает схему сжатия CCITT3.

### CCITT_4 {#CCITT-4}
```
public static int CCITT_4
```


Указывает схему сжатия CCITT4.

### LZW {#LZW}
```
public static int LZW
```


Указывает схему сжатия LZW. В Java эмулируется сжатие Deflate (Zip).

### NONE {#NONE}
```
public static int NONE
```


Указывает отсутствие сжатия.

### RLE {#RLE}
```
public static int RLE
```


Указывает схему сжатия RLE.

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
### fromName(String tiffCompressionName) {#fromName-java.lang.String-}
```
public static int fromName(String tiffCompressionName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| tiffCompressionName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int tiffCompression) {#getName-int-}
```
public static String getName(int tiffCompression)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| tiffCompression | int |  |

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
### toString(int tiffCompression) {#toString-int-}
```
public static String toString(int tiffCompression)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| tiffCompression | int |  |

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
