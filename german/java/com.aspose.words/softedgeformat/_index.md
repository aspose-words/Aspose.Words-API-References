---
title: "SoftEdgeFormat"
linktitle: "SoftEdgeFormat"
second_title: "Aspose.Words für Java"
description: "Stellt die Soft-Edge-Formatierung für ein Objekt in Java dar."
type: docs
weight: 625
url: /de/java/com.aspose.words/softedgeformat/
---

**Inheritance:**
java.lang.Object
```
public class SoftEdgeFormat
```

Stellt die Weichkant-Formatierung für ein Objekt dar.

 **Remarks:** 

Verwenden Sie die [ShapeBase.getSoftEdge()](../../com.aspose.words/shapebase/\#getSoftEdge) Eigenschaft, um auf die Soft-Edge-Eigenschaften eines Objekts zuzugreifen. Sie erstellen keine Instanzen der Klasse [SoftEdgeFormat](../../com.aspose.words/softedgeformat/) direkt.

 **Examples:** 

Zeigt, wie man mit Soft-Edge-Formatierung arbeitet.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getRadius()](#getRadius) | Gibt einen double-Wert zurück, der die Länge des Radius für einen Soft-Edge-Effekt in Punkten (pt) darstellt. |
| [remove()](#remove) | Entfernt [SoftEdgeFormat](../../com.aspose.words/softedgeformat/) aus dem übergeordneten Objekt. |
| [setRadius(double value)](#setRadius-double) | Setzt einen double-Wert, der die Länge des Radius für einen Soft-Edge-Effekt in Punkten (pt) darstellt. |
### getRadius() {#getRadius}
```
public double getRadius()
```


Gibt einen double-Wert zurück, der die Länge des Radius für einen Soft-Edge-Effekt in Punkten (pt) darstellt. Der Standardwert ist 0.0.

 **Examples:** 

Zeigt, wie man mit Soft-Edge-Formatierung arbeitet.

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

Zeigt, wie man ein Limit für die Bildauflösung festlegt.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 SvgSaveOptions saveOptions = new SvgSaveOptions();
 saveOptions.setMaxImageResolution(72);

 doc.save(getArtifactsDir() + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
 
```

**Returns:**
double – Ein double-Wert, der die Länge des Radius für einen Soft-Edge-Effekt in Punkten (pt) darstellt.
### remove() {#remove}
```
public void remove()
```


Entfernt [SoftEdgeFormat](../../com.aspose.words/softedgeformat/) aus dem übergeordneten Objekt.

 **Examples:** 

Zeigt, wie man mit Soft-Edge-Formatierung arbeitet.

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

Zeigt, wie man ein Limit für die Bildauflösung festlegt.

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


Setzt einen double-Wert, der die Länge des Radius für einen Soft-Edge-Effekt in Punkten (pt) darstellt. Der Standardwert ist 0.0.

 **Examples:** 

Zeigt, wie man mit Soft-Edge-Formatierung arbeitet.

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

Zeigt, wie man ein Limit für die Bildauflösung festlegt.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 SvgSaveOptions saveOptions = new SvgSaveOptions();
 saveOptions.setMaxImageResolution(72);

 doc.save(getArtifactsDir() + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Ein double-Wert, der die Länge des Radius für einen Soft-Edge-Effekt in Punkten (pt) darstellt. |

