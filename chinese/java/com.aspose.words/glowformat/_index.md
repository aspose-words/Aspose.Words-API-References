---
title: "GlowFormat"
linktitle: "GlowFormat"
second_title: "Aspose.Words for Java"
description: "表示 Java 中对象的发光格式。"
type: docs
weight: 358
url: /zh/java/com.aspose.words/glowformat/
---

**Inheritance:**
java.lang.Object
```
public class GlowFormat
```

表示对象的发光格式。

 **Remarks:** 

使用 [ShapeBase.getGlow()](../../com.aspose.words/shapebase/\#getGlow) 属性来访问对象的发光属性。不要直接创建 [GlowFormat](../../com.aspose.words/glowformat/) 类的实例。

 **Examples:** 

展示如何与发光形状效果交互。

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
## 方法

| 方法 | 描述 |
| --- | --- |
| [getColor()](#getColor) | 获取表示发光效果颜色的 java.awt.Color 对象。 |
| [getRadius()](#getRadius) | 获取表示发光效果半径长度（以点 (pt) 为单位）的 double 值。 |
| [getTransparency()](#getTransparency) | 获取发光效果的透明度，取值范围为 0.0（不透明）到 1.0（透明）。 |
| [remove()](#remove) | 从父对象中移除 [GlowFormat](../../com.aspose.words/glowformat/)。 |
| [setColor(Color value)](#setColor-java.awt.Color) | 设置表示发光效果颜色的 java.awt.Color 对象。 |
| [setRadius(double value)](#setRadius-double) | 设置表示发光效果半径长度（以点 (pt) 为单位）的 double 值。 |
| [setTransparency(double value)](#setTransparency-double) | 设置发光效果的透明度，取值范围为 0.0（不透明）到 1.0（透明）。 |
### getColor() {#getColor}
```
public Color getColor()
```


获取表示发光效果颜色的 java.awt.Color 对象。默认值为 java.awt.Color\#getBlack().getBlack()。

 **Examples:** 

展示如何与发光形状效果交互。

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
java.awt.Color - 表示发光效果颜色的 java.awt.Color 对象。
### getRadius() {#getRadius}
```
public double getRadius()
```


获取表示发光效果半径长度（以点 (pt) 为单位）的 double 值。默认值为 0.0。

 **Examples:** 

展示如何与发光形状效果交互。

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
double - 表示发光效果半径长度（以点 (pt) 为单位）的 double 值。
### getTransparency() {#getTransparency}
```
public double getTransparency()
```


获取发光效果的透明度，取值范围为 0.0（不透明）到 1.0（透明）。默认值为 0.0。

 **Examples:** 

展示如何与发光形状效果交互。

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
double - 发光效果的透明度，取值范围为 0.0（不透明）和 1.0（透明）之间的值。
### remove() {#remove}
```
public void remove()
```


从父对象中移除 [GlowFormat](../../com.aspose.words/glowformat/)。

 **Examples:** 

展示如何与发光形状效果交互。

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


设置一个 java.awt.Color 对象，表示发光效果的颜色。默认值是 java.awt.Color\#getBlack().getBlack().

 **Examples:** 

展示如何与发光形状效果交互。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Color | 一个 java.awt.Color 对象，表示发光效果的颜色。 |

### setRadius(double value) {#setRadius-double}
```
public void setRadius(double value)
```


设置一个 double 值，表示发光效果半径的长度，单位为点 (pt)。默认值为 0.0。

 **Examples:** 

展示如何与发光形状效果交互。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 一个 double 值，表示发光效果半径的长度，单位为点 (pt)。 |

### setTransparency(double value) {#setTransparency-double}
```
public void setTransparency(double value)
```


设置发光效果的透明度，取值范围为 0.0（不透明）到 1.0（透明）之间的值。默认值为 0.0。

 **Examples:** 

展示如何与发光形状效果交互。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 发光效果的透明度，取值范围为 0.0（不透明）到 1.0（透明）之间的值。 |

