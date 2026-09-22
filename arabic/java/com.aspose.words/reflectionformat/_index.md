---
title: "ReflectionFormat"
linktitle: "ReflectionFormat"
second_title: "Aspose.Words لـ Java"
description: "يمثل تنسيق الانعكاس لكائن في Java."
type: docs
weight: 560
url: /ar/java/com.aspose.words/reflectionformat/
---

**Inheritance:**
java.lang.Object
```
public class ReflectionFormat
```

يمثل تنسيق الانعكاس لكائن.

 **Remarks:** 

استخدم الخاصية [ShapeBase.getReflection()](../../com.aspose.words/shapebase/\#getReflection) للوصول إلى خصائص الانعكاس لكائن. لا تقوم بإنشاء مثيلات من الفئة [ReflectionFormat](../../com.aspose.words/reflectionformat/) مباشرة.

 **Examples:** 

يوضح كيفية التفاعل مع تأثير شكل الانعكاس.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply reflection effect to the shape.
 shape.getReflection().setTransparency(0.37);
 shape.getReflection().setSize(0.48);
 shape.getReflection().setBlur(17.5);
 shape.getReflection().setDistance(9.2);

 doc.save(getArtifactsDir() + "Shape.Reflection.docx");

 doc = new Document(getArtifactsDir() + "Shape.Reflection.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check reflection effect attributes.
 Assert.assertEquals(0.37d, shape.getReflection().getTransparency(), 0.01d);
 Assert.assertEquals(0.48d, shape.getReflection().getSize(), 0.01d);
 Assert.assertEquals(17.5d, shape.getReflection().getBlur(), 0.01d);
 Assert.assertEquals(9.2d, shape.getReflection().getDistance(), 0.01d);

 // Remove reflection effect from the shape.
 shape.getReflection().remove();

 Assert.assertEquals(0, shape.getReflection().getTransparency());
 Assert.assertEquals(0, shape.getReflection().getSize());
 Assert.assertEquals(0, shape.getReflection().getBlur());
 Assert.assertEquals(0, shape.getReflection().getDistance());
 
```
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getBlur()](#getBlur) | يحصل على قيمة مزدوجة تحدد درجة تأثير الضبابية المطبقة على تأثير الانعكاس بالنقاط. |
| [getDistance()](#getDistance) | يحصل على قيمة مزدوجة تحدد مقدار الفصل بين الصورة المنعكسة والكائن بالنقاط. |
| [getSize()](#getSize) | يحصل على قيمة مزدوجة بين 0.0 و 1.0 تمثل حجم الانعكاس كنسبة مئوية من الكائن المنعكس. |
| [getTransparency()](#getTransparency) | يحصل على قيمة مزدوجة بين 0.0 (معتم) و 1.0 (شفاف) تمثل درجة الشفافية لتأثير الانعكاس. |
| [remove()](#remove) | يزيل [ReflectionFormat](../../com.aspose.words/reflectionformat/) من الكائن الأصل. |
| [setBlur(double value)](#setBlur-double) | يضبط قيمة مزدوجة تحدد درجة تأثير الضبابية المطبقة على تأثير الانعكاس بالنقاط. |
| [setDistance(double value)](#setDistance-double) | يضبط قيمة مزدوجة تحدد مقدار الفصل بين الصورة المنعكسة والكائن بالنقاط. |
| [setSize(double value)](#setSize-double) | يضبط قيمة مزدوجة بين 0.0 و 1.0 تمثل حجم الانعكاس كنسبة مئوية من الكائن المنعكس. |
| [setTransparency(double value)](#setTransparency-double) | يضبط قيمة مزدوجة بين 0.0 (معتم) و 1.0 (شفاف) تمثل درجة الشفافية لتأثير الانعكاس. |
### getBlur() {#getBlur}
```
public double getBlur()
```


يحصل على قيمة مزدوجة تحدد درجة تأثير الضبابية المطبقة على تأثير الانعكاس بالنقاط. القيمة الافتراضية هي 0.0.

 **Examples:** 

يوضح كيفية التفاعل مع تأثير شكل الانعكاس.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply reflection effect to the shape.
 shape.getReflection().setTransparency(0.37);
 shape.getReflection().setSize(0.48);
 shape.getReflection().setBlur(17.5);
 shape.getReflection().setDistance(9.2);

 doc.save(getArtifactsDir() + "Shape.Reflection.docx");

 doc = new Document(getArtifactsDir() + "Shape.Reflection.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check reflection effect attributes.
 Assert.assertEquals(0.37d, shape.getReflection().getTransparency(), 0.01d);
 Assert.assertEquals(0.48d, shape.getReflection().getSize(), 0.01d);
 Assert.assertEquals(17.5d, shape.getReflection().getBlur(), 0.01d);
 Assert.assertEquals(9.2d, shape.getReflection().getDistance(), 0.01d);

 // Remove reflection effect from the shape.
 shape.getReflection().remove();

 Assert.assertEquals(0, shape.getReflection().getTransparency());
 Assert.assertEquals(0, shape.getReflection().getSize());
 Assert.assertEquals(0, shape.getReflection().getBlur());
 Assert.assertEquals(0, shape.getReflection().getDistance());
 
```

**Returns:**
double - قيمة مزدوجة تحدد درجة تأثير الضبابية المطبقة على تأثير الانعكاس بالنقاط.
### getDistance() {#getDistance}
```
public double getDistance()
```


يحصل على قيمة مزدوجة تحدد مقدار الفصل بين الصورة المنعكسة والكائن بالنقاط. القيمة الافتراضية هي 0.0.

 **Examples:** 

يوضح كيفية التفاعل مع تأثير شكل الانعكاس.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply reflection effect to the shape.
 shape.getReflection().setTransparency(0.37);
 shape.getReflection().setSize(0.48);
 shape.getReflection().setBlur(17.5);
 shape.getReflection().setDistance(9.2);

 doc.save(getArtifactsDir() + "Shape.Reflection.docx");

 doc = new Document(getArtifactsDir() + "Shape.Reflection.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check reflection effect attributes.
 Assert.assertEquals(0.37d, shape.getReflection().getTransparency(), 0.01d);
 Assert.assertEquals(0.48d, shape.getReflection().getSize(), 0.01d);
 Assert.assertEquals(17.5d, shape.getReflection().getBlur(), 0.01d);
 Assert.assertEquals(9.2d, shape.getReflection().getDistance(), 0.01d);

 // Remove reflection effect from the shape.
 shape.getReflection().remove();

 Assert.assertEquals(0, shape.getReflection().getTransparency());
 Assert.assertEquals(0, shape.getReflection().getSize());
 Assert.assertEquals(0, shape.getReflection().getBlur());
 Assert.assertEquals(0, shape.getReflection().getDistance());
 
```

**Returns:**
double - قيمة مزدوجة تحدد مقدار الفصل بين الصورة المنعكسة والكائن بالنقاط.
### getSize() {#getSize}
```
public double getSize()
```


يحصل على قيمة مزدوجة بين 0.0 و 1.0 تمثل حجم الانعكاس كنسبة مئوية من الكائن المنعكس. القيمة الافتراضية هي 0.0.

 **Examples:** 

يوضح كيفية التفاعل مع تأثير شكل الانعكاس.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply reflection effect to the shape.
 shape.getReflection().setTransparency(0.37);
 shape.getReflection().setSize(0.48);
 shape.getReflection().setBlur(17.5);
 shape.getReflection().setDistance(9.2);

 doc.save(getArtifactsDir() + "Shape.Reflection.docx");

 doc = new Document(getArtifactsDir() + "Shape.Reflection.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check reflection effect attributes.
 Assert.assertEquals(0.37d, shape.getReflection().getTransparency(), 0.01d);
 Assert.assertEquals(0.48d, shape.getReflection().getSize(), 0.01d);
 Assert.assertEquals(17.5d, shape.getReflection().getBlur(), 0.01d);
 Assert.assertEquals(9.2d, shape.getReflection().getDistance(), 0.01d);

 // Remove reflection effect from the shape.
 shape.getReflection().remove();

 Assert.assertEquals(0, shape.getReflection().getTransparency());
 Assert.assertEquals(0, shape.getReflection().getSize());
 Assert.assertEquals(0, shape.getReflection().getBlur());
 Assert.assertEquals(0, shape.getReflection().getDistance());
 
```

**Returns:**
double - قيمة مزدوجة بين 0.0 و 1.0 تمثل حجم الانعكاس كنسبة مئوية من الكائن المنعكس.
### getTransparency() {#getTransparency}
```
public double getTransparency()
```


يحصل على قيمة مزدوجة بين 0.0 (معتم) و 1.0 (شفاف) تمثل درجة الشفافية لتأثير الانعكاس. القيمة الافتراضية هي 0.0.

 **Examples:** 

يوضح كيفية التفاعل مع تأثير شكل الانعكاس.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply reflection effect to the shape.
 shape.getReflection().setTransparency(0.37);
 shape.getReflection().setSize(0.48);
 shape.getReflection().setBlur(17.5);
 shape.getReflection().setDistance(9.2);

 doc.save(getArtifactsDir() + "Shape.Reflection.docx");

 doc = new Document(getArtifactsDir() + "Shape.Reflection.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check reflection effect attributes.
 Assert.assertEquals(0.37d, shape.getReflection().getTransparency(), 0.01d);
 Assert.assertEquals(0.48d, shape.getReflection().getSize(), 0.01d);
 Assert.assertEquals(17.5d, shape.getReflection().getBlur(), 0.01d);
 Assert.assertEquals(9.2d, shape.getReflection().getDistance(), 0.01d);

 // Remove reflection effect from the shape.
 shape.getReflection().remove();

 Assert.assertEquals(0, shape.getReflection().getTransparency());
 Assert.assertEquals(0, shape.getReflection().getSize());
 Assert.assertEquals(0, shape.getReflection().getBlur());
 Assert.assertEquals(0, shape.getReflection().getDistance());
 
```

**Returns:**
double - قيمة مزدوجة بين 0.0 (معتم) و 1.0 (شفاف) تمثل درجة الشفافية لتأثير الانعكاس.
### remove() {#remove}
```
public void remove()
```


يزيل [ReflectionFormat](../../com.aspose.words/reflectionformat/) من الكائن الأصل.

 **Examples:** 

يوضح كيفية التفاعل مع تأثير شكل الانعكاس.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply reflection effect to the shape.
 shape.getReflection().setTransparency(0.37);
 shape.getReflection().setSize(0.48);
 shape.getReflection().setBlur(17.5);
 shape.getReflection().setDistance(9.2);

 doc.save(getArtifactsDir() + "Shape.Reflection.docx");

 doc = new Document(getArtifactsDir() + "Shape.Reflection.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check reflection effect attributes.
 Assert.assertEquals(0.37d, shape.getReflection().getTransparency(), 0.01d);
 Assert.assertEquals(0.48d, shape.getReflection().getSize(), 0.01d);
 Assert.assertEquals(17.5d, shape.getReflection().getBlur(), 0.01d);
 Assert.assertEquals(9.2d, shape.getReflection().getDistance(), 0.01d);

 // Remove reflection effect from the shape.
 shape.getReflection().remove();

 Assert.assertEquals(0, shape.getReflection().getTransparency());
 Assert.assertEquals(0, shape.getReflection().getSize());
 Assert.assertEquals(0, shape.getReflection().getBlur());
 Assert.assertEquals(0, shape.getReflection().getDistance());
 
```

### setBlur(double value) {#setBlur-double}
```
public void setBlur(double value)
```


يضبط قيمة مزدوجة تحدد درجة تأثير الضبابية المطبقة على تأثير الانعكاس بالنقاط. القيمة الافتراضية هي 0.0.

 **Examples:** 

يوضح كيفية التفاعل مع تأثير شكل الانعكاس.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply reflection effect to the shape.
 shape.getReflection().setTransparency(0.37);
 shape.getReflection().setSize(0.48);
 shape.getReflection().setBlur(17.5);
 shape.getReflection().setDistance(9.2);

 doc.save(getArtifactsDir() + "Shape.Reflection.docx");

 doc = new Document(getArtifactsDir() + "Shape.Reflection.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check reflection effect attributes.
 Assert.assertEquals(0.37d, shape.getReflection().getTransparency(), 0.01d);
 Assert.assertEquals(0.48d, shape.getReflection().getSize(), 0.01d);
 Assert.assertEquals(17.5d, shape.getReflection().getBlur(), 0.01d);
 Assert.assertEquals(9.2d, shape.getReflection().getDistance(), 0.01d);

 // Remove reflection effect from the shape.
 shape.getReflection().remove();

 Assert.assertEquals(0, shape.getReflection().getTransparency());
 Assert.assertEquals(0, shape.getReflection().getSize());
 Assert.assertEquals(0, shape.getReflection().getBlur());
 Assert.assertEquals(0, shape.getReflection().getDistance());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | قيمة مزدوجة تحدد درجة تأثير الضبابية المطبقة على تأثير الانعكاس بالنقاط. |

### setDistance(double value) {#setDistance-double}
```
public void setDistance(double value)
```


يضبط قيمة مزدوجة تحدد مقدار الفصل بين الصورة المنعكسة والكائن بالنقاط. القيمة الافتراضية هي 0.0.

 **Examples:** 

يوضح كيفية التفاعل مع تأثير شكل الانعكاس.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply reflection effect to the shape.
 shape.getReflection().setTransparency(0.37);
 shape.getReflection().setSize(0.48);
 shape.getReflection().setBlur(17.5);
 shape.getReflection().setDistance(9.2);

 doc.save(getArtifactsDir() + "Shape.Reflection.docx");

 doc = new Document(getArtifactsDir() + "Shape.Reflection.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check reflection effect attributes.
 Assert.assertEquals(0.37d, shape.getReflection().getTransparency(), 0.01d);
 Assert.assertEquals(0.48d, shape.getReflection().getSize(), 0.01d);
 Assert.assertEquals(17.5d, shape.getReflection().getBlur(), 0.01d);
 Assert.assertEquals(9.2d, shape.getReflection().getDistance(), 0.01d);

 // Remove reflection effect from the shape.
 shape.getReflection().remove();

 Assert.assertEquals(0, shape.getReflection().getTransparency());
 Assert.assertEquals(0, shape.getReflection().getSize());
 Assert.assertEquals(0, shape.getReflection().getBlur());
 Assert.assertEquals(0, shape.getReflection().getDistance());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | قيمة مزدوجة تحدد مقدار الفصل بين الصورة المنعكسة والكائن بالنقاط. |

### setSize(double value) {#setSize-double}
```
public void setSize(double value)
```


يضبط قيمة مزدوجة بين 0.0 و 1.0 تمثل حجم الانعكاس كنسبة مئوية من الكائن المنعكس. القيمة الافتراضية هي 0.0.

 **Examples:** 

يوضح كيفية التفاعل مع تأثير شكل الانعكاس.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply reflection effect to the shape.
 shape.getReflection().setTransparency(0.37);
 shape.getReflection().setSize(0.48);
 shape.getReflection().setBlur(17.5);
 shape.getReflection().setDistance(9.2);

 doc.save(getArtifactsDir() + "Shape.Reflection.docx");

 doc = new Document(getArtifactsDir() + "Shape.Reflection.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check reflection effect attributes.
 Assert.assertEquals(0.37d, shape.getReflection().getTransparency(), 0.01d);
 Assert.assertEquals(0.48d, shape.getReflection().getSize(), 0.01d);
 Assert.assertEquals(17.5d, shape.getReflection().getBlur(), 0.01d);
 Assert.assertEquals(9.2d, shape.getReflection().getDistance(), 0.01d);

 // Remove reflection effect from the shape.
 shape.getReflection().remove();

 Assert.assertEquals(0, shape.getReflection().getTransparency());
 Assert.assertEquals(0, shape.getReflection().getSize());
 Assert.assertEquals(0, shape.getReflection().getBlur());
 Assert.assertEquals(0, shape.getReflection().getDistance());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | قيمة مزدوجة بين 0.0 و 1.0 تمثل حجم الانعكاس كنسبة مئوية من الكائن المنعكس. |

### setTransparency(double value) {#setTransparency-double}
```
public void setTransparency(double value)
```


يضبط قيمة مزدوجة بين 0.0 (معتم) و 1.0 (شفاف) تمثل درجة الشفافية لتأثير الانعكاس. القيمة الافتراضية هي 0.0.

 **Examples:** 

يوضح كيفية التفاعل مع تأثير شكل الانعكاس.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply reflection effect to the shape.
 shape.getReflection().setTransparency(0.37);
 shape.getReflection().setSize(0.48);
 shape.getReflection().setBlur(17.5);
 shape.getReflection().setDistance(9.2);

 doc.save(getArtifactsDir() + "Shape.Reflection.docx");

 doc = new Document(getArtifactsDir() + "Shape.Reflection.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check reflection effect attributes.
 Assert.assertEquals(0.37d, shape.getReflection().getTransparency(), 0.01d);
 Assert.assertEquals(0.48d, shape.getReflection().getSize(), 0.01d);
 Assert.assertEquals(17.5d, shape.getReflection().getBlur(), 0.01d);
 Assert.assertEquals(9.2d, shape.getReflection().getDistance(), 0.01d);

 // Remove reflection effect from the shape.
 shape.getReflection().remove();

 Assert.assertEquals(0, shape.getReflection().getTransparency());
 Assert.assertEquals(0, shape.getReflection().getSize());
 Assert.assertEquals(0, shape.getReflection().getBlur());
 Assert.assertEquals(0, shape.getReflection().getDistance());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | قيمة مزدوجة بين 0.0 (معتم) و 1.0 (شفاف) تمثل درجة الشفافية لتأثير الانعكاس. |

