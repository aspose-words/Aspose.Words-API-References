---
title: "DocumentRecoveryMode"
linktitle: "DocumentRecoveryMode"
second_title: "Aspose.Words لـ Java"
description: "يحدد خيارات الاستعادة المتاحة عندما يواجه المستند أخطاءً أثناء التحميل في Java."
type: docs
weight: 171
url: /ar/java/com.aspose.words/documentrecoverymode/
---

**Inheritance:**
java.lang.Object
```
public class DocumentRecoveryMode
```

يحدد خيارات الاستعادة المتاحة عندما يواجه المستند أخطاءً أثناء التحميل.

 **Examples:** 

يوضح كيفية محاولة استعادة مستند إذا حدثت أخطاء أثناء التحميل.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setRecoveryMode(DocumentRecoveryMode.TRY_RECOVER);

 Document doc = new Document(getMyDir() + "Corrupted footnotes.docx", loadOptions);
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [NONE](#NONE) | لم يتم محاولة الاستعادة. |
| [TRY_RECOVER](#TRY-RECOVER) | محاولة استعادة المستند مع الحفاظ على أكبر قدر ممكن من البيانات. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String documentRecoveryModeName)](#fromName-java.lang.String) |  |
| [getName(int documentRecoveryMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int documentRecoveryMode)](#toString-int) |  |
### NONE {#NONE}
```
public static int NONE
```


لم يتم محاولة الاستعادة. إذا كان المستند غير صالح، سيفشل التحميل مع حدوث خطأ.

### TRY_RECOVER {#TRY-RECOVER}
```
public static int TRY_RECOVER
```


محاولة استعادة المستند مع الحفاظ على أكبر قدر ممكن من البيانات.

### length {#length}
```
public static int length
```


### fromName(String documentRecoveryModeName) {#fromName-java.lang.String}
```
public static int fromName(String documentRecoveryModeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| documentRecoveryModeName | java.lang.String |  |

**Returns:**
int
### getName(int documentRecoveryMode) {#getName-int}
```
public static String getName(int documentRecoveryMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| documentRecoveryMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int documentRecoveryMode) {#toString-int}
```
public static String toString(int documentRecoveryMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| documentRecoveryMode | int |  |

**Returns:**
java.lang.String
