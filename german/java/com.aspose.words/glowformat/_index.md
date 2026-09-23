---
title: "GlowFormat"
linktitle: "GlowFormat"
second_title: "Aspose.Words für Java"
description: "Stellt die Glow-Formatierung für ein Objekt in Java dar."
type: docs
weight: 358
url: /de/java/com.aspose.words/glowformat/
---

**Inheritance:**
java.lang.Object
```
public class GlowFormat
```

Stellt die Leuchteffekt-Formatierung für ein Objekt dar.

 **Remarks:** 

Verwenden Sie die [ShapeBase.getGlow()](../../com.aspose.words/shapebase/\#getGlow)-Eigenschaft, um auf die Glow-Eigenschaften eines Objekts zuzugreifen. Sie erstellen keine Instanzen der [GlowFormat](../../com.aspose.words/glowformat/)-Klasse direkt.

 **Examples:** 

Zeigt, wie man mit dem Glow-Formeffekt interagiert.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getColor()](#getColor) | Ruft ein java.awt.Color-Objekt ab, das die Farbe für einen Glow-Effekt darstellt. |
| [getRadius()](#getRadius) | Ruft einen double-Wert ab, der die Länge des Radius für einen Glow-Effekt in Punkten (pt) darstellt. |
| [getTransparency()](#getTransparency) | Ruft den Transparenzgrad für den Glow-Effekt als Wert zwischen 0.0 (undurchsichtig) und 1.0 (transparent) ab. |
| [remove()](#remove) | Entfernt [GlowFormat](../../com.aspose.words/glowformat/) aus dem übergeordneten Objekt. |
| [setColor(Color value)](#setColor-java.awt.Color) | Setzt ein java.awt.Color-Objekt, das die Farbe für einen Glow-Effekt darstellt. |
| [setRadius(double value)](#setRadius-double) | Setzt einen double-Wert, der die Länge des Radius für einen Glow-Effekt in Punkten (pt) darstellt. |
| [setTransparency(double value)](#setTransparency-double) | Setzt den Transparenzgrad für den Glow-Effekt als Wert zwischen 0.0 (undurchsichtig) und 1.0 (transparent). |
### getColor() {#getColor}
```
public Color getColor()
```


Ruft ein java.awt.Color-Objekt ab, das die Farbe für einen Glow-Effekt darstellt. Der Standardwert ist java.awt.Color\#getBlack().getBlack().

 **Examples:** 

Zeigt, wie man mit dem Glow-Formeffekt interagiert.

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
java.awt.Color - Ein java.awt.Color-Objekt, das die Farbe für einen Glow-Effekt darstellt.
### getRadius() {#getRadius}
```
public double getRadius()
```


Ruft einen double-Wert ab, der die Länge des Radius für einen Glow-Effekt in Punkten (pt) darstellt. Der Standardwert ist 0.0.

 **Examples:** 

Zeigt, wie man mit dem Glow-Formeffekt interagiert.

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
double - Ein double-Wert, der die Länge des Radius für einen Glow-Effekt in Punkten (pt) darstellt.
### getTransparency() {#getTransparency}
```
public double getTransparency()
```


Ruft den Transparenzgrad für den Glow-Effekt als Wert zwischen 0.0 (undurchsichtig) und 1.0 (transparent) ab. Der Standardwert ist 0.0.

 **Examples:** 

Zeigt, wie man mit dem Glow-Formeffekt interagiert.

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
double - Der Transparenzgrad für den Leuchteffekt als Wert zwischen 0.0 (undurchsichtig) und 1.0 (klar).
### remove() {#remove}
```
public void remove()
```


Entfernt [GlowFormat](../../com.aspose.words/glowformat/) aus dem übergeordneten Objekt.

 **Examples:** 

Zeigt, wie man mit dem Glow-Formeffekt interagiert.

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


Setzt ein java.awt.Color-Objekt, das die Farbe für einen Leuchteffekt darstellt. Der Standardwert ist java.awt.Color\\#getBlack().getBlack().

 **Examples:** 

Zeigt, wie man mit dem Glow-Formeffekt interagiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.awt.Color | Ein java.awt.Color-Objekt, das die Farbe für einen Leuchteffekt darstellt. |

### setRadius(double value) {#setRadius-double}
```
public void setRadius(double value)
```


Setzt einen double-Wert, der die Länge des Radius für einen Leuchteffekt in Punkten (pt) darstellt. Der Standardwert ist 0.0.

 **Examples:** 

Zeigt, wie man mit dem Glow-Formeffekt interagiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Ein double-Wert, der die Länge des Radius für einen Leuchteffekt in Punkten (pt) darstellt. |

### setTransparency(double value) {#setTransparency-double}
```
public void setTransparency(double value)
```


Setzt den Transparenzgrad für den Leuchteffekt als Wert zwischen 0.0 (undurchsichtig) und 1.0 (klar). Der Standardwert ist 0.0.

 **Examples:** 

Zeigt, wie man mit dem Glow-Formeffekt interagiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Der Transparenzgrad für den Leuchteffekt als Wert zwischen 0.0 (undurchsichtig) und 1.0 (klar). |

