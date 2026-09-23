---
title: "ReflectionFormat"
linktitle: "ReflectionFormat"
second_title: "Aspose.Words per Java"
description: "Rappresenta la formattazione della riflessione per un oggetto in Java."
type: docs
weight: 560
url: /it/java/com.aspose.words/reflectionformat/
---

**Inheritance:**
java.lang.Object
```
public class ReflectionFormat
```

Rappresenta la formattazione della riflessione per un oggetto.

 **Remarks:** 

Utilizza la proprietà [ShapeBase.getReflection()](../../com.aspose.words/shapebase/\#getReflection) per accedere alle proprietà di riflessione di un oggetto. Non è necessario creare istanze della classe [ReflectionFormat](../../com.aspose.words/reflectionformat/) direttamente.

 **Examples:** 

Mostra come interagire con l'effetto di forma di riflessione.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getBlur()](#getBlur) | Restituisce un valore double che specifica il grado di effetto sfocatura applicato all'effetto di riflessione in punti. |
| [getDistance()](#getDistance) | Restituisce un valore double che specifica la quantità di separazione dell'immagine riflessa dall'oggetto in punti. |
| [getSize()](#getSize) | Restituisce un valore double compreso tra 0.0 e 1.0 che rappresenta la dimensione della riflessione come percentuale dell'oggetto riflesso. |
| [getTransparency()](#getTransparency) | Restituisce un valore double compreso tra 0.0 (opaco) e 1.0 (chiaro) che rappresenta il grado di trasparenza per l'effetto di riflessione. |
| [remove()](#remove) | Rimuove [ReflectionFormat](../../com.aspose.words/reflectionformat/) dall'oggetto padre. |
| [setBlur(double value)](#setBlur-double) | Imposta un valore double che specifica il grado di effetto sfocatura applicato all'effetto di riflessione in punti. |
| [setDistance(double value)](#setDistance-double) | Imposta un valore double che specifica la quantità di separazione dell'immagine riflessa dall'oggetto in punti. |
| [setSize(double value)](#setSize-double) | Imposta un valore double compreso tra 0.0 e 1.0 che rappresenta la dimensione della riflessione come percentuale dell'oggetto riflesso. |
| [setTransparency(double value)](#setTransparency-double) | Imposta un valore double compreso tra 0.0 (opaco) e 1.0 (chiaro) che rappresenta il grado di trasparenza per l'effetto di riflessione. |
### getBlur() {#getBlur}
```
public double getBlur()
```


Restituisce un valore double che specifica il grado di effetto sfocatura applicato all'effetto di riflessione in punti. Il valore predefinito è 0.0.

 **Examples:** 

Mostra come interagire con l'effetto di forma di riflessione.

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
double - Un valore double che specifica il grado di effetto sfocatura applicato all'effetto di riflessione in punti.
### getDistance() {#getDistance}
```
public double getDistance()
```


Restituisce un valore double che specifica la quantità di separazione dell'immagine riflessa dall'oggetto in punti. Il valore predefinito è 0.0.

 **Examples:** 

Mostra come interagire con l'effetto di forma di riflessione.

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
double - Un valore double che specifica la quantità di separazione dell'immagine riflessa dall'oggetto in punti.
### getSize() {#getSize}
```
public double getSize()
```


Restituisce un valore double compreso tra 0.0 e 1.0 che rappresenta la dimensione della riflessione come percentuale dell'oggetto riflesso. Il valore predefinito è 0.0.

 **Examples:** 

Mostra come interagire con l'effetto di forma di riflessione.

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
double - Un valore double compreso tra 0.0 e 1.0 che rappresenta la dimensione della riflessione come percentuale dell'oggetto riflesso.
### getTransparency() {#getTransparency}
```
public double getTransparency()
```


Restituisce un valore double compreso tra 0.0 (opaco) e 1.0 (chiaro) che rappresenta il grado di trasparenza per l'effetto di riflessione. Il valore predefinito è 0.0.

 **Examples:** 

Mostra come interagire con l'effetto di forma di riflessione.

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
double - Un valore double compreso tra 0.0 (opaco) e 1.0 (chiaro) che rappresenta il grado di trasparenza per l'effetto di riflessione.
### remove() {#remove}
```
public void remove()
```


Rimuove [ReflectionFormat](../../com.aspose.words/reflectionformat/) dall'oggetto padre.

 **Examples:** 

Mostra come interagire con l'effetto di forma di riflessione.

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


Imposta un valore double che specifica il grado di effetto sfocatura applicato all'effetto di riflessione in punti. Il valore predefinito è 0.0.

 **Examples:** 

Mostra come interagire con l'effetto di forma di riflessione.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | Un valore double che specifica il grado di effetto sfocatura applicato all'effetto di riflessione in punti. |

### setDistance(double value) {#setDistance-double}
```
public void setDistance(double value)
```


Imposta un valore double che specifica la quantità di separazione dell'immagine riflessa dall'oggetto in punti. Il valore predefinito è 0.0.

 **Examples:** 

Mostra come interagire con l'effetto di forma di riflessione.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | Un valore double che specifica la quantità di separazione dell'immagine riflessa dall'oggetto in punti. |

### setSize(double value) {#setSize-double}
```
public void setSize(double value)
```


Imposta un valore double compreso tra 0.0 e 1.0 che rappresenta la dimensione del riflesso come percentuale dell'oggetto riflesso. Il valore predefinito è 0.0.

 **Examples:** 

Mostra come interagire con l'effetto di forma di riflessione.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | Un valore double compreso tra 0.0 e 1.0 che rappresenta la dimensione del riflesso come percentuale dell'oggetto riflesso. |

### setTransparency(double value) {#setTransparency-double}
```
public void setTransparency(double value)
```


Imposta un valore double compreso tra 0.0 (opaco) e 1.0 (trasparente) che rappresenta il grado di trasparenza dell'effetto di riflessione. Il valore predefinito è 0.0.

 **Examples:** 

Mostra come interagire con l'effetto di forma di riflessione.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | Un valore double compreso tra 0.0 (opaco) e 1.0 (trasparente) che rappresenta il grado di trasparenza dell'effetto di riflessione. |

