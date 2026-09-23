---
title: "GlowFormat"
linktitle: "GlowFormat"
second_title: "Aspose.Words per Java"
description: "Rappresenta la formattazione glow per un oggetto in Java."
type: docs
weight: 358
url: /it/java/com.aspose.words/glowformat/
---

**Inheritance:**
java.lang.Object
```
public class GlowFormat
```

Rappresenta la formattazione di bagliore per un oggetto.

 **Remarks:** 

Utilizza la proprietà [ShapeBase.getGlow()](../../com.aspose.words/shapebase/\#getGlow) per accedere alle proprietà di bagliore di un oggetto. Non crei istanze della classe [GlowFormat](../../com.aspose.words/glowformat/) direttamente.

 **Examples:** 

Mostra come interagire con l'effetto di bagliore della forma.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getColor()](#getColor) | Restituisce un oggetto java.awt.Color che rappresenta il colore per un effetto di bagliore. |
| [getRadius()](#getRadius) | Restituisce un valore double che rappresenta la lunghezza del raggio per un effetto di bagliore in punti (pt). |
| [getTransparency()](#getTransparency) | Restituisce il grado di trasparenza per l'effetto di bagliore come valore compreso tra 0.0 (opaco) e 1.0 (trasparente). |
| [remove()](#remove) | Rimuove [GlowFormat](../../com.aspose.words/glowformat/) dall'oggetto padre. |
| [setColor(Color value)](#setColor-java.awt.Color) | Imposta un oggetto java.awt.Color che rappresenta il colore per un effetto di bagliore. |
| [setRadius(double value)](#setRadius-double) | Imposta un valore double che rappresenta la lunghezza del raggio per un effetto di bagliore in punti (pt). |
| [setTransparency(double value)](#setTransparency-double) | Imposta il grado di trasparenza per l'effetto di bagliore come valore compreso tra 0.0 (opaco) e 1.0 (trasparente). |
### getColor() {#getColor}
```
public Color getColor()
```


Restituisce un oggetto java.awt.Color che rappresenta il colore per un effetto di bagliore. Il valore predefinito è java.awt.Color\#getBlack().getBlack().

 **Examples:** 

Mostra come interagire con l'effetto di bagliore della forma.

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
java.awt.Color - Un oggetto java.awt.Color che rappresenta il colore per un effetto di bagliore.
### getRadius() {#getRadius}
```
public double getRadius()
```


Restituisce un valore double che rappresenta la lunghezza del raggio per un effetto di bagliore in punti (pt). Il valore predefinito è 0.0.

 **Examples:** 

Mostra come interagire con l'effetto di bagliore della forma.

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
double - Un valore double che rappresenta la lunghezza del raggio per un effetto di bagliore in punti (pt).
### getTransparency() {#getTransparency}
```
public double getTransparency()
```


Restituisce il grado di trasparenza per l'effetto di bagliore come valore compreso tra 0.0 (opaco) e 1.0 (trasparente). Il valore predefinito è 0.0.

 **Examples:** 

Mostra come interagire con l'effetto di bagliore della forma.

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
double - Il grado di trasparenza per l'effetto di bagliore come valore compreso tra 0.0 (opaco) e 1.0 (trasparente).
### remove() {#remove}
```
public void remove()
```


Rimuove [GlowFormat](../../com.aspose.words/glowformat/) dall'oggetto padre.

 **Examples:** 

Mostra come interagire con l'effetto di bagliore della forma.

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


Imposta un oggetto java.awt.Color che rappresenta il colore per un effetto di bagliore. Il valore predefinito è java.awt.Color\#getBlack().getBlack().

 **Examples:** 

Mostra come interagire con l'effetto di bagliore della forma.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.awt.Color | Un oggetto java.awt.Color che rappresenta il colore per un effetto di bagliore. |

### setRadius(double value) {#setRadius-double}
```
public void setRadius(double value)
```


Imposta un valore double che rappresenta la lunghezza del raggio per un effetto di bagliore in punti (pt). Il valore predefinito è 0.0.

 **Examples:** 

Mostra come interagire con l'effetto di bagliore della forma.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | Un valore double che rappresenta la lunghezza del raggio per un effetto di bagliore in punti (pt). |

### setTransparency(double value) {#setTransparency-double}
```
public void setTransparency(double value)
```


Imposta il grado di trasparenza per l'effetto di bagliore come valore compreso tra 0.0 (opaco) e 1.0 (trasparente). Il valore predefinito è 0.0.

 **Examples:** 

Mostra come interagire con l'effetto di bagliore della forma.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | Il grado di trasparenza per l'effetto di bagliore come valore compreso tra 0.0 (opaco) e 1.0 (trasparente). |

