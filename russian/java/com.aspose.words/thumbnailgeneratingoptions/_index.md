---
title: ThumbnailGeneratingOptions
second_title: Справочник по API Aspose.Words для Java
description: Может использоваться для указания дополнительных параметров при создании миниатюры для документа.
type: docs
weight: 578
url: /ru/java/com.aspose.words/thumbnailgeneratingoptions/
---

**Наследование:**
java.lang.Object
```
public class ThumbnailGeneratingOptions
```

 Может использоваться для указания дополнительных параметров при создании миниатюры для документа. Пользователь может вызвать метод[Document.updateThumbnail(com.aspose.words.ThumbnailGeneratingOptions)](../../com.aspose.words/document\#updateThumbnail-com.aspose.words.ThumbnailGeneratingOptions-) генерировать[BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties\#getThumbnail--) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties\#setThumbnail-byte---) для документа.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getGenerateFromFirstPage()](#getGenerateFromFirstPage--) | Указывает, следует ли создавать миниатюру из первой страницы документа или первого изображения. |
| [getThumbnailSize()](#getThumbnailSize--) | Размер создаваемой миниатюры в пикселях. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setGenerateFromFirstPage(boolean value)](#setGenerateFromFirstPage-boolean-) | Указывает, следует ли создавать миниатюру из первой страницы документа или первого изображения. |
| [setThumbnailSize(Dimension value)](#setThumbnailSize-java.awt.Dimension-) | Размер создаваемой миниатюры в пикселях. |
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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getGenerateFromFirstPage() {#getGenerateFromFirstPage--}
```
public boolean getGenerateFromFirstPage()
```


Указывает, следует ли создавать миниатюру из первой страницы документа или первого изображения. Значение по умолчанию — true , что означает, что миниатюра будет создана с первой страницы документа. Если значение равно false и в документе нет изображения, эскиз будет сгенерирован с первой страницы документа.

**Возвращает:**
boolean - соответствующее логическое значение.
### getThumbnailSize() {#getThumbnailSize--}
```
public Dimension getThumbnailSize()
```


Размер создаваемой миниатюры в пикселях. По умолчанию 600x900.

**Возвращает:**
java.awt.Dimension — соответствующее значение java.awt.Dimension.
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




### setGenerateFromFirstPage(boolean value) {#setGenerateFromFirstPage-boolean-}
```
public void setGenerateFromFirstPage(boolean value)
```


Указывает, следует ли создавать миниатюру из первой страницы документа или первого изображения. Значение по умолчанию — true , что означает, что миниатюра будет создана с первой страницы документа. Если значение равно false и в документе нет изображения, эскиз будет сгенерирован с первой страницы документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setThumbnailSize(Dimension value) {#setThumbnailSize-java.awt.Dimension-}
```
public void setThumbnailSize(Dimension value)
```


Размер создаваемой миниатюры в пикселях. По умолчанию 600x900.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.awt.Dimension | Соответствующее значение java.awt.Dimension. |

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
