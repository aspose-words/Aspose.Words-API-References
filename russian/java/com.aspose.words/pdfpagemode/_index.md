---
title: PdfPageMode
second_title: Справочник по API Aspose.Words для Java
description: Указывает, как документ PDF должен отображаться при открытии в программе чтения PDF.
type: docs
weight: 459
url: /ru/java/com.aspose.words/pdfpagemode/
---

**Наследование:**
java.lang.Object
```
public class PdfPageMode
```

Указывает, как документ PDF должен отображаться при открытии в программе чтения PDF.
## Поля

| Поле | Описание |
| --- | --- |
| [FULL_SCREEN](#FULL-SCREEN) | Полноэкранный режим, без строки меню, оконных элементов управления или любого другого видимого окна. |
| [USE_ATTACHMENTS](#USE-ATTACHMENTS) | Панель вложений видна. |
| [USE_NONE](#USE-NONE) | Ни контур документа, ни эскизы изображений не видны. |
| [USE_OC](#USE-OC) | Необязательная панель группы содержимого видна. |
| [USE_OUTLINES](#USE-OUTLINES) | Контур документа виден. |
| [USE_THUMBS](#USE-THUMBS) | Миниатюры изображений видны. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String pdfPageModeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int pdfPageMode)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int pdfPageMode)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### FULL_SCREEN {#FULL-SCREEN}
```
public static int FULL_SCREEN
```


Полноэкранный режим, без строки меню, оконных элементов управления или любого другого видимого окна.

### USE_ATTACHMENTS {#USE-ATTACHMENTS}
```
public static int USE_ATTACHMENTS
```


 Панель вложений видна. Не поддерживается в следующих версиях PDF:[PdfCompliance.PDF\_A\_1\_A](../../com.aspose.words/pdfcompliance\#PDF-A-1-A), [PdfCompliance.PDF\_A\_1\_B](../../com.aspose.words/pdfcompliance\#PDF-A-1-B).

### USE_NONE {#USE-NONE}
```
public static int USE_NONE
```


Ни контур документа, ни эскизы изображений не видны.

### USE_OC {#USE-OC}
```
public static int USE_OC
```


 Необязательная панель группы содержимого видна. Не поддерживается в следующих версиях PDF:[PdfCompliance.PDF\_A\_1\_A](../../com.aspose.words/pdfcompliance\#PDF-A-1-A), [PdfCompliance.PDF\_A\_1\_B](../../com.aspose.words/pdfcompliance\#PDF-A-1-B).

### USE_OUTLINES {#USE-OUTLINES}
```
public static int USE_OUTLINES
```


Контур документа виден. Обратите внимание, что если в документе PDF нет контуров, панель навигации по контуру все равно не будет видна.

### USE_THUMBS {#USE-THUMBS}
```
public static int USE_THUMBS
```


Миниатюры изображений видны.

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
### fromName(String pdfPageModeName) {#fromName-java.lang.String-}
```
public static int fromName(String pdfPageModeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfPageModeName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int pdfPageMode) {#getName-int-}
```
public static String getName(int pdfPageMode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfPageMode | int |  |

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
### toString(int pdfPageMode) {#toString-int-}
```
public static String toString(int pdfPageMode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfPageMode | int |  |

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
