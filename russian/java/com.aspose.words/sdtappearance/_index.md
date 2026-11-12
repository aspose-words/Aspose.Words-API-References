---
title: "SdtAppearance"
linktitle: "SdtAppearance"
second_title: "Aspose.Words для Java"
description: "Указывает внешний вид структурированного тега документа в Java."
type: docs
weight: 599
url: /ru/java/com.aspose.words/sdtappearance/
---

**Inheritance:**
java.lang.Object
```
public class SdtAppearance
```

Указывает внешний вид структурированного тега документа.

 **Examples:** 

Показывает, как отобразить тег вокруг содержимого.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");
 StructuredDocumentTagRangeStart tag = (StructuredDocumentTagRangeStart) doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, true);

 if (tag.getAppearance() == SdtAppearance.HIDDEN)
     tag.setAppearance(SdtAppearance.TAGS);
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [BOUNDING_BOX](#BOUNDING-BOX) | Представляет структурированный тег документа, отображаемый в виде затенённого прямоугольника или ограничивающего блока. |
| [DEFAULT](#DEFAULT) | По умолчанию — [BOUNDING\_BOX](../../com.aspose.words/sdtappearance/\#BOUNDING-BOX). |
| [HIDDEN](#HIDDEN) | Представляет структурированный тег документа, который не отображается. |
| [TAGS](#TAGS) | Представляет структурированный тег документа, отображаемый в виде начального и конечного маркеров. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String sdtAppearanceName)](#fromName-java.lang.String) |  |
| [getName(int sdtAppearance)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sdtAppearance)](#toString-int) |  |
### BOUNDING_BOX {#BOUNDING-BOX}
```
public static int BOUNDING_BOX
```


Представляет структурированный тег документа, отображаемый в виде затенённого прямоугольника или ограничивающего блока.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


По умолчанию — [BOUNDING\_BOX](../../com.aspose.words/sdtappearance/\#BOUNDING-BOX).

### HIDDEN {#HIDDEN}
```
public static int HIDDEN
```


Представляет структурированный тег документа, который не отображается.

### TAGS {#TAGS}
```
public static int TAGS
```


Представляет структурированный тег документа, отображаемый в виде начального и конечного маркеров.

### length {#length}
```
public static int length
```


### fromName(String sdtAppearanceName) {#fromName-java.lang.String}
```
public static int fromName(String sdtAppearanceName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| sdtAppearanceName | java.lang.String |  |

**Returns:**
int
### getName(int sdtAppearance) {#getName-int}
```
public static String getName(int sdtAppearance)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| sdtAppearance | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int sdtAppearance) {#toString-int}
```
public static String toString(int sdtAppearance)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| sdtAppearance | int |  |

**Returns:**
java.lang.String
