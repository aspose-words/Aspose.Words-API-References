---
title: "BorderType"
linktitle: "BorderType"
second_title: "Aspose.Words لـ Java"
description: "يحدد جوانب الحد في Java."
type: docs
weight: 48
url: /ar/java/com.aspose.words/bordertype/
---

**Inheritance:**
java.lang.Object
```
public class BorderType
```

يحدد جوانب الحد.

لمزيد من المعلومات، زر مقالة الوثائق [ Programming with Documents ][Programming with Documents].

 **Examples:** 

يظهر كيفية إدراج فقرة بحد أعلى.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Border topBorder = builder.getParagraphFormat().getBorders().getByBorderType(BorderType.TOP);
 topBorder.setLineWidth(4.0d);
 topBorder.setLineStyle(LineStyle.DASH_SMALL_GAP);
 // Set ThemeColor only when LineWidth or LineStyle setted.
 topBorder.setThemeColor(ThemeColor.ACCENT_1);
 topBorder.setTintAndShade(0.25d);

 builder.writeln("Text with a top border.");

 doc.save(getArtifactsDir() + "Border.ParagraphTopBorder.docx");
 
```


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## الحقول

| حقل | الوصف |
| --- | --- |
| [BOTTOM](#BOTTOM) | يحدد الحد السفلي لفقرة أو خلية جدول. |
| [DIAGONAL_DOWN](#DIAGONAL-DOWN) | يحدد الحد القطري في خلية جدول. |
| [DIAGONAL_UP](#DIAGONAL-UP) | يحدد الحد القطري في خلية جدول. |
| [HORIZONTAL](#HORIZONTAL) | يحدد الحد الأفقي بين الخلايا في جدول أو بين الفقرات المتطابقة. |
| [LEFT](#LEFT) | يحدد الحد الأيسر لفقرة أو خلية جدول. |
| [NONE](#NONE) | القيمة الافتراضية. |
| [RIGHT](#RIGHT) | يحدد الحد الأيمن لفقرة أو خلية جدول. |
| [TOP](#TOP) | يحدد الحد العلوي لفقرة أو خلية جدول. |
| [VERTICAL](#VERTICAL) | يحدد الحد العمودي بين الخلايا في جدول. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String borderTypeName)](#fromName-java.lang.String) |  |
| [getName(int borderType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int borderType)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


يحدد الحد السفلي لفقرة أو خلية جدول.

### DIAGONAL_DOWN {#DIAGONAL-DOWN}
```
public static int DIAGONAL_DOWN
```


يحدد الحد القطري في خلية جدول.

### DIAGONAL_UP {#DIAGONAL-UP}
```
public static int DIAGONAL_UP
```


يحدد الحد القطري في خلية جدول.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


يحدد الحد الأفقي بين الخلايا في جدول أو بين الفقرات المتطابقة.

### LEFT {#LEFT}
```
public static int LEFT
```


يحدد الحد الأيسر لفقرة أو خلية جدول.

### NONE {#NONE}
```
public static int NONE
```


القيمة الافتراضية.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


يحدد الحد الأيمن لفقرة أو خلية جدول.

### TOP {#TOP}
```
public static int TOP
```


يحدد الحد العلوي لفقرة أو خلية جدول.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


يحدد الحد العمودي بين الخلايا في جدول.

### length {#length}
```
public static int length
```


### fromName(String borderTypeName) {#fromName-java.lang.String}
```
public static int fromName(String borderTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| borderTypeName | java.lang.String |  |

**Returns:**
int
### getName(int borderType) {#getName-int}
```
public static String getName(int borderType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| borderType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int borderType) {#toString-int}
```
public static String toString(int borderType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| borderType | int |  |

**Returns:**
java.lang.String
