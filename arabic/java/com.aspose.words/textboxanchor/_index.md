---
title: "TextBoxAnchor"
linktitle: "TextBoxAnchor"
second_title: "Aspose.Words لـ Java"
description: "يحدد القيم المستخدمة لمحاذاة النص العمودي للشكل في Java."
type: docs
weight: 667
url: /ar/java/com.aspose.words/textboxanchor/
---

**Inheritance:**
java.lang.Object
```
public class TextBoxAnchor
```

يحدد القيم المستخدمة لمحاذاة النص العمودية داخل الشكل.

 **Examples:** 

يوضح كيفية محاذاة محتوى النص عموديًا داخل مربع النص.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.TEXT_BOX, 200.0, 200.0);

 // Set the "VerticalAnchor" property to "TextBoxAnchor.Top" to
 // align the text in this text box with the top side of the shape.
 // Set the "VerticalAnchor" property to "TextBoxAnchor.Middle" to
 // align the text in this text box to the center of the shape.
 // Set the "VerticalAnchor" property to "TextBoxAnchor.Bottom" to
 // align the text in this text box to the bottom of the shape.
 shape.getTextBox().setVerticalAnchor(verticalAnchor);

 builder.moveTo(shape.getFirstParagraph());
 builder.write("Hello world!");

 // The vertical aligning of text inside text boxes is available from Microsoft Word 2007 onwards.
 doc.getCompatibilityOptions().optimizeFor(MsWordVersion.WORD_2007);
 doc.save(getArtifactsDir() + "Shape.VerticalAnchor.docx");
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [BOTTOM](#BOTTOM) | النص محاذى إلى أسفل مربع النص. |
| [BOTTOM_BASELINE](#BOTTOM-BASELINE) | النص محاذى إلى الخط الأساسي السفلي لمربع النص. |
| [BOTTOM_CENTERED](#BOTTOM-CENTERED) | النص محاذى إلى أسفل مركز مربع النص. |
| [BOTTOM_CENTERED_BASELINE](#BOTTOM-CENTERED-BASELINE) | النص محاذى إلى الخط الأساسي السفلي المركزي لمربع النص. |
| [MIDDLE](#MIDDLE) | النص محاذى إلى وسط مربع النص. |
| [MIDDLE_CENTERED](#MIDDLE-CENTERED) | النص محاذى إلى وسط مركز مربع النص. |
| [TOP](#TOP) | النص محاذى إلى أعلى مربع النص. |
| [TOP_BASELINE](#TOP-BASELINE) | النص محاذى إلى الخط الأساسي العلوي لمربع النص. |
| [TOP_CENTERED](#TOP-CENTERED) | النص محاذى إلى أعلى مركز مربع النص. |
| [TOP_CENTERED_BASELINE](#TOP-CENTERED-BASELINE) | النص محاذى إلى الخط الأساسي العلوي المركزي لمربع النص. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String textBoxAnchorName)](#fromName-java.lang.String) |  |
| [getName(int textBoxAnchor)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textBoxAnchor)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


النص محاذى إلى أسفل مربع النص.

### BOTTOM_BASELINE {#BOTTOM-BASELINE}
```
public static int BOTTOM_BASELINE
```


النص محاذى إلى الخط الأساسي السفلي لمربع النص.

### BOTTOM_CENTERED {#BOTTOM-CENTERED}
```
public static int BOTTOM_CENTERED
```


النص محاذى إلى أسفل مركز مربع النص.

### BOTTOM_CENTERED_BASELINE {#BOTTOM-CENTERED-BASELINE}
```
public static int BOTTOM_CENTERED_BASELINE
```


النص محاذى إلى الخط الأساسي السفلي المركزي لمربع النص.

### MIDDLE {#MIDDLE}
```
public static int MIDDLE
```


النص محاذى إلى وسط مربع النص.

### MIDDLE_CENTERED {#MIDDLE-CENTERED}
```
public static int MIDDLE_CENTERED
```


النص محاذى إلى وسط مركز مربع النص.

### TOP {#TOP}
```
public static int TOP
```


النص محاذى إلى أعلى مربع النص.

### TOP_BASELINE {#TOP-BASELINE}
```
public static int TOP_BASELINE
```


النص محاذى إلى الخط الأساسي العلوي لمربع النص.

### TOP_CENTERED {#TOP-CENTERED}
```
public static int TOP_CENTERED
```


النص محاذى إلى أعلى مركز مربع النص.

### TOP_CENTERED_BASELINE {#TOP-CENTERED-BASELINE}
```
public static int TOP_CENTERED_BASELINE
```


النص محاذى إلى الخط الأساسي العلوي المركزي لمربع النص.

### length {#length}
```
public static int length
```


### fromName(String textBoxAnchorName) {#fromName-java.lang.String}
```
public static int fromName(String textBoxAnchorName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| textBoxAnchorName | java.lang.String |  |

**Returns:**
int
### getName(int textBoxAnchor) {#getName-int}
```
public static String getName(int textBoxAnchor)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| textBoxAnchor | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int textBoxAnchor) {#toString-int}
```
public static String toString(int textBoxAnchor)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| textBoxAnchor | int |  |

**Returns:**
java.lang.String
