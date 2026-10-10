---
title: "HtmlControlType"
linktitle: "HtmlControlType"
second_title: "Aspose.Words для Java"
description: "Тип узлов документа, представляющих  и  элементы, импортированные из HTML в Java."
type: docs
weight: 377
url: /ru/java/com.aspose.words/htmlcontroltype/
---

**Inheritance:**
java.lang.Object
```
public class HtmlControlType
```

Тип узлов документа, представляющих  и  элементы, импортированные из HTML. Примеры:Показано, как установить предпочтительный тип узлов документа, который будет представлять импортированные  и  элементы.   final String html = "\\r\\n\\r\\n\\r\\n" + "item1\\r\\n\\r\\n\\r\\n\\r\\n"; HtmlLoadOptions htmlLoadOptions = new HtmlLoadOptions(); htmlLoadOptions.setPreferredControlType(HtmlControlType.STRUCTURED\_DOCUMENT\_TAG); Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF\_8)), htmlLoadOptions); NodeCollection nodes = doc.getChildNodes(NodeType.STRUCTURED\_DOCUMENT\_TAG, true); StructuredDocumentTag tag = (StructuredDocumentTag) nodes.get(0);
## Поля

| Поле | Описание |
| --- | --- |
| [FORM_FIELD](#FORM-FIELD) | Поле формы. |
| [STRUCTURED_DOCUMENT_TAG](#STRUCTURED-DOCUMENT-TAG) | Тег структурированного документа |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String htmlControlTypeName)](#fromName-java.lang.String) |  |
| [getName(int htmlControlType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int htmlControlType)](#toString-int) |  |
### FORM_FIELD {#FORM-FIELD}
```
public static int FORM_FIELD
```


Поле формы.

### STRUCTURED_DOCUMENT_TAG {#STRUCTURED-DOCUMENT-TAG}
```
public static int STRUCTURED_DOCUMENT_TAG
```


Тег структурированного документа

### length {#length}
```
public static int length
```


### fromName(String htmlControlTypeName) {#fromName-java.lang.String}
```
public static int fromName(String htmlControlTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| htmlControlTypeName | java.lang.String |  |

**Returns:**
int
### getName(int htmlControlType) {#getName-int}
```
public static String getName(int htmlControlType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| htmlControlType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int htmlControlType) {#toString-int}
```
public static String toString(int htmlControlType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| htmlControlType | int |  |

**Returns:**
java.lang.String
