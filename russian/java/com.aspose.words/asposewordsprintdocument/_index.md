---
title: AsposeWordsPrintDocument
second_title: Справочник по API Aspose.Words для Java
description: Предоставляет реализацию по умолчанию для печати в среде печати Java.
type: docs
weight: 14
url: /ru/java/com.aspose.words/asposewordsprintdocument/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.awt.print.Pageable, java.awt.print.Printable
```
public class AsposeWordsPrintDocument implements Pageable, Printable
```

 Обеспечивает реализацию по умолчанию для печати[Document](../../com.aspose.words/document) в среде печати Java.

 Чтобы узнать больше, посетите**Printing a Document Programmatically or Using Dialogs** документальная статья.

[AsposeWordsPrintDocument](../../com.aspose.words/asposewordsprintdocument) переопределяет оба и .

 Один документ Aspose.Words может состоять из нескольких разделов, в которых указаны страницы разного размера, ориентации и лотков для бумаги.[AsposeWordsPrintDocument](../../com.aspose.words/asposewordsprintdocument) следует использовать для правильной печати на бумаге разного размера, ориентации и т. д.

 С другой стороны, если документ состоит только из одного раздела, разработчик может использовать[AsposeWordsPrintDocument](../../com.aspose.words/asposewordsprintdocument) как улучшить производительность печати.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [AsposeWordsPrintDocument(Document document)](#AsposeWordsPrintDocument-com.aspose.words.Document-) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getNumberOfPages()](#getNumberOfPages--) |  |
| [getPageFormat(int pageIndex)](#getPageFormat-int-) |  |
| [getPrintable(int pageIndex)](#getPrintable-int-) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [print(Graphics graphics, PageFormat pageFormat, int pageIndex)](#print-java.awt.Graphics-java.awt.print.PageFormat-int-) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### AsposeWordsPrintDocument(Document document) {#AsposeWordsPrintDocument-com.aspose.words.Document-}
```
public AsposeWordsPrintDocument(Document document)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document) | Документ для печати. |

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
### getNumberOfPages() {#getNumberOfPages--}
```
public int getNumberOfPages()
```




**Возвращает:**
инт
### getPageFormat(int pageIndex) {#getPageFormat-int-}
```
public PageFormat getPageFormat(int pageIndex)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pageIndex | int |  |

**Возвращает:**
java.awt.print.PageFormat
### getPrintable(int pageIndex) {#getPrintable-int-}
```
public Printable getPrintable(int pageIndex)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pageIndex | int |  |

**Возвращает:**
java.awt.print.Printable
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




### print(Graphics graphics, PageFormat pageFormat, int pageIndex) {#print-java.awt.Graphics-java.awt.print.PageFormat-int-}
```
public int print(Graphics graphics, PageFormat pageFormat, int pageIndex)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| graphics | java.awt.Graphics |  |
| pageFormat | java.awt.print.PageFormat |  |
| pageIndex | int |  |

**Возвращает:**
инт
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
