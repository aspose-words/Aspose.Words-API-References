---
title: "SoftEdgeFormat"
linktitle: "SoftEdgeFormat"
second_title: "Aspose.Words para Java"
description: "Representa el formato de borde suave para un objeto en Java."
type: docs
weight: 625
url: /es/java/com.aspose.words/softedgeformat/
---

**Inheritance:**
java.lang.Object
```
public class SoftEdgeFormat
```

Representa el formato de borde suave para un objeto.

 **Remarks:** 

Utiliza la propiedad [ShapeBase.getSoftEdge()](../../com.aspose.words/shapebase/\#getSoftEdge) para acceder a las propiedades de borde suave de un objeto. No creas instancias de la clase [SoftEdgeFormat](../../com.aspose.words/softedgeformat/) directamente.

 **Examples:** 

Muestra cómo trabajar con el formato de borde suave.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [getRadius()](#getRadius) | Obtiene un valor double que representa la longitud del radio para un efecto de borde suave en puntos (pt). |
| [remove()](#remove) | Elimina [SoftEdgeFormat](../../com.aspose.words/softedgeformat/) del objeto padre. |
| [setRadius(double value)](#setRadius-double) | Establece un valor double que representa la longitud del radio para un efecto de borde suave en puntos (pt). |
### getRadius() {#getRadius}
```
public double getRadius()
```


Obtiene un valor double que representa la longitud del radio para un efecto de borde suave en puntos (pt). El valor predeterminado es 0.0.

 **Examples:** 

Muestra cómo trabajar con el formato de borde suave.

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

Muestra cómo establecer un límite para la resolución de la imagen.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 SvgSaveOptions saveOptions = new SvgSaveOptions();
 saveOptions.setMaxImageResolution(72);

 doc.save(getArtifactsDir() + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
 
```

**Returns:**
double - Un valor double que representa la longitud del radio para un efecto de borde suave en puntos (pt).
### remove() {#remove}
```
public void remove()
```


Elimina [SoftEdgeFormat](../../com.aspose.words/softedgeformat/) del objeto padre.

 **Examples:** 

Muestra cómo trabajar con el formato de borde suave.

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

Muestra cómo establecer un límite para la resolución de la imagen.

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


Establece un valor double que representa la longitud del radio para un efecto de borde suave en puntos (pt). El valor predeterminado es 0.0.

 **Examples:** 

Muestra cómo trabajar con el formato de borde suave.

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

Muestra cómo establecer un límite para la resolución de la imagen.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 SvgSaveOptions saveOptions = new SvgSaveOptions();
 saveOptions.setMaxImageResolution(72);

 doc.save(getArtifactsDir() + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | Un valor double que representa la longitud del radio para un efecto de borde suave en puntos (pt). |

