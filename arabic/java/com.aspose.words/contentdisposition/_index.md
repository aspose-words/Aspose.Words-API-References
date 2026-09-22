---
title: "ContentDisposition"
linktitle: "ContentDisposition"
second_title: "Aspose.Words لـ Java"
description: "يسرد طرقًا مختلفة لعرض المستند في متصفح العميل باستخدام Java."
type: docs
weight: 126
url: /ar/java/com.aspose.words/contentdisposition/
---

**Inheritance:**
java.lang.Object
```
public class ContentDisposition
```

يسرد طرقًا مختلفة لعرض المستند في متصفح العميل.

 **Remarks:** 

لاحظ أن السلوك الفعلي على متصفح العميل قد يتأثر بإعدادات الأمان للمتصفح.

 **Examples:** 

يوضح كيفية إجراء دمج بريد، ثم حفظ المستند في متصفح العميل.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertField(" MERGEFIELD FullName ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD Company ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD Address ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD City ");

 doc.getMailMerge().execute(new String[]{"FullName", "Company", "Address", "City"},
         new Object[]{"James Bond", "MI5 Headquarters", "Milbank", "London"});
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [ATTACHMENT](#ATTACHMENT) | أرسل المستند إلى المتصفح وقدم خيارًا لحفظ المستند على القرص أو فتحه في التطبيق المرتبط بامتداد المستند. |
| [INLINE](#INLINE) | أرسل المستند إلى المتصفح ويقدم خيارًا لحفظ المستند على القرص أو فتحه داخل المتصفح. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String contentDispositionName)](#fromName-java.lang.String) |  |
| [getName(int contentDisposition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int contentDisposition)](#toString-int) |  |
### ATTACHMENT {#ATTACHMENT}
```
public static int ATTACHMENT
```


أرسل المستند إلى المتصفح وقدم خيارًا لحفظ المستند على القرص أو فتحه في التطبيق المرتبط بامتداد المستند.

### INLINE {#INLINE}
```
public static int INLINE
```


أرسل المستند إلى المتصفح ويقدم خيارًا لحفظ المستند على القرص أو فتحه داخل المتصفح.

### length {#length}
```
public static int length
```


### fromName(String contentDispositionName) {#fromName-java.lang.String}
```
public static int fromName(String contentDispositionName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| contentDispositionName | java.lang.String |  |

**Returns:**
int
### getName(int contentDisposition) {#getName-int}
```
public static String getName(int contentDisposition)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| contentDisposition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int contentDisposition) {#toString-int}
```
public static String toString(int contentDisposition)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| contentDisposition | int |  |

**Returns:**
java.lang.String
