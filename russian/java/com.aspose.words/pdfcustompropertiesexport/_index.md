---
title: PdfCustomPropertiesExport
second_title: Справочник по API Aspose.Words для Java
description: Указывает способ экспорта в файл PDF.
type: docs
weight: 450
url: /ru/java/com.aspose.words/pdfcustompropertiesexport/
---

**Наследование:**
java.lang.Object
```
public class PdfCustomPropertiesExport
```

 Указывает способ[Document.getCustomDocumentProperties()](../../com.aspose.words/document\#getCustomDocumentProperties--) экспортируются в файл PDF.
## Поля

| Поле | Описание |
| --- | --- |
| [METADATA](#METADATA) | Пользовательские свойства — это метаданные. |
| [NONE](#NONE) | Пользовательские свойства не экспортируются. |
| [STANDARD](#STANDARD) | Пользовательские свойства экспортируются как записи в словаре /Info. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String pdfCustomPropertiesExportName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int pdfCustomPropertiesExport)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int pdfCustomPropertiesExport)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### METADATA {#METADATA}
```
public static int METADATA
```


Пользовательские свойства — это метаданные.

Пространство имен экспортируемых свойств в пакете XMP — «custprops». С каждым свойством связан xml-элемент «custprops:Property1», «custprops:Property2» и так далее. Внутри элемента свойства находится элемент "rdf:Description". Элемент описания состоит из двух элементов «custprops:Name», содержащих имя пользовательского свойства в качестве значения этого xml-элемента, и «custprops:Value», содержащего значение пользовательского свойства в качестве значения этого xml-элемента.

### NONE {#NONE}
```
public static int NONE
```


Пользовательские свойства не экспортируются.

### STANDARD {#STANDARD}
```
public static int STANDARD
```


Пользовательские свойства экспортируются как записи в словаре /Info.

Пользовательские свойства со следующими именами не экспортируются: «Заголовок», «Автор», «Тема», «Ключевые слова», «Создатель», «Производитель», «Дата создания», «Дата модификации», «В ловушке».

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
### fromName(String pdfCustomPropertiesExportName) {#fromName-java.lang.String-}
```
public static int fromName(String pdfCustomPropertiesExportName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfCustomPropertiesExportName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int pdfCustomPropertiesExport) {#getName-int-}
```
public static String getName(int pdfCustomPropertiesExport)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfCustomPropertiesExport | int |  |

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
### toString(int pdfCustomPropertiesExport) {#toString-int-}
```
public static String toString(int pdfCustomPropertiesExport)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfCustomPropertiesExport | int |  |

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
