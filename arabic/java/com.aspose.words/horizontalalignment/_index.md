---
title: "HorizontalAlignment"
linktitle: "HorizontalAlignment"
second_title: "Aspose.Words لـ Java"
description: "يحدد المحاذاة الأفقية لإطار نص الشكل العائم أو الجدول العائم في Java."
type: docs
weight: 374
url: /ar/java/com.aspose.words/horizontalalignment/
---

**Inheritance:**
java.lang.Object
```
public class HorizontalAlignment
```

يحدد المحاذاة الأفقية لشكل عائم أو إطار نص أو جدول عائم.

 **Examples:** 

يوضح كيفية إدراج صورة عائمة في مركز الصفحة.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a floating image that will appear behind the overlapping text and align it to the page's center.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setHorizontalAlignment(HorizontalAlignment.CENTER);
 shape.setVerticalAlignment(VerticalAlignment.CENTER);

 doc.save(getArtifactsDir() + "Image.CreateFloatingPageCenter.docx");
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [CENTER](#CENTER) | يحدد أن الكائن يجب أن يكون مركزيًا بالنسبة لقاعدة المحاذاة الأفقية. |
| [DEFAULT](#DEFAULT) | نفس [NONE](../../com.aspose.words/horizontalalignment/\#NONE). |
| [INSIDE](#INSIDE) | يحدد أن الكائن يجب أن يكون داخل قاعدة المحاذاة الأفقية. |
| [LEFT](#LEFT) | يحدد أن الكائن يجب أن يكون محاذيًا إلى اليسار لقاعدة المحاذاة الأفقية. |
| [NONE](#NONE) | الكائن موضعه صريحًا، عادةً باستخدام خاصية **Left**. |
| [OUTSIDE](#OUTSIDE) | يحدد أن الكائن يجب أن يكون خارج قاعدة المحاذاة الأفقية. |
| [RIGHT](#RIGHT) | يحدد أن الكائن يجب أن يكون محاذيًا إلى اليمين لقاعدة المحاذاة الأفقية. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String horizontalAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int horizontalAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int horizontalAlignment)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


يحدد أن الكائن يجب أن يكون مركزيًا بالنسبة لقاعدة المحاذاة الأفقية.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


نفس [NONE](../../com.aspose.words/horizontalalignment/\#NONE).

### INSIDE {#INSIDE}
```
public static int INSIDE
```


يحدد أن الكائن يجب أن يكون داخل قاعدة المحاذاة الأفقية.

### LEFT {#LEFT}
```
public static int LEFT
```


يحدد أن الكائن يجب أن يكون محاذيًا إلى اليسار لقاعدة المحاذاة الأفقية.

### NONE {#NONE}
```
public static int NONE
```


الكائن موضعه صريحًا، عادةً باستخدام خاصية **Left**.

### OUTSIDE {#OUTSIDE}
```
public static int OUTSIDE
```


يحدد أن الكائن يجب أن يكون خارج قاعدة المحاذاة الأفقية.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


يحدد أن الكائن يجب أن يكون محاذيًا إلى اليمين لقاعدة المحاذاة الأفقية.

### length {#length}
```
public static int length
```


### fromName(String horizontalAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String horizontalAlignmentName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| horizontalAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int horizontalAlignment) {#getName-int}
```
public static String getName(int horizontalAlignment)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| horizontalAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int horizontalAlignment) {#toString-int}
```
public static String toString(int horizontalAlignment)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| horizontalAlignment | int |  |

**Returns:**
java.lang.String
