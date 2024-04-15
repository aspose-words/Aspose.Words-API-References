---
title: GlowFormat
linktitle: GlowFormat
second_title: Aspose.Words for Java
description: Represents the glow formatting for an object in Java.
type: docs
weight: 329
url: /java/com.aspose.words/glowformat/
---

**Inheritance:**
java.lang.Object
```
public class GlowFormat
```

Represents the glow formatting for an object.

 **Remarks:** 

Use the [ShapeBase.getGlow()](../../com.aspose.words/shapebase/\#getGlow) property to access glow properties of an object. You do not create instances of the [GlowFormat](../../com.aspose.words/glowformat/) class directly.
## Methods

| Method | Description |
| --- | --- |
| [getColor()](#getColor) | Gets a java.awt.Color object that represents the color for a glow effect. |
| [getRadius()](#getRadius) | Gets a double value that represents the length of the radius for a glow effect in points (pt). |
| [getTransparency()](#getTransparency) | Gets the degree of transparency for the glow effect as a value between 0.0 (opaque) and 1.0 (clear). |
| [remove()](#remove) | Removes [GlowFormat](../../com.aspose.words/glowformat/) from the parent object. |
| [setColor(Color value)](#setColor-java.awt.Color) | Sets a java.awt.Color object that represents the color for a glow effect. |
| [setRadius(double value)](#setRadius-double) | Sets a double value that represents the length of the radius for a glow effect in points (pt). |
| [setTransparency(double value)](#setTransparency-double) | Sets the degree of transparency for the glow effect as a value between 0.0 (opaque) and 1.0 (clear). |
### getColor() {#getColor}
```
public Color getColor()
```


Gets a java.awt.Color object that represents the color for a glow effect. The default value is java.awt.Color\#getBlack().getBlack().

 **Examples:** 

Shows how to interact with glow shape effect.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(msColor.getSalmon());
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
java.awt.Color - A java.awt.Color object that represents the color for a glow effect.
### getRadius() {#getRadius}
```
public double getRadius()
```


Gets a double value that represents the length of the radius for a glow effect in points (pt). The default value is 0.0.

 **Examples:** 

Shows how to interact with glow shape effect.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(msColor.getSalmon());
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
double - A double value that represents the length of the radius for a glow effect in points (pt).
### getTransparency() {#getTransparency}
```
public double getTransparency()
```


Gets the degree of transparency for the glow effect as a value between 0.0 (opaque) and 1.0 (clear). The default value is 0.0.

 **Examples:** 

Shows how to interact with glow shape effect.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(msColor.getSalmon());
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
double - The degree of transparency for the glow effect as a value between 0.0 (opaque) and 1.0 (clear).
### remove() {#remove}
```
public void remove()
```


Removes [GlowFormat](../../com.aspose.words/glowformat/) from the parent object.

 **Examples:** 

Shows how to interact with glow shape effect.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(msColor.getSalmon());
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


Sets a java.awt.Color object that represents the color for a glow effect. The default value is java.awt.Color\#getBlack().getBlack().

 **Examples:** 

Shows how to interact with glow shape effect.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(msColor.getSalmon());
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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | A java.awt.Color object that represents the color for a glow effect. |

### setRadius(double value) {#setRadius-double}
```
public void setRadius(double value)
```


Sets a double value that represents the length of the radius for a glow effect in points (pt). The default value is 0.0.

 **Examples:** 

Shows how to interact with glow shape effect.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(msColor.getSalmon());
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
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | A double value that represents the length of the radius for a glow effect in points (pt). |

### setTransparency(double value) {#setTransparency-double}
```
public void setTransparency(double value)
```


Sets the degree of transparency for the glow effect as a value between 0.0 (opaque) and 1.0 (clear). The default value is 0.0.

 **Examples:** 

Shows how to interact with glow shape effect.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(msColor.getSalmon());
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
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The degree of transparency for the glow effect as a value between 0.0 (opaque) and 1.0 (clear). |

