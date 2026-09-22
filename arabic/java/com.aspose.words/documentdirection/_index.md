---
title: "DocumentDirection"
linktitle: "DocumentDirection"
second_title: "Aspose.Words لـ Java"
description: "يسمح بتحديد اتجاه تدفق النص في مستند في Java."
type: docs
weight: 165
url: /ar/java/com.aspose.words/documentdirection/
---

**Inheritance:**
java.lang.Object
```
public class DocumentDirection
```

يسمح بتحديد اتجاه تدفق النص في المستند.

 **Examples:** 

يوضح كيفية اكتشاف اتجاه نص المستند النصي العادي.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [AUTO](#AUTO) | اكتشاف الاتجاه تلقائيًا. |
| [LEFT_TO_RIGHT](#LEFT-TO-RIGHT) | اتجاه من اليسار إلى اليمين. |
| [RIGHT_TO_LEFT](#RIGHT-TO-LEFT) | اتجاه من اليمين إلى اليسار. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String documentDirectionName)](#fromName-java.lang.String) |  |
| [getName(int documentDirection)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int documentDirection)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


اكتشاف الاتجاه تلقائيًا.

 **Remarks:** 

عند اختيار هذا الخيار ووجود نص يحتوي على أحرف تنتمي إلى سكريبتات من اليمين إلى اليسار، سيتم ضبط اتجاه المستند تلقائيًا إلى اليمين إلى اليسار.

### LEFT_TO_RIGHT {#LEFT-TO-RIGHT}
```
public static int LEFT_TO_RIGHT
```


اتجاه من اليسار إلى اليمين.

### RIGHT_TO_LEFT {#RIGHT-TO-LEFT}
```
public static int RIGHT_TO_LEFT
```


اتجاه من اليمين إلى اليسار.

### length {#length}
```
public static int length
```


### fromName(String documentDirectionName) {#fromName-java.lang.String}
```
public static int fromName(String documentDirectionName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| documentDirectionName | java.lang.String |  |

**Returns:**
int
### getName(int documentDirection) {#getName-int}
```
public static String getName(int documentDirection)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| documentDirection | int |  |

**Returns:**
java.lang.String
