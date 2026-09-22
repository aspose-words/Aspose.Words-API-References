---
title: "RelativeVerticalPosition"
linktitle: "RelativeVerticalPosition"
second_title: "Aspose.Words لـ Java"
description: "يحدد إلى ماذا يكون موضع الشكل أو إطار النص العمودي نسبياً في Java."
type: docs
weight: 563
url: /ar/java/com.aspose.words/relativeverticalposition/
---

**Inheritance:**
java.lang.Object
```
public class RelativeVerticalPosition
```

يحدد إلى ماذا يكون موضع الشكل أو إطار النص العمودي نسبيًا.

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
| [BOTTOM_MARGIN](#BOTTOM-MARGIN) | يحدد أن التموضع العمودي يجب أن يكون نسبياً إلى الهامش السفلي للصفحة الحالية. |
| [INSIDE_MARGIN](#INSIDE-MARGIN) | يحدد أن التموضع العمودي يجب أن يكون نسبياً إلى الهامش الداخلي للصفحة الحالية. |
| [LINE](#LINE) | غير موثق. |
| [MARGIN](#MARGIN) | يحدد أن التموضع العمودي يجب أن يكون نسبياً إلى هوامش الصفحة. |
| [OUTSIDE_MARGIN](#OUTSIDE-MARGIN) | يحدد أن التموضع العمودي يجب أن يكون نسبياً إلى الهامش الخارجي للصفحة الحالية. |
| [PAGE](#PAGE) | الكائن موضعه نسبياً إلى الحافة العلوية للصفحة. |
| [PARAGRAPH](#PARAGRAPH) | الكائن موضعه نسبياً إلى أعلى الفقرة التي تحتوي على المرجع. |
| [TABLE_DEFAULT](#TABLE-DEFAULT) | القيمة الافتراضية هي [MARGIN](../../com.aspose.words/relativeverticalposition/\#MARGIN). |
| [TEXT_FRAME_DEFAULT](#TEXT-FRAME-DEFAULT) | القيمة الافتراضية هي [PARAGRAPH](../../com.aspose.words/relativeverticalposition/\#PARAGRAPH). |
| [TOP_MARGIN](#TOP-MARGIN) | يحدد أن التموضع العمودي يجب أن يكون نسبياً إلى الهامش العلوي للصفحة الحالية. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String relativeVerticalPositionName)](#fromName-java.lang.String) |  |
| [getName(int relativeVerticalPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeVerticalPosition)](#toString-int) |  |
### BOTTOM_MARGIN {#BOTTOM-MARGIN}
```
public static int BOTTOM_MARGIN
```


يحدد أن التموضع العمودي يجب أن يكون نسبياً إلى الهامش السفلي للصفحة الحالية.

### INSIDE_MARGIN {#INSIDE-MARGIN}
```
public static int INSIDE_MARGIN
```


يحدد أن التموضع العمودي يجب أن يكون نسبياً إلى الهامش الداخلي للصفحة الحالية.

### LINE {#LINE}
```
public static int LINE
```


غير موثق.

### MARGIN {#MARGIN}
```
public static int MARGIN
```


يحدد أن التموضع العمودي يجب أن يكون نسبياً إلى هوامش الصفحة.

### OUTSIDE_MARGIN {#OUTSIDE-MARGIN}
```
public static int OUTSIDE_MARGIN
```


يحدد أن التموضع العمودي يجب أن يكون نسبياً إلى الهامش الخارجي للصفحة الحالية.

### PAGE {#PAGE}
```
public static int PAGE
```


الكائن موضعه نسبياً إلى الحافة العلوية للصفحة.

### PARAGRAPH {#PARAGRAPH}
```
public static int PARAGRAPH
```


الكائن موضعه نسبياً إلى أعلى الفقرة التي تحتوي على المرجع.

### TABLE_DEFAULT {#TABLE-DEFAULT}
```
public static int TABLE_DEFAULT
```


القيمة الافتراضية هي [MARGIN](../../com.aspose.words/relativeverticalposition/\#MARGIN).

### TEXT_FRAME_DEFAULT {#TEXT-FRAME-DEFAULT}
```
public static int TEXT_FRAME_DEFAULT
```


القيمة الافتراضية هي [PARAGRAPH](../../com.aspose.words/relativeverticalposition/\#PARAGRAPH).

### TOP_MARGIN {#TOP-MARGIN}
```
public static int TOP_MARGIN
```


يحدد أن التموضع العمودي يجب أن يكون نسبياً إلى الهامش العلوي للصفحة الحالية.

### length {#length}
```
public static int length
```


### fromName(String relativeVerticalPositionName) {#fromName-java.lang.String}
```
public static int fromName(String relativeVerticalPositionName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| relativeVerticalPositionName | java.lang.String |  |

**Returns:**
int
### getName(int relativeVerticalPosition) {#getName-int}
```
public static String getName(int relativeVerticalPosition)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| relativeVerticalPosition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int relativeVerticalPosition) {#toString-int}
```
public static String toString(int relativeVerticalPosition)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| relativeVerticalPosition | int |  |

**Returns:**
java.lang.String
