---
title: PdfCompliance
second_title: Справочник по API Aspose.Words для Java
description: Указывает уровень соответствия стандартам PDF.
type: docs
weight: 449
url: /ru/java/com.aspose.words/pdfcompliance/
---

**Наследование:**
java.lang.Object
```
public class PdfCompliance
```

Указывает уровень соответствия стандартам PDF.
## Поля

| Поле | Описание |
| --- | --- |
| [PDF_17](#PDF-17) | Выходной файл будет соответствовать стандарту PDF 1.7 (ISO 32000-1). |
| [PDF_20](#PDF-20) | Выходной файл будет соответствовать стандарту PDF 2.0 (ISO 32000-2). |
| [PDF_A_1_A](#PDF-A-1-A) | Выходной файл будет соответствовать стандарту PDF/A-1a (ISO 19005-1). |
| [PDF_A_1_B](#PDF-A-1-B) | Выходной файл будет соответствовать стандарту PDF/A-1b (ISO 19005-1). |
| [PDF_A_2_A](#PDF-A-2-A) | Выходной файл будет соответствовать стандарту PDF/A-2a (ISO 19005-2). |
| [PDF_A_2_U](#PDF-A-2-U) | Выходной файл будет соответствовать стандарту PDF/A-2u (ISO 19005-2). |
| [PDF_A_4](#PDF-A-4) | Выходной файл будет соответствовать стандарту PDF/A-4 (ISO 19005-4:2020). |
| [PDF_UA_1](#PDF-UA-1) | Выходной файл будет соответствовать стандарту PDF/UA-1 (ISO 14289-1). |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String pdfComplianceName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int pdfCompliance)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int pdfCompliance)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### PDF_17 {#PDF-17}
```
public static int PDF_17
```


Выходной файл будет соответствовать стандарту PDF 1.7 (ISO 32000-1).

### PDF_20 {#PDF-20}
```
public static int PDF_20
```


Выходной файл будет соответствовать стандарту PDF 2.0 (ISO 32000-2).

### PDF_A_1_A {#PDF-A-1-A}
```
public static int PDF_A_1_A
```


Выходной файл будет соответствовать стандарту PDF/A-1a (ISO 19005-1). Этот уровень включает в себя все требования PDF/A-1b и дополнительно требует, чтобы была включена структура документа (также известная как «помеченная») с целью обеспечения возможности поиска и изменения содержимого документа. Обратите внимание, что экспорт структуры документа значительно увеличивает потребление памяти, особенно для больших документов.

### PDF_A_1_B {#PDF-A-1-B}
```
public static int PDF_A_1_B
```


Выходной файл будет соответствовать стандарту PDF/A-1b (ISO 19005-1). PDF/A-1b предназначен для обеспечения надежного воспроизведения внешнего вида документа.

### PDF_A_2_A {#PDF-A-2-A}
```
public static int PDF_A_2_A
```


Выходной файл будет соответствовать стандарту PDF/A-2a (ISO 19005-2). Этот уровень включает в себя все требования PDF/A-2u и дополнительно требует, чтобы была включена структура документа (также известная как «помеченная») с целью обеспечения возможности поиска и изменения содержимого документа. Обратите внимание, что экспорт структуры документа значительно увеличивает потребление памяти, особенно для больших документов.

### PDF_A_2_U {#PDF-A-2-U}
```
public static int PDF_A_2_U
```


Выходной файл будет соответствовать стандарту PDF/A-2u (ISO 19005-2). PDF/A-2u имеет целью сохранение статического внешнего вида документа с течением времени, независимо от инструментов и систем, используемых для создания, хранения или рендеринга файлов. Кроме того, любой текст, содержащийся в документе, может быть надежно извлечен как последовательность кодовых точек Unicode.

### PDF_A_4 {#PDF-A-4}
```
public static int PDF_A_4
```


Выходной файл будет соответствовать стандарту PDF/A-4 (ISO 19005-4:2020). PDF/A-4 имеет целью сохранение статического внешнего вида документа с течением времени, независимо от инструментов и систем, используемых для создания, хранения или рендеринга файлов. Кроме того, любой текст, содержащийся в документе, может быть надежно извлечен как последовательность кодовых точек Unicode.

### PDF_UA_1 {#PDF-UA-1}
```
public static int PDF_UA_1
```


Выходной файл будет соответствовать стандарту PDF/UA-1 (ISO 14289-1). Основная цель PDF/UA — определить, как представлять электронные документы в формате PDF таким образом, чтобы файл был доступен.

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
### fromName(String pdfComplianceName) {#fromName-java.lang.String-}
```
public static int fromName(String pdfComplianceName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfComplianceName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int pdfCompliance) {#getName-int-}
```
public static String getName(int pdfCompliance)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfCompliance | int |  |

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
### toString(int pdfCompliance) {#toString-int-}
```
public static String toString(int pdfCompliance)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfCompliance | int |  |

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
