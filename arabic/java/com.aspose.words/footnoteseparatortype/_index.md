---
title: "FootnoteSeparatorType"
linktitle: "FootnoteSeparatorType"
second_title: "Aspose.Words لـ Java"
description: "يحدد نوع فاصل الحاشية السفلية/الحاشية العلوية في جافا."
type: docs
weight: 345
url: /ar/java/com.aspose.words/footnoteseparatortype/
---

**Inheritance:**
java.lang.Object
```
public class FootnoteSeparatorType
```

يحدد نوع فاصل الحاشية السفلية/الحاشية العلوية.

 **Examples:** 

يوضح كيفية إزالة فاصل الحاشية العلوية.

```

 Document doc = new Document(getMyDir() + "Footnotes and endnotes.docx");

 FootnoteSeparator endnoteSeparator = doc.getFootnoteSeparators().getByFootnoteSeparatorType(FootnoteSeparatorType.ENDNOTE_SEPARATOR);
 // Remove endnote separator.
 endnoteSeparator.getFirstParagraph().getFirstChild().remove();
 
```

يوضح كيفية إدارة تنسيق فاصل الحاشية.

```

 Document doc = new Document(getMyDir() + "Footnotes and endnotes.docx");

 FootnoteSeparator footnoteSeparator = doc.getFootnoteSeparators().getByFootnoteSeparatorType(FootnoteSeparatorType.FOOTNOTE_SEPARATOR);
 // Align footnote separator.
 footnoteSeparator.getFirstParagraph().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [ENDNOTE_CONTINUATION_NOTICE](#ENDNOTE-CONTINUATION-NOTICE) | يطبع أسفل نص الحاشية العلوية على الصفحة عندما يجب أن يستمر نص الحاشية العلوية في الصفحة التالية. |
| [ENDNOTE_CONTINUATION_SEPARATOR](#ENDNOTE-CONTINUATION-SEPARATOR) | يطبع فوق نص الحاشية العلوية على الصفحة عندما يجب أن يستمر النص من صفحة سابقة. |
| [ENDNOTE_SEPARATOR](#ENDNOTE-SEPARATOR) | فاصل بين النص الرئيسي ونص الحاشية العلوية. |
| [FOOTNOTE_CONTINUATION_NOTICE](#FOOTNOTE-CONTINUATION-NOTICE) | يطبع أسفل نص الحاشية السفلية على الصفحة عندما يجب أن يستمر نص الحاشية السفلية في الصفحة التالية. |
| [FOOTNOTE_CONTINUATION_SEPARATOR](#FOOTNOTE-CONTINUATION-SEPARATOR) | يطبع فوق نص الحاشية السفلية على الصفحة عندما يجب أن يستمر النص من صفحة سابقة. |
| [FOOTNOTE_SEPARATOR](#FOOTNOTE-SEPARATOR) | فاصل بين النص الرئيسي ونص الحاشية السفلية. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String footnoteSeparatorTypeName)](#fromName-java.lang.String) |  |
| [getName(int footnoteSeparatorType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int footnoteSeparatorType)](#toString-int) |  |
### ENDNOTE_CONTINUATION_NOTICE {#ENDNOTE-CONTINUATION-NOTICE}
```
public static int ENDNOTE_CONTINUATION_NOTICE
```


يطبع أسفل نص الحاشية العلوية على الصفحة عندما يجب أن يستمر نص الحاشية العلوية في الصفحة التالية.

### ENDNOTE_CONTINUATION_SEPARATOR {#ENDNOTE-CONTINUATION-SEPARATOR}
```
public static int ENDNOTE_CONTINUATION_SEPARATOR
```


يطبع فوق نص الحاشية العلوية على الصفحة عندما يجب أن يستمر النص من صفحة سابقة.

### ENDNOTE_SEPARATOR {#ENDNOTE-SEPARATOR}
```
public static int ENDNOTE_SEPARATOR
```


فاصل بين النص الرئيسي ونص الحاشية العلوية.

### FOOTNOTE_CONTINUATION_NOTICE {#FOOTNOTE-CONTINUATION-NOTICE}
```
public static int FOOTNOTE_CONTINUATION_NOTICE
```


يطبع أسفل نص الحاشية السفلية على الصفحة عندما يجب أن يستمر نص الحاشية السفلية في الصفحة التالية.

### FOOTNOTE_CONTINUATION_SEPARATOR {#FOOTNOTE-CONTINUATION-SEPARATOR}
```
public static int FOOTNOTE_CONTINUATION_SEPARATOR
```


يطبع فوق نص الحاشية السفلية على الصفحة عندما يجب أن يستمر النص من صفحة سابقة.

### FOOTNOTE_SEPARATOR {#FOOTNOTE-SEPARATOR}
```
public static int FOOTNOTE_SEPARATOR
```


فاصل بين النص الرئيسي ونص الحاشية السفلية.

### length {#length}
```
public static int length
```


### fromName(String footnoteSeparatorTypeName) {#fromName-java.lang.String}
```
public static int fromName(String footnoteSeparatorTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| footnoteSeparatorTypeName | java.lang.String |  |

**Returns:**
int
### getName(int footnoteSeparatorType) {#getName-int}
```
public static String getName(int footnoteSeparatorType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| footnoteSeparatorType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int footnoteSeparatorType) {#toString-int}
```
public static String toString(int footnoteSeparatorType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| footnoteSeparatorType | int |  |

**Returns:**
java.lang.String
