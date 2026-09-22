---
title: "ShadowFormat"
linktitle: "ShadowFormat"
second_title: "Aspose.Words لـ Java"
description: "يمثل تنسيق الظل لكائن في Java."
type: docs
weight: 610
url: /ar/java/com.aspose.words/shadowformat/
---

**Inheritance:**
java.lang.Object
```
public class ShadowFormat
```

يمثل تنسيق الظل لكائن.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Graphic Elements ][Working with Graphic Elements].

 **Examples:** 

يظهر كيفية الحصول على لون الظل.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```


[Working with Graphic Elements]: https://docs.aspose.com/words/java/working-with-graphic-elements/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [clear()](#clear) | يمسح تنسيق الظل. |
| [getColor()](#getColor) | يحصل على كائن java.awt.Color الذي يمثل لون الظل. |
| [getTransparency()](#getTransparency) | يحصل على درجة الشفافية لتأثير الظل كقيمة بين 0.0 (معتم) و 1.0 (شفاف). |
| [getType()](#getType) | يحصل على [ShadowType](../../com.aspose.words/shadowtype/) المحدد لـ ShadowFormat. |
| [getVisible()](#getVisible) | يرجع  true  إذا كان التنسيق المطبق على هذه الحالة مرئيًا. |
| [setColor(Color value)](#setColor-java.awt.Color) | يضبط كائن java.awt.Color الذي يمثل اللون للظل. |
| [setTransparency(double value)](#setTransparency-double) | يضبط درجة الشفافية لتأثير الظل كقيمة بين 0.0 (معتم) و 1.0 (شفاف). |
| [setType(int value)](#setType-int) | يضبط [ShadowType](../../com.aspose.words/shadowtype/) المحدد لـ ShadowFormat. |
### clear() {#clear}
```
public void clear()
```


يمسح تنسيق الظل.

 **Examples:** 

يظهر كيفية العمل مع تنسيق الظل للشكل.

```

 Document doc = new Document(getMyDir() + "Shape stroke pattern border.docx");
 Shape shape = (Shape)doc.getChildNodes(NodeType.SHAPE, true).get(0);

 if (shape.getShadowFormat().getVisible() && shape.getShadowFormat().getType() == ShadowType.SHADOW_2)
     shape.getShadowFormat().setType(ShadowType.SHADOW_7);

 if (shape.getShadowFormat().getType() == ShadowType.SHADOW_MIXED)
     shape.getShadowFormat().clear();
 
```

### getColor() {#getColor}
```
public Color getColor()
```


يحصل على كائن java.awt.Color الذي يمثل اللون للظل. القيمة الافتراضية هي java.awt.Color\#getBlack().getBlack().

 **Examples:** 

يظهر كيفية الحصول على لون الظل.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

يعرض كيفية ضبط لون مع الشفافية.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 ShadowFormat shadowFormat = shape.getShadowFormat();
 shadowFormat.setType(ShadowType.SHADOW_21);
 shadowFormat.setColor(Color.RED);
 shadowFormat.setTransparency(0.8);

 doc.save(getArtifactsDir() + "Shape.ShadowFormatTransparency.docx");
 
```

**Returns:**
java.awt.Color - كائن java.awt.Color يمثل اللون للظل.
### getTransparency() {#getTransparency}
```
public double getTransparency()
```


يحصل على درجة الشفافية لتأثير الظل كقيمة بين 0.0 (معتم) و 1.0 (شفاف). القيمة الافتراضية هي 0.0.

 **Examples:** 

يعرض كيفية ضبط لون مع الشفافية.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 ShadowFormat shadowFormat = shape.getShadowFormat();
 shadowFormat.setType(ShadowType.SHADOW_21);
 shadowFormat.setColor(Color.RED);
 shadowFormat.setTransparency(0.8);

 doc.save(getArtifactsDir() + "Shape.ShadowFormatTransparency.docx");
 
