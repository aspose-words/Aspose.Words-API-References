---
title: "ReflectionFormat"
linktitle: "ReflectionFormat"
second_title: "Aspose.Words pour Java"
description: "Représente le formatage de réflexion pour un objet en Java."
type: docs
weight: 560
url: /fr/java/com.aspose.words/reflectionformat/
---

**Inheritance:**
java.lang.Object
```
public class ReflectionFormat
```

Représente le formatage de réflexion pour un objet.

 **Remarks:** 

Utilisez la propriété [ShapeBase.getReflection()](../../com.aspose.words/shapebase/\#getReflection) pour accéder aux propriétés de réflexion d'un objet. Vous ne créez pas d'instances de la classe [ReflectionFormat](../../com.aspose.words/reflectionformat/) directement.

 **Examples:** 

Montre comment interagir avec l'effet de forme de réflexion.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [getBlur()](#getBlur) | Obtient une valeur double qui spécifie le degré d'effet de flou appliqué à l'effet de réflexion en points. |
| [getDistance()](#getDistance) | Obtient une valeur double qui spécifie la quantité de séparation de l'image réfléchie par rapport à l'objet en points. |
| [getSize()](#getSize) | Obtient une valeur double entre 0.0 et 1.0 représentant la taille de la réflexion en pourcentage de l'objet reflété. |
| [getTransparency()](#getTransparency) | Obtient une valeur double entre 0.0 (opaque) et 1.0 (transparent) représentant le degré de transparence de l'effet de réflexion. |
| [remove()](#remove) | Supprime [ReflectionFormat](../../com.aspose.words/reflectionformat/) de l'objet parent. |
| [setBlur(double value)](#setBlur-double) | Définit une valeur double qui spécifie le degré d'effet de flou appliqué à l'effet de réflexion en points. |
| [setDistance(double value)](#setDistance-double) | Définit une valeur double qui spécifie la quantité de séparation de l'image réfléchie par rapport à l'objet en points. |
| [setSize(double value)](#setSize-double) | Définit une valeur double entre 0.0 et 1.0 représentant la taille de la réflexion en pourcentage de l'objet reflété. |
| [setTransparency(double value)](#setTransparency-double) | Définit une valeur double entre 0.0 (opaque) et 1.0 (transparent) représentant le degré de transparence de l'effet de réflexion. |
### getBlur() {#getBlur}
```
public double getBlur()
```


Obtient une valeur double qui spécifie le degré d'effet de flou appliqué à l'effet de réflexion en points. La valeur par défaut est 0.0.

 **Examples:** 

Montre comment interagir avec l'effet de forme de réflexion.

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
double - Une valeur double qui spécifie le degré d'effet de flou appliqué à l'effet de réflexion en points.
### getDistance() {#getDistance}
```
public double getDistance()
```


Obtient une valeur double qui spécifie la quantité de séparation de l'image réfléchie par rapport à l'objet en points. La valeur par défaut est 0.0.

 **Examples:** 

Montre comment interagir avec l'effet de forme de réflexion.

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
double - Une valeur double qui spécifie la quantité de séparation de l'image réfléchie par rapport à l'objet en points.
### getSize() {#getSize}
```
public double getSize()
```


Obtient une valeur double entre 0.0 et 1.0 représentant la taille de la réflexion en pourcentage de l'objet reflété. La valeur par défaut est 0.0.

 **Examples:** 

Montre comment interagir avec l'effet de forme de réflexion.

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
double - Une valeur double entre 0.0 et 1.0 représentant la taille de la réflexion en pourcentage de l'objet reflété.
### getTransparency() {#getTransparency}
```
public double getTransparency()
```


Obtient une valeur double entre 0.0 (opaque) et 1.0 (transparent) représentant le degré de transparence de l'effet de réflexion. La valeur par défaut est 0.0.

 **Examples:** 

Montre comment interagir avec l'effet de forme de réflexion.

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
double - Une valeur double entre 0.0 (opaque) et 1.0 (transparent) représentant le degré de transparence de l'effet de réflexion.
### remove() {#remove}
```
public void remove()
```


Supprime [ReflectionFormat](../../com.aspose.words/reflectionformat/) de l'objet parent.

 **Examples:** 

Montre comment interagir avec l'effet de forme de réflexion.

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


Définit une valeur double qui spécifie le degré d'effet de flou appliqué à l'effet de réflexion en points. La valeur par défaut est 0.0.

 **Examples:** 

Montre comment interagir avec l'effet de forme de réflexion.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | Une valeur double qui spécifie le degré d'effet de flou appliqué à l'effet de réflexion en points. |

### setDistance(double value) {#setDistance-double}
```
public void setDistance(double value)
```


Définit une valeur double qui spécifie la quantité de séparation de l'image reflétée par rapport à l'objet en points. La valeur par défaut est 0.0.

 **Examples:** 

Montre comment interagir avec l'effet de forme de réflexion.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | Une valeur double qui spécifie la quantité de séparation de l'image reflétée par rapport à l'objet en points. |

### setSize(double value) {#setSize-double}
```
public void setSize(double value)
```


Définit une valeur double entre 0.0 et 1.0 représentant la taille de la réflexion en pourcentage de l'objet reflété. La valeur par défaut est 0.0.

 **Examples:** 

Montre comment interagir avec l'effet de forme de réflexion.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | Une valeur double entre 0.0 et 1.0 représentant la taille de la réflexion en pourcentage de l'objet reflété. |

### setTransparency(double value) {#setTransparency-double}
```
public void setTransparency(double value)
```


Définit une valeur double entre 0.0 (opaque) et 1.0 (transparent) représentant le degré de transparence de l'effet de réflexion. La valeur par défaut est 0.0.

 **Examples:** 

Montre comment interagir avec l'effet de forme de réflexion.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | Une valeur double entre 0.0 (opaque) et 1.0 (transparent) représentant le degré de transparence de l'effet de réflexion. |

