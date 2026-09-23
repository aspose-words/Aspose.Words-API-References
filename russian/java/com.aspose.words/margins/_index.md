---
title: "Поля"
linktitle: "Поля"
second_title: "Aspose.Words для Java"
description: "Указывает предустановленные поля в Java."
type: docs
weight: 449
url: /ru/java/com.aspose.words/margins/
---

**Inheritance:**
java.lang.Object
```
public class Margins
```

Указывает предустановленные поля.

 **Examples:** 

Показывает, когда пересчитывать компоновку страниц документа.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Saving a document to PDF, to an image, or printing for the first time will automatically
 // cache the layout of the document within its pages.
 doc.save(getArtifactsDir() + "Document.UpdatePageLayout.1.pdf");

 // Modify the document in some way.
 doc.getStyles().get("Normal").getFont().setSize(6.0);
 doc.getSections().get(0).getPageSetup().setOrientation(Orientation.LANDSCAPE);
 doc.getSections().get(0).getPageSetup().setMargins(Margins.MIRRORED);

 // In the current version of Aspose.Words, modifying the document does not automatically rebuild
 // the cached page layout. If we wish for the cached layout
 // to stay up to date, we will need to update it manually.
 doc.updatePageLayout();

 doc.save(getArtifactsDir() + "Document.UpdatePageLayout.2.pdf");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [CUSTOM](#CUSTOM) | Пользовательские поля. |
| [MIRRORED](#MIRRORED) | Отражённые поля. |
| [MODERATE](#MODERATE) | Умеренные поля. |
| [NARROW](#NARROW) | Узкие поля. |
| [NORMAL](#NORMAL) | Обычные поля. |
| [WIDE](#WIDE) | Широкие поля. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String marginsName)](#fromName-java.lang.String) |  |
| [getName(int margins)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int margins)](#toString-int) |  |
### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


Пользовательские поля.

### MIRRORED {#MIRRORED}
```
public static int MIRRORED
```


Отражённые поля.

 **Remarks:** 

Установка полей в значение Mirrored задаст соответствующее значение свойства [PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup/\#getMultiplePages) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup/\#setMultiplePages-int). Это повлияет на весь документ, а не только на текущий раздел.

### MODERATE {#MODERATE}
```
public static int MODERATE
```


Умеренные поля.

### NARROW {#NARROW}
```
public static int NARROW
```


Узкие поля.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Обычные поля.

### WIDE {#WIDE}
```
public static int WIDE
```


Широкие поля.

### length {#length}
```
public static int length
```


### fromName(String marginsName) {#fromName-java.lang.String}
```
public static int fromName(String marginsName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| marginsName | java.lang.String |  |

**Returns:**
int
### getName(int margins) {#getName-int}
```
public static String getName(int margins)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| margins | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int margins) {#toString-int}
```
public static String toString(int margins)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| margins | int |  |

**Returns:**
java.lang.String