```

**Returns:**
double - درجة الشفافية لتأثير الظل كقيمة بين 0.0 (معتم) و 1.0 (شفاف).
### getType() {#getType}
```
public int getType()
```


يحصل على [ShadowType](../../com.aspose.words/shadowtype/) المحدد لـ ShadowFormat.

 **Remarks:** 

ضبط نوع ظل جديد سيعيد تعيين قيم اللون والشفافية إلى القيم الافتراضية. لذلك، من المنطقي أولاً ضبط نوع الظل المطلوب ثم قيم اللون والشفافية.

 **Examples:** 

يظهر كيفية الحصول على لون الظل.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

**Returns:**
int - [ShadowType](../../com.aspose.words/shadowtype/) المحدد لـ ShadowFormat. القيمة المرجعة هي واحدة من ثوابت [ShadowType](../../com.aspose.words/shadowtype/).
### getVisible() {#getVisible}
```
public boolean getVisible()
```


يرجع  true  إذا كان التنسيق المطبق على هذه الحالة مرئيًا.

 **Remarks:** 

على عكس [clear()](../../com.aspose.words/shadowformat/\#clear)، تعيين  false  إلى Visible لا يزيل التنسيق، بل يخفى تأثير الشكل فقط.

 **Examples:** 

يظهر كيفية العمل مع تنسيق الظل للشكل.

```

 Document doc = new Document(getMyDir() + "Shape stroke pattern border.docx");
 Shape shape = (Shape)doc.getChildNodes(NodeType.SHAPE, true).get(0);

 if (shape.getShadowFormat().getVisible() && shape.getShadowFormat().getType() == ShadowType.SHADOW_2)
     shape.getShadowFormat().setType(ShadowType.SHADOW_7);

 if (shape.getShadowFormat().getType() == ShadowType.SHADOW_MIXED)
     shape.getShadowFormat().clear();
 
```

**Returns:**
boolean -  true  إذا كان التنسيق المطبق على هذه الحالة مرئيًا.
### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


يضبط كائن java.awt.Color الذي يمثل اللون للظل. القيمة الافتراضية هي java.awt.Color\#getBlack().getBlack().

 **Examples:** 

يظهر كيفية الحصول على لون الظل.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

يعرض كيفية ضبط لون مع الشفافية.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 ShadowFormat shadowFormat = shape.getShadowFormat();
 shadowFormat.setType(ShadowType.SHADOW_21);
 shadowFormat.setColor(Color.RED);
 shadowFormat.setTransparency(0.8);

 doc.save(getArtifactsDir() + "Shape.ShadowFormatTransparency.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color | كائن java.awt.Color يمثل اللون للظل. |

### setTransparency(double value) {#setTransparency-double}
```
public void setTransparency(double value)
```


يضبط درجة الشفافية لتأثير الظل كقيمة بين 0.0 (معتم) و 1.0 (شفاف). القيمة الافتراضية هي 0.0.

 **Examples:** 

يعرض كيفية ضبط لون مع الشفافية.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 ShadowFormat shadowFormat = shape.getShadowFormat();
 shadowFormat.setType(ShadowType.SHADOW_21);
 shadowFormat.setColor(Color.RED);
 shadowFormat.setTransparency(0.8);

 doc.save(getArtifactsDir() + "Shape.ShadowFormatTransparency.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | درجة الشفافية لتأثير الظل كقيمة بين 0.0 (معتم) و 1.0 (شفاف). |

### setType(int value) {#setType-int}
```
public void setType(int value)
```


يضبط [ShadowType](../../com.aspose.words/shadowtype/) المحدد لـ ShadowFormat.

 **Remarks:** 

ضبط نوع ظل جديد سيعيد تعيين قيم اللون والشفافية إلى القيم الافتراضية. لذلك، من المنطقي أولاً ضبط نوع الظل المطلوب ثم قيم اللون والشفافية.

 **Examples:** 

يظهر كيفية الحصول على لون الظل.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | الـ [ShadowType](../../com.aspose.words/shadowtype/) المحدد لـ ShadowFormat. يجب أن تكون القيمة واحدة من ثوابت [ShadowType](../../com.aspose.words/shadowtype/). |

