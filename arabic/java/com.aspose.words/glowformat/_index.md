---
title: "GlowFormat"
linktitle: "GlowFormat"
second_title: "Aspose.Words لـ Java"
description: "يمثل تنسيق التوهج لكائن في Java."
type: docs
weight: 358
url: /ar/java/com.aspose.words/glowformat/
---

**Inheritance:**
java.lang.Object
```
public class GlowFormat
```

يمثل تنسيق التوهج لكائن.

 **Remarks:** 

استخدم خاصية [ShapeBase.getGlow()](../../com.aspose.words/shapebase/\#getGlow) للوصول إلى خصائص التوهج لكائن. لا تقوم بإنشاء مثيلات من الفئة [GlowFormat](../../com.aspose.words/glowformat/) مباشرةً.

 **Examples:** 

يظهر كيفية التفاعل مع تأثير الشكل المتوهج.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(new Color(0xFFFA8072));
 shape.getGlow().setRadius(30.0);
 shape.getGlow().setTransparency(0.15);

 doc.save(getArtifactsDir() + "Shape.Glow.docx");

 doc = new Document(getArtifactsDir() + "Shape.Glow.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check glow effect attributes.
 Assert.assertEquals(new Color((250), (128), (114), (217)).getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(30, shape.getGlow().getRadius());
 Assert.assertEquals(0.15d, shape.getGlow().getTransparency(), 0.01d);

 // Remove glow effect from the shape.
 shape.getGlow().remove();

 Assert.assertEquals(Color.BLACK.getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(0, shape.getGlow().getRadius());
 Assert.assertEquals(0, shape.getGlow().getTransparency());
 
```
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getColor()](#getColor) | يحصل على كائن java.awt.Color يمثل اللون لتأثير التوهج. |
| [getRadius()](#getRadius) | يحصل على قيمة مزدوجة تمثل طول نصف القطر لتأثير التوهج بالنقاط (pt). |
| [getTransparency()](#getTransparency) | يحصل على درجة الشفافية لتأثير التوهج كقيمة بين 0.0 (معتم) و 1.0 (شفاف). |
| [remove()](#remove) | يزيل [GlowFormat](../../com.aspose.words/glowformat/) من الكائن الأب. |
| [setColor(Color value)](#setColor-java.awt.Color) | يضبط كائن java.awt.Color يمثل اللون لتأثير التوهج. |
| [setRadius(double value)](#setRadius-double) | يضبط قيمة مزدوجة تمثل طول نصف القطر لتأثير التوهج بالنقاط (pt). |
| [setTransparency(double value)](#setTransparency-double) | يضبط درجة الشفافية لتأثير التوهج كقيمة بين 0.0 (معتم) و 1.0 (شفاف). |
### getColor() {#getColor}
```
public Color getColor()
```


يحصل على كائن java.awt.Color يمثل اللون لتأثير التوهج. القيمة الافتراضية هي java.awt.Color\#getBlack().getBlack().

 **Examples:** 

يظهر كيفية التفاعل مع تأثير الشكل المتوهج.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(new Color(0xFFFA8072));
 shape.getGlow().setRadius(30.0);
 shape.getGlow().setTransparency(0.15);

 doc.save(getArtifactsDir() + "Shape.Glow.docx");

 doc = new Document(getArtifactsDir() + "Shape.Glow.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check glow effect attributes.
 Assert.assertEquals(new Color((250), (128), (114), (217)).getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(30, shape.getGlow().getRadius());
 Assert.assertEquals(0.15d, shape.getGlow().getTransparency(), 0.01d);

 // Remove glow effect from the shape.
 shape.getGlow().remove();

 Assert.assertEquals(Color.BLACK.getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(0, shape.getGlow().getRadius());
 Assert.assertEquals(0, shape.getGlow().getTransparency());
 
```

**Returns:**
java.awt.Color - كائن java.awt.Color يمثل اللون لتأثير التوهج.
### getRadius() {#getRadius}
```
public double getRadius()
```


يحصل على قيمة مزدوجة تمثل طول نصف القطر لتأثير التوهج بالنقاط (pt). القيمة الافتراضية هي 0.0.

 **Examples:** 

يظهر كيفية التفاعل مع تأثير الشكل المتوهج.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(new Color(0xFFFA8072));
 shape.getGlow().setRadius(30.0);
 shape.getGlow().setTransparency(0.15);

 doc.save(getArtifactsDir() + "Shape.Glow.docx");

 doc = new Document(getArtifactsDir() + "Shape.Glow.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check glow effect attributes.
 Assert.assertEquals(new Color((250), (128), (114), (217)).getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(30, shape.getGlow().getRadius());
 Assert.assertEquals(0.15d, shape.getGlow().getTransparency(), 0.01d);

 // Remove glow effect from the shape.
 shape.getGlow().remove();

 Assert.assertEquals(Color.BLACK.getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(0, shape.getGlow().getRadius());
 Assert.assertEquals(0, shape.getGlow().getTransparency());
 
```

**Returns:**
double - قيمة مزدوجة تمثل طول نصف القطر لتأثير التوهج بالنقاط (pt).
### getTransparency() {#getTransparency}
```
public double getTransparency()
```


يحصل على درجة الشفافية لتأثير التوهج كقيمة بين 0.0 (معتم) و 1.0 (شفاف). القيمة الافتراضية هي 0.0.

 **Examples:** 

يظهر كيفية التفاعل مع تأثير الشكل المتوهج.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(new Color(0xFFFA8072));
 shape.getGlow().setRadius(30.0);
 shape.getGlow().setTransparency(0.15);

 doc.save(getArtifactsDir() + "Shape.Glow.docx");

 doc = new Document(getArtifactsDir() + "Shape.Glow.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check glow effect attributes.
 Assert.assertEquals(new Color((250), (128), (114), (217)).getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(30, shape.getGlow().getRadius());
 Assert.assertEquals(0.15d, shape.getGlow().getTransparency(), 0.01d);

 // Remove glow effect from the shape.
 shape.getGlow().remove();

 Assert.assertEquals(Color.BLACK.getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(0, shape.getGlow().getRadius());
 Assert.assertEquals(0, shape.getGlow().getTransparency());
 
```

**Returns:**
double - درجة الشفافية لتأثير التوهج كقيمة بين 0.0 (معتم) و 1.0 (شفاف).
### remove() {#remove}
```
public void remove()
```


يزيل [GlowFormat](../../com.aspose.words/glowformat/) من الكائن الأب.

 **Examples:** 

يظهر كيفية التفاعل مع تأثير الشكل المتوهج.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(new Color(0xFFFA8072));
 shape.getGlow().setRadius(30.0);
 shape.getGlow().setTransparency(0.15);

 doc.save(getArtifactsDir() + "Shape.Glow.docx");

 doc = new Document(getArtifactsDir() + "Shape.Glow.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check glow effect attributes.
 Assert.assertEquals(new Color((250), (128), (114), (217)).getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(30, shape.getGlow().getRadius());
 Assert.assertEquals(0.15d, shape.getGlow().getTransparency(), 0.01d);

 // Remove glow effect from the shape.
 shape.getGlow().remove();

 Assert.assertEquals(Color.BLACK.getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(0, shape.getGlow().getRadius());
 Assert.assertEquals(0, shape.getGlow().getTransparency());
 
```

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


يضبط كائن java.awt.Color يمثل اللون لتأثير التوهج. القيمة الافتراضية هي java.awt.Color\#getBlack().getBlack().

 **Examples:** 

يظهر كيفية التفاعل مع تأثير الشكل المتوهج.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(new Color(0xFFFA8072));
 shape.getGlow().setRadius(30.0);
 shape.getGlow().setTransparency(0.15);

 doc.save(getArtifactsDir() + "Shape.Glow.docx");

 doc = new Document(getArtifactsDir() + "Shape.Glow.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check glow effect attributes.
 Assert.assertEquals(new Color((250), (128), (114), (217)).getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(30, shape.getGlow().getRadius());
 Assert.assertEquals(0.15d, shape.getGlow().getTransparency(), 0.01d);

 // Remove glow effect from the shape.
 shape.getGlow().remove();

 Assert.assertEquals(Color.BLACK.getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(0, shape.getGlow().getRadius());
 Assert.assertEquals(0, shape.getGlow().getTransparency());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color | كائن java.awt.Color يمثل اللون لتأثير التوهج. |

### setRadius(double value) {#setRadius-double}
```
public void setRadius(double value)
```


يضبط قيمة مزدوجة تمثل طول نصف القطر لتأثير التوهج بالنقاط (pt). القيمة الافتراضية هي 0.0.

 **Examples:** 

يظهر كيفية التفاعل مع تأثير الشكل المتوهج.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(new Color(0xFFFA8072));
 shape.getGlow().setRadius(30.0);
 shape.getGlow().setTransparency(0.15);

 doc.save(getArtifactsDir() + "Shape.Glow.docx");

 doc = new Document(getArtifactsDir() + "Shape.Glow.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check glow effect attributes.
 Assert.assertEquals(new Color((250), (128), (114), (217)).getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(30, shape.getGlow().getRadius());
 Assert.assertEquals(0.15d, shape.getGlow().getTransparency(), 0.01d);

 // Remove glow effect from the shape.
 shape.getGlow().remove();

 Assert.assertEquals(Color.BLACK.getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(0, shape.getGlow().getRadius());
 Assert.assertEquals(0, shape.getGlow().getTransparency());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | قيمة مزدوجة تمثل طول نصف القطر لتأثير التوهج بالنقاط (pt). |

### setTransparency(double value) {#setTransparency-double}
```
public void setTransparency(double value)
```


يضبط درجة الشفافية لتأثير التوهج كقيمة بين 0.0 (معتم) و 1.0 (شفاف). القيمة الافتراضية هي 0.0.

 **Examples:** 

يظهر كيفية التفاعل مع تأثير الشكل المتوهج.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(new Color(0xFFFA8072));
 shape.getGlow().setRadius(30.0);
 shape.getGlow().setTransparency(0.15);

 doc.save(getArtifactsDir() + "Shape.Glow.docx");

 doc = new Document(getArtifactsDir() + "Shape.Glow.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check glow effect attributes.
 Assert.assertEquals(new Color((250), (128), (114), (217)).getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(30, shape.getGlow().getRadius());
 Assert.assertEquals(0.15d, shape.getGlow().getTransparency(), 0.01d);

 // Remove glow effect from the shape.
 shape.getGlow().remove();

 Assert.assertEquals(Color.BLACK.getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(0, shape.getGlow().getRadius());
 Assert.assertEquals(0, shape.getGlow().getTransparency());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | درجة الشفافية لتأثير التوهج كقيمة بين 0.0 (معتم) و 1.0 (شفاف). |

