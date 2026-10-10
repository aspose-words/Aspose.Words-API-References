---
title: "DocumentDirection"
linktitle: "DocumentDirection"
second_title: "Aspose.Words для Java"
description: "Позволяет указать направление потока текста в документе в Java."
type: docs
weight: 165
url: /ru/java/com.aspose.words/documentdirection/
---

**Inheritance:**
java.lang.Object
```
public class DocumentDirection
```

Позволяет указать направление потока текста в документе.

 **Examples:** 

Показывает, как определить направление текста в простом документе.

```

 // Create a "TxtLoadOptions" object, which we can pass to a document's constructor
 // to modify how we load a plaintext document.
 TxtLoadOptions loadOptions = new TxtLoadOptions();

 // Set the "DocumentDirection" property to "DocumentDirection.Auto" automatically detects
 // the direction of every paragraph of text that Aspose.Words loads from plaintext.
 // Each paragraph's "Bidi" property will store its direction.
 loadOptions.setDocumentDirection(DocumentDirection.AUTO);

 // Detect Hebrew text as right-to-left.
 Document doc = new Document(getMyDir() + "Hebrew text.txt", loadOptions);

 Assert.assertTrue(doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBidi());

 // Detect English text as right-to-left.
 doc = new Document(getMyDir() + "English text.txt", loadOptions);

 Assert.assertFalse(doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBidi());
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [AUTO](#AUTO) | Автоматическое определение направления. |
| [LEFT_TO_RIGHT](#LEFT-TO-RIGHT) | Направление слева направо. |
| [RIGHT_TO_LEFT](#RIGHT-TO-LEFT) | Направление справа налево. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String documentDirectionName)](#fromName-java.lang.String) |  |
| [getName(int documentDirection)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int documentDirection)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Автоматическое определение направления.

 **Remarks:** 

Когда эта опция выбрана и текст содержит символы, принадлежащие RTL‑скриптам, направление документа будет автоматически установлено в RTL.

### LEFT_TO_RIGHT {#LEFT-TO-RIGHT}
```
public static int LEFT_TO_RIGHT
```


Направление слева направо.

### RIGHT_TO_LEFT {#RIGHT-TO-LEFT}
```
public static int RIGHT_TO_LEFT
```


Направление справа налево.

### length {#length}
```
public static int length
```


### fromName(String documentDirectionName) {#fromName-java.lang.String}
```
public static int fromName(String documentDirectionName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| documentDirectionName | java.lang.String |  |

**Returns:**
int
### getName(int documentDirection) {#getName-int}
```
public static String getName(int documentDirection)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| documentDirection | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int documentDirection) {#toString-int}
```
public static String toString(int documentDirection)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| documentDirection | int |  |

**Returns:**
java.lang.String
