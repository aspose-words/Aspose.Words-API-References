---
title: "SoftEdgeFormat"
linktitle: "SoftEdgeFormat"
second_title: "Aspose.Words لـ Java"
description: "يمثل تنسيق الحافة الناعمة لكائن في Java."
type: docs
weight: 625
url: /ar/java/com.aspose.words/softedgeformat/
---

**Inheritance:**
java.lang.Object
```
public class SoftEdgeFormat
```

يمثل تنسيق الحافة الناعمة لكائن.

 **Remarks:** 

استخدم الخاصية [ShapeBase.getSoftEdge()](../../com.aspose.words/shapebase/\#getSoftEdge) للوصول إلى خصائص الحافة الناعمة لكائن. لا تقوم بإنشاء مثيلات من الفئة [SoftEdgeFormat](../../com.aspose.words/softedgeformat/) مباشرة.

 **Examples:** 

يوضح كيفية العمل مع تنسيق الحافة الناعمة.

```

 DocumentBuilder builder = new DocumentBuilder();
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 200.0, 200.0);

 // Apply soft edge to the shape.
 shape.getSoftEdge().setRadius(30.0);

 builder.getDocument().save(getArtifactsDir() + "Shape.SoftEdge.docx");

 // Load document with rectangle shape with soft edge.
 Document doc = new Document(getArtifactsDir() + "Shape.SoftEdge.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check soft edge radius.
 Assert.assertEquals(30, shape.getSoftEdge().getRadius());

 // Remove soft edge from the shape.
 shape.getSoftEdge().remove();

 // Check radius of the removed soft edge.
 Assert.assertEquals(0, shape.getSoftEdge().getRadius());
 
```
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getRadius()](#getRadius) | يحصل على قيمة مزدوجة تمثل طول نصف القطر لتأثير الحافة الناعمة بالنقاط (pt). |
| [remove()](#remove) | يزيل [SoftEdgeFormat](../../com.aspose.words/softedgeformat/) من الكائن الأصلي. |
| [setRadius(double value)](#setRadius-double) | يضبط قيمة مزدوجة تمثل طول نصف القطر لتأثير الحافة الناعمة بالنقاط (pt). |
### getRadius() {#getRadius}
```
public double getRadius()
```


يحصل على قيمة مزدوجة تمثل طول نصف القطر لتأثير الحافة الناعمة بالنقاط (pt). القيمة الافتراضية هي 0.0.

 **Examples:** 

يوضح كيفية العمل مع تنسيق الحافة الناعمة.

```

 DocumentBuilder builder = new DocumentBuilder();
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 200.0, 200.0);

 // Apply soft edge to the shape.
 shape.getSoftEdge().setRadius(30.0);

 builder.getDocument().save(getArtifactsDir() + "Shape.SoftEdge.docx");

 // Load document with rectangle shape with soft edge.
 Document doc = new Document(getArtifactsDir() + "Shape.SoftEdge.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check soft edge radius.
 Assert.assertEquals(30, shape.getSoftEdge().getRadius());

 // Remove soft edge from the shape.
 shape.getSoftEdge().remove();

 // Check radius of the removed soft edge.
 Assert.assertEquals(0, shape.getSoftEdge().getRadius());
 
```

يوضح كيفية تعيين حد لدقة الصورة.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 SvgSaveOptions saveOptions = new SvgSaveOptions();
 saveOptions.setMaxImageResolution(72);

 doc.save(getArtifactsDir() + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
 
```

**Returns:**
مزدوج - قيمة مزدوجة تمثل طول نصف القطر لتأثير الحافة الناعمة بالنقاط (pt).
### remove() {#remove}
```
public void remove()
```


يزيل [SoftEdgeFormat](../../com.aspose.words/softedgeformat/) من الكائن الأصلي.

 **Examples:** 

يوضح كيفية العمل مع تنسيق الحافة الناعمة.

```

 DocumentBuilder builder = new DocumentBuilder();
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 200.0, 200.0);

 // Apply soft edge to the shape.
 shape.getSoftEdge().setRadius(30.0);

 builder.getDocument().save(getArtifactsDir() + "Shape.SoftEdge.docx");

 // Load document with rectangle shape with soft edge.
 Document doc = new Document(getArtifactsDir() + "Shape.SoftEdge.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check soft edge radius.
 Assert.assertEquals(30, shape.getSoftEdge().getRadius());

 // Remove soft edge from the shape.
 shape.getSoftEdge().remove();

 // Check radius of the removed soft edge.
 Assert.assertEquals(0, shape.getSoftEdge().getRadius());
 
```

يوضح كيفية تعيين حد لدقة الصورة.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 SvgSaveOptions saveOptions = new SvgSaveOptions();
 saveOptions.setMaxImageResolution(72);

 doc.save(getArtifactsDir() + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
 
```

### setRadius(double value) {#setRadius-double}
```
public void setRadius(double value)
```


يضبط قيمة مزدوجة تمثل طول نصف القطر لتأثير الحافة الناعمة بالنقاط (pt). القيمة الافتراضية هي 0.0.

 **Examples:** 

يوضح كيفية العمل مع تنسيق الحافة الناعمة.

```

 DocumentBuilder builder = new DocumentBuilder();
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 200.0, 200.0);

 // Apply soft edge to the shape.
 shape.getSoftEdge().setRadius(30.0);

 builder.getDocument().save(getArtifactsDir() + "Shape.SoftEdge.docx");

 // Load document with rectangle shape with soft edge.
 Document doc = new Document(getArtifactsDir() + "Shape.SoftEdge.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check soft edge radius.
 Assert.assertEquals(30, shape.getSoftEdge().getRadius());

 // Remove soft edge from the shape.
 shape.getSoftEdge().remove();

 // Check radius of the removed soft edge.
 Assert.assertEquals(0, shape.getSoftEdge().getRadius());
 
```

يوضح كيفية تعيين حد لدقة الصورة.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 SvgSaveOptions saveOptions = new SvgSaveOptions();
 saveOptions.setMaxImageResolution(72);

 doc.save(getArtifactsDir() + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | قيمة مزدوجة تمثل طول نصف القطر لتأثير الحافة الناعمة بالنقاط (pt). |

