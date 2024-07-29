---
title: SoftEdgeFormat
linktitle: SoftEdgeFormat
second_title: Aspose.Words for Java
description: Represents the soft edge formatting for an object in Java.
type: docs
weight: 576
url: /java/com.aspose.words/softedgeformat/
---

**Inheritance:**
java.lang.Object
```
public class SoftEdgeFormat
```

Represents the soft edge formatting for an object.

 **Remarks:** 

Use the [ShapeBase.getSoftEdge()](../../com.aspose.words/shapebase/\#getSoftEdge) property to access soft edge properties of an object. You do not create instances of the [SoftEdgeFormat](../../com.aspose.words/softedgeformat/) class directly.

 **Examples:** 

Shows how to work with soft edge formatting.

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
## Methods

| Method | Description |
| --- | --- |
| [getRadius()](#getRadius) | Gets a double value that represents the length of the radius for a soft edge effect in points (pt). |
| [remove()](#remove) | Removes [SoftEdgeFormat](../../com.aspose.words/softedgeformat/) from the parent object. |
| [setRadius(double value)](#setRadius-double) | Sets a double value that represents the length of the radius for a soft edge effect in points (pt). |
### getRadius() {#getRadius}
```
public double getRadius()
```


Gets a double value that represents the length of the radius for a soft edge effect in points (pt). The default value is 0.0.

 **Examples:** 

Shows how to set limit for image resolution.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 SvgSaveOptions saveOptions = new SvgSaveOptions();
 saveOptions.setMaxImageResolution(72);

 doc.save(getArtifactsDir() + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
 
```

Shows how to work with soft edge formatting.

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

**Returns:**
double - A double value that represents the length of the radius for a soft edge effect in points (pt).
### remove() {#remove}
```
public void remove()
```


Removes [SoftEdgeFormat](../../com.aspose.words/softedgeformat/) from the parent object.

 **Examples:** 

Shows how to set limit for image resolution.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 SvgSaveOptions saveOptions = new SvgSaveOptions();
 saveOptions.setMaxImageResolution(72);

 doc.save(getArtifactsDir() + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
 
```

Shows how to work with soft edge formatting.

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

### setRadius(double value) {#setRadius-double}
```
public void setRadius(double value)
```


Sets a double value that represents the length of the radius for a soft edge effect in points (pt). The default value is 0.0.

 **Examples:** 

Shows how to set limit for image resolution.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 SvgSaveOptions saveOptions = new SvgSaveOptions();
 saveOptions.setMaxImageResolution(72);

 doc.save(getArtifactsDir() + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
 
```

Shows how to work with soft edge formatting.

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | A double value that represents the length of the radius for a soft edge effect in points (pt). |

