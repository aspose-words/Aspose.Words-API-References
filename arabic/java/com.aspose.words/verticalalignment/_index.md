---
title: "VerticalAlignment"
linktitle: "VerticalAlignment"
second_title: "Aspose.Words لـ Java"
description: "يحدد المحاذاة العمودية لإطار نص الشكل العائم أو الجدول العائم في جافا."
type: docs
weight: 713
url: /ar/java/com.aspose.words/verticalalignment/
---

**Inheritance:**
java.lang.Object
```
public class VerticalAlignment
```

يحدد المحاذاة العمودية لشكل عائم أو إطار نص أو جدول عائم.

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
| [BOTTOM](#BOTTOM) | يحدد أن الكائن يجب أن يكون في أسفل قاعدة المحاذاة العمودية. |
| [CENTER](#CENTER) | يحدد أن الكائن يجب أن يكون مركزيًا بالنسبة لقاعدة المحاذاة العمودية. |
| [DEFAULT](#DEFAULT) | نفسه مثل [NONE](../../com.aspose.words/verticalalignment/\#NONE). |
| [INLINE](#INLINE) | غير موثق. |
| [INSIDE](#INSIDE) | يحدد أن الكائن يجب أن يكون داخل قاعدة المحاذاة الأفقية. |
| [NONE](#NONE) | الكائن موضعه صريح، عادةً باستخدام خاصية **Top**. |
| [OUTSIDE](#OUTSIDE) | يحدد أن الكائن يجب أن يكون خارج قاعدة المحاذاة العمودية. |
| [TOP](#TOP) | يحدد أن الكائن يجب أن يكون في أعلى قاعدة المحاذاة العمودية. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String verticalAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int verticalAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int verticalAlignment)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


يحدد أن الكائن يجب أن يكون في أسفل قاعدة المحاذاة العمودية.

### CENTER {#CENTER}
```
public static int CENTER
```


يحدد أن الكائن يجب أن يكون مركزيًا بالنسبة لقاعدة المحاذاة العمودية.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


نفسه مثل [NONE](../../com.aspose.words/verticalalignment/\#NONE).

### INLINE {#INLINE}
```
public static int INLINE
```


غير موثق. يبدو أنه قيمة محتملة للفقرات والجداول العائمة.

### INSIDE {#INSIDE}
```
public static int INSIDE
```


يحدد أن الكائن يجب أن يكون داخل قاعدة المحاذاة الأفقية.

### NONE {#NONE}
```
public static int NONE
```


الكائن موضعه صريح، عادةً باستخدام خاصية **Top**.

### OUTSIDE {#OUTSIDE}
```
public static int OUTSIDE
```


يحدد أن الكائن يجب أن يكون خارج قاعدة المحاذاة العمودية.

### TOP {#TOP}
```
public static int TOP
```


يحدد أن الكائن يجب أن يكون في أعلى قاعدة المحاذاة العمودية.

### length {#length}
```
public static int length
```


### fromName(String verticalAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String verticalAlignmentName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| verticalAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int verticalAlignment) {#getName-int}
```
public static String getName(int verticalAlignment)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| verticalAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int verticalAlignment) {#toString-int}
```
public static String toString(int verticalAlignment)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| verticalAlignment | int |  |

**Returns:**
java.lang.String
