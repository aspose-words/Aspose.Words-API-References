---
title: "ShapeLineStyle"
linktitle: "ShapeLineStyle"
second_title: "Aspose.Words لـ Java"
description: "يحدد نمط الخط المركب لكائن Shape في Java."
type: docs
weight: 614
url: /ar/java/com.aspose.words/shapelinestyle/
---

**Inheritance:**
java.lang.Object
```
public class ShapeLineStyle
```

يحدد نمط الخط المركب لـ [Shape](../../com.aspose.words/shape/).

 **Examples:** 

يعرض كيفية تغيير خصائص الخط.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 100.0,
         RelativeVerticalPosition.TOP_MARGIN, 100.0, 200.0, 200.0, WrapType.NONE);

 // Basic shapes, such as the rectangle, have two visible parts.
 // 1 -  The fill, which applies to the area within the outline of the shape:
 shape.getFill().setForeColor(Color.WHITE);

 // 2 -  The stroke, which marks the outline of the shape:
 // Modify various properties of this shape's stroke.
 Stroke stroke = shape.getStroke();
 stroke.setOn(true);
 stroke.setWeight(5.0);
 stroke.setColor(Color.RED);
 stroke.setDashStyle(DashStyle.SHORT_DASH_DOT_DOT);
 stroke.setJoinStyle(JoinStyle.MITER);
 stroke.setEndCap(EndCap.SQUARE);
 stroke.setLineStyle(ShapeLineStyle.TRIPLE);
 stroke.getFill().twoColorGradient(Color.RED, Color.BLUE, GradientStyle.VERTICAL, GradientVariant.VARIANT_1);

 doc.save(getArtifactsDir() + "Shape.Stroke.docx");
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [DEFAULT](#DEFAULT) | القيمة الافتراضية هي [SINGLE](../../com.aspose.words/shapelinestyle/\#SINGLE). |
| [DOUBLE](#DOUBLE) | خطوط مزدوجة بعرض متساوٍ. |
| [SINGLE](#SINGLE) | خط واحد. |
| [THICK_THIN](#THICK-THIN) | خطوط مزدوجة، أحدهما سميك والآخر رفيع. |
| [THIN_THICK](#THIN-THICK) | خطوط مزدوجة، أحدها رفيع والآخر سميك. |
| [TRIPLE](#TRIPLE) | ثلاثة خطوط، رفيع، سميك، رفيع. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String shapeLineStyleName)](#fromName-java.lang.String) |  |
| [getName(int shapeLineStyle)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shapeLineStyle)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


القيمة الافتراضية هي [SINGLE](../../com.aspose.words/shapelinestyle/\#SINGLE).

### DOUBLE {#DOUBLE}
```
public static int DOUBLE
```


خطوط مزدوجة بعرض متساوٍ.

### SINGLE {#SINGLE}
```
public static int SINGLE
```


خط واحد.

### THICK_THIN {#THICK-THIN}
```
public static int THICK_THIN
```


خطوط مزدوجة، أحدهما سميك والآخر رفيع.

### THIN_THICK {#THIN-THICK}
```
public static int THIN_THICK
```


خطوط مزدوجة، أحدها رفيع والآخر سميك.

### TRIPLE {#TRIPLE}
```
public static int TRIPLE
```


ثلاثة خطوط، رفيع، سميك، رفيع.

### length {#length}
```
public static int length
```


### fromName(String shapeLineStyleName) {#fromName-java.lang.String}
```
public static int fromName(String shapeLineStyleName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| shapeLineStyleName | java.lang.String |  |

**Returns:**
int
### getName(int shapeLineStyle) {#getName-int}
```
public static String getName(int shapeLineStyle)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| shapeLineStyle | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int shapeLineStyle) {#toString-int}
```
public static String toString(int shapeLineStyle)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| shapeLineStyle | int |  |

**Returns:**
java.lang.String
