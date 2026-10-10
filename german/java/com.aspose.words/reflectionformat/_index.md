---
title: "ReflectionFormat"
linktitle: "ReflectionFormat"
second_title: "Aspose.Words für Java"
description: "Stellt die Reflexionsformatierung für ein Objekt in Java dar."
type: docs
weight: 560
url: /de/java/com.aspose.words/reflectionformat/
---

**Inheritance:**
java.lang.Object
```
public class ReflectionFormat
```

Stellt die Reflexionsformatierung für ein Objekt dar.

 **Remarks:** 

Verwenden Sie die Eigenschaft [ShapeBase.getReflection()](../../com.aspose.words/shapebase/\#getReflection), um auf die Reflexionseigenschaften eines Objekts zuzugreifen. Sie erstellen keine Instanzen der Klasse [ReflectionFormat](../../com.aspose.words/reflectionformat/) direkt.

 **Examples:** 

Zeigt, wie man mit dem Reflexionsformen-Effekt interagiert.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getBlur()](#getBlur) | Gibt einen double-Wert zurück, der den Grad des Unschärfeeffekts angibt, der auf den Reflexionseffekt in Punkten angewendet wird. |
| [getDistance()](#getDistance) | Gibt einen double-Wert zurück, der den Abstand des reflektierten Bildes vom Objekt in Punkten angibt. |
| [getSize()](#getSize) | Gibt einen double-Wert zwischen 0.0 und 1.0 zurück, der die Größe der Reflexion als Prozentsatz des reflektierten Objekts darstellt. |
| [getTransparency()](#getTransparency) | Gibt einen double-Wert zwischen 0.0 (undurchsichtig) und 1.0 (transparent) zurück, der den Grad der Transparenz für den Reflexionseffekt darstellt. |
| [remove()](#remove) | Entfernt [ReflectionFormat](../../com.aspose.words/reflectionformat/) aus dem übergeordneten Objekt. |
| [setBlur(double value)](#setBlur-double) | Legt einen double-Wert fest, der den Grad des Unschärfeeffekts angibt, der auf den Reflexionseffekt in Punkten angewendet wird. |
| [setDistance(double value)](#setDistance-double) | Legt einen double-Wert fest, der den Abstand des reflektierten Bildes vom Objekt in Punkten angibt. |
| [setSize(double value)](#setSize-double) | Legt einen double-Wert zwischen 0.0 und 1.0 fest, der die Größe der Reflexion als Prozentsatz des reflektierten Objekts darstellt. |
| [setTransparency(double value)](#setTransparency-double) | Legt einen double-Wert zwischen 0.0 (undurchsichtig) und 1.0 (transparent) fest, der den Grad der Transparenz für den Reflexionseffekt darstellt. |
### getBlur() {#getBlur}
```
public double getBlur()
```


Gibt einen double-Wert zurück, der den Grad des Unschärfeeffekts angibt, der auf den Reflexionseffekt in Punkten angewendet wird. Der Standardwert ist 0.0.

 **Examples:** 

Zeigt, wie man mit dem Reflexionsformen-Effekt interagiert.

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
double - Ein double-Wert, der den Grad des Unschärfeeffekts angibt, der auf den Reflexionseffekt in Punkten angewendet wird.
### getDistance() {#getDistance}
```
public double getDistance()
```


Gibt einen double-Wert zurück, der den Abstand des reflektierten Bildes vom Objekt in Punkten angibt. Der Standardwert ist 0.0.

 **Examples:** 

Zeigt, wie man mit dem Reflexionsformen-Effekt interagiert.

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
double - Ein double-Wert, der den Abstand des reflektierten Bildes vom Objekt in Punkten angibt.
### getSize() {#getSize}
```
public double getSize()
```


Gibt einen double-Wert zwischen 0.0 und 1.0 zurück, der die Größe der Reflexion als Prozentsatz des reflektierten Objekts darstellt. Der Standardwert ist 0.0.

 **Examples:** 

Zeigt, wie man mit dem Reflexionsformen-Effekt interagiert.

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
double - Ein double-Wert zwischen 0.0 und 1.0, der die Größe der Reflexion als Prozentsatz des reflektierten Objekts darstellt.
### getTransparency() {#getTransparency}
```
public double getTransparency()
```


Gibt einen double-Wert zwischen 0.0 (undurchsichtig) und 1.0 (transparent) zurück, der den Grad der Transparenz für den Reflexionseffekt darstellt. Der Standardwert ist 0.0.

 **Examples:** 

Zeigt, wie man mit dem Reflexionsformen-Effekt interagiert.

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
double - Ein double-Wert zwischen 0.0 (undurchsichtig) und 1.0 (transparent), der den Grad der Transparenz für den Reflexionseffekt darstellt.
### remove() {#remove}
```
public void remove()
```


Entfernt [ReflectionFormat](../../com.aspose.words/reflectionformat/) aus dem übergeordneten Objekt.

 **Examples:** 

Zeigt, wie man mit dem Reflexionsformen-Effekt interagiert.

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


Legt einen double-Wert fest, der den Grad des Unschärfeeffekts angibt, der auf den Reflexionseffekt in Punkten angewendet wird. Der Standardwert ist 0.0.

 **Examples:** 

Zeigt, wie man mit dem Reflexionsformen-Effekt interagiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Ein double-Wert, der den Grad des Unschärfeeffekts angibt, der auf den Reflexionseffekt in Punkten angewendet wird. |

### setDistance(double value) {#setDistance-double}
```
public void setDistance(double value)
```


Legt einen double-Wert fest, der den Abstand des reflektierten Bildes vom Objekt in Punkten angibt. Der Standardwert ist 0.0.

 **Examples:** 

Zeigt, wie man mit dem Reflexionsformen-Effekt interagiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Ein Double-Wert, der die Menge der Trennung des reflektierten Bildes vom Objekt in Punkten angibt. |

### setSize(double value) {#setSize-double}
```
public void setSize(double value)
```


Legt einen Double-Wert zwischen 0.0 und 1.0 fest, der die Größe der Reflexion als Prozentsatz des reflektierten Objekts darstellt. Der Standardwert ist 0.0.

 **Examples:** 

Zeigt, wie man mit dem Reflexionsformen-Effekt interagiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Ein Double-Wert zwischen 0.0 und 1.0, der die Größe der Reflexion als Prozentsatz des reflektierten Objekts darstellt. |

### setTransparency(double value) {#setTransparency-double}
```
public void setTransparency(double value)
```


Legt einen Double-Wert zwischen 0.0 (undurchsichtig) und 1.0 (klar) fest, der den Grad der Transparenz für den Reflexionseffekt darstellt. Der Standardwert ist 0.0.

 **Examples:** 

Zeigt, wie man mit dem Reflexionsformen-Effekt interagiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Ein Double-Wert zwischen 0.0 (undurchsichtig) und 1.0 (klar), der den Grad der Transparenz für den Reflexionseffekt darstellt. |

