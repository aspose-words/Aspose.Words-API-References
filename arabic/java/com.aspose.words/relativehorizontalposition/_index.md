---
title: "RelativeHorizontalPosition"
linktitle: "RelativeHorizontalPosition"
second_title: "Aspose.Words لـ Java"
description: "يحدد إلى أي شيء يكون الموضع الأفقي لشكل أو إطار نصي نسبيًا في Java."
type: docs
weight: 561
url: /ar/java/com.aspose.words/relativehorizontalposition/
---

**Inheritance:**
java.lang.Object
```
public class RelativeHorizontalPosition
```

يحدد إلى ماذا يكون موضع الشكل أو إطار النص الأفقي نسبيًا.

 **Examples:** 

يوضح كيفية إدراج صورة واستخدامها كعلامة مائية.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert the image into the header so that it will be visible on every page.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 Shape shape = builder.insertImage(getImageDir() + "Transparent background logo.png");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);

 // Place the image at the center of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setLeft((builder.getPageSetup().getPageWidth() - shape.getWidth()) / 2.0);
 shape.setTop((builder.getPageSetup().getPageHeight() - shape.getHeight()) / 2.0);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertWatermark.docx");
 
```

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
| [CHARACTER](#CHARACTER) | الكائن موضعه نسبيًا إلى الجانب الأيسر من الفقرة. |
| [COLUMN](#COLUMN) | الكائن موضعه نسبيًا إلى الجانب الأيسر من العمود. |
| [DEFAULT](#DEFAULT) | القيمة الافتراضية هي [COLUMN](../../com.aspose.words/relativehorizontalposition/\#COLUMN). |
| [INSIDE_MARGIN](#INSIDE-MARGIN) | يحدد أن التموضع الأفقي يجب أن يكون نسبيًا إلى الهامش الداخلي للصفحة الحالية (الهامش الأيسر في الصفحات الفردية، واليمين في الصفحات الزوجية). |
| [LEFT_MARGIN](#LEFT-MARGIN) | يحدد أن التموضع الأفقي يجب أن يكون نسبيًا إلى الهامش الأيسر للصفحة. |
| [MARGIN](#MARGIN) | يحدد أن التموضع الأفقي يجب أن يكون نسبيًا إلى هوامش الصفحة. |
| [OUTSIDE_MARGIN](#OUTSIDE-MARGIN) | يحدد أن التموضع الأفقي يجب أن يكون نسبيًا إلى الهامش الخارجي للصفحة الحالية (الهامش الأيمن في الصفحات الفردية، واليسار في الصفحات الزوجية). |
| [PAGE](#PAGE) | الكائن موضعه نسبيًا إلى الحافة اليسرى للصفحة. |
| [RIGHT_MARGIN](#RIGHT-MARGIN) | يحدد أن التموضع الأفقي يجب أن يكون نسبيًا إلى الهامش الأيمن للصفحة. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String relativeHorizontalPositionName)](#fromName-java.lang.String) |  |
| [getName(int relativeHorizontalPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeHorizontalPosition)](#toString-int) |  |
### CHARACTER {#CHARACTER}
```
public static int CHARACTER
```


الكائن موضعه نسبيًا إلى الجانب الأيسر من الفقرة.

### COLUMN {#COLUMN}
```
public static int COLUMN
```


الكائن موضعه نسبيًا إلى الجانب الأيسر من العمود.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


القيمة الافتراضية هي [COLUMN](../../com.aspose.words/relativehorizontalposition/\#COLUMN).

### INSIDE_MARGIN {#INSIDE-MARGIN}
```
public static int INSIDE_MARGIN
```


يحدد أن التموضع الأفقي يجب أن يكون نسبيًا إلى الهامش الداخلي للصفحة الحالية (الهامش الأيسر في الصفحات الفردية، واليمين في الصفحات الزوجية).

### LEFT_MARGIN {#LEFT-MARGIN}
```
public static int LEFT_MARGIN
```


يحدد أن التموضع الأفقي يجب أن يكون نسبيًا إلى الهامش الأيسر للصفحة.

### MARGIN {#MARGIN}
```
public static int MARGIN
```


يحدد أن التموضع الأفقي يجب أن يكون نسبيًا إلى هوامش الصفحة.

### OUTSIDE_MARGIN {#OUTSIDE-MARGIN}
```
public static int OUTSIDE_MARGIN
```


يحدد أن التموضع الأفقي يجب أن يكون نسبيًا إلى الهامش الخارجي للصفحة الحالية (الهامش الأيمن في الصفحات الفردية، واليسار في الصفحات الزوجية).

### PAGE {#PAGE}
```
public static int PAGE
```


الكائن موضعه نسبيًا إلى الحافة اليسرى للصفحة.

### RIGHT_MARGIN {#RIGHT-MARGIN}
```
public static int RIGHT_MARGIN
```


يحدد أن التموضع الأفقي يجب أن يكون نسبيًا إلى الهامش الأيمن للصفحة.

### length {#length}
```
public static int length
```


### fromName(String relativeHorizontalPositionName) {#fromName-java.lang.String}
```
public static int fromName(String relativeHorizontalPositionName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| relativeHorizontalPositionName | java.lang.String |  |

**Returns:**
int
### getName(int relativeHorizontalPosition) {#getName-int}
```
public static String getName(int relativeHorizontalPosition)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| relativeHorizontalPosition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int relativeHorizontalPosition) {#toString-int}
```
public static String toString(int relativeHorizontalPosition)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| relativeHorizontalPosition | int |  |

**Returns:**
java.lang.String
