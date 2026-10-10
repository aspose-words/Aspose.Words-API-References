---
title: "SoftEdgeFormat"
linktitle: "SoftEdgeFormat"
second_title: "Aspose.Words per Java"
description: "Rappresenta la formattazione dei bordi morbidi per un oggetto in Java."
type: docs
weight: 625
url: /it/java/com.aspose.words/softedgeformat/
---

**Inheritance:**
java.lang.Object
```
public class SoftEdgeFormat
```

Rappresenta la formattazione dei bordi morbidi per un oggetto.

 **Remarks:** 

Utilizza la proprietà [ShapeBase.getSoftEdge()](../../com.aspose.words/shapebase/\#getSoftEdge) per accedere alle proprietà dei bordi morbidi di un oggetto. Non è necessario creare istanze della classe [SoftEdgeFormat](../../com.aspose.words/softedgeformat/) direttamente.

 **Examples:** 

Mostra come lavorare con la formattazione dei bordi morbidi.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getRadius()](#getRadius) | Restituisce un valore double che rappresenta la lunghezza del raggio per un effetto di bordo morbido in punti (pt). |
| [remove()](#remove) | Rimuove [SoftEdgeFormat](../../com.aspose.words/softedgeformat/) dall'oggetto padre. |
| [setRadius(double value)](#setRadius-double) | Imposta un valore double che rappresenta la lunghezza del raggio per un effetto di bordo morbido in punti (pt). |
### getRadius() {#getRadius}
```
public double getRadius()
```


Restituisce un valore double che rappresenta la lunghezza del raggio per un effetto di bordo morbido in punti (pt). Il valore predefinito è 0.0.

 **Examples:** 

Mostra come lavorare con la formattazione dei bordi morbidi.

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

Mostra come impostare il limite per la risoluzione dell'immagine.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 SvgSaveOptions saveOptions = new SvgSaveOptions();
 saveOptions.setMaxImageResolution(72);

 doc.save(getArtifactsDir() + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
 
```

**Returns:**
double - Un valore double che rappresenta la lunghezza del raggio per un effetto di bordo morbido in punti (pt).
### remove() {#remove}
```
public void remove()
```


Rimuove [SoftEdgeFormat](../../com.aspose.words/softedgeformat/) dall'oggetto padre.

 **Examples:** 

Mostra come lavorare con la formattazione dei bordi morbidi.

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

Mostra come impostare il limite per la risoluzione dell'immagine.

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


Imposta un valore double che rappresenta la lunghezza del raggio per un effetto di bordo morbido in punti (pt). Il valore predefinito è 0.0.

 **Examples:** 

Mostra come lavorare con la formattazione dei bordi morbidi.

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

Mostra come impostare il limite per la risoluzione dell'immagine.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 SvgSaveOptions saveOptions = new SvgSaveOptions();
 saveOptions.setMaxImageResolution(72);

 doc.save(getArtifactsDir() + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | Un valore double che rappresenta la lunghezza del raggio per un effetto di bordo morbido in punti (pt). |

