---
title: "ReflectionFormat"
linktitle: "ReflectionFormat"
second_title: "Aspose.Words para Java"
description: "Representa el formato de reflexión para un objeto en Java."
type: docs
weight: 560
url: /es/java/com.aspose.words/reflectionformat/
---

**Inheritance:**
java.lang.Object
```
public class ReflectionFormat
```

Representa el formato de reflexión para un objeto.

 **Remarks:** 

Utilice la propiedad [ShapeBase.getReflection()](../../com.aspose.words/shapebase/\#getReflection) para acceder a las propiedades de reflexión de un objeto. No crea instancias de la clase [ReflectionFormat](../../com.aspose.words/reflectionformat/) directamente.

 **Examples:** 

Muestra cómo interactuar con el efecto de forma de reflexión.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [getBlur()](#getBlur) | Obtiene un valor double que especifica el grado del efecto de desenfoque aplicado al efecto de reflexión en puntos. |
| [getDistance()](#getDistance) | Obtiene un valor double que especifica la cantidad de separación de la imagen reflejada del objeto en puntos. |
| [getSize()](#getSize) | Obtiene un valor double entre 0.0 y 1.0 que representa el tamaño de la reflexión como un porcentaje del objeto reflejado. |
| [getTransparency()](#getTransparency) | Obtiene un valor double entre 0.0 (opaco) y 1.0 (claro) que representa el grado de transparencia del efecto de reflexión. |
| [remove()](#remove) | Elimina [ReflectionFormat](../../com.aspose.words/reflectionformat/) del objeto padre. |
| [setBlur(double value)](#setBlur-double) | Establece un valor double que especifica el grado del efecto de desenfoque aplicado al efecto de reflexión en puntos. |
| [setDistance(double value)](#setDistance-double) | Establece un valor double que especifica la cantidad de separación de la imagen reflejada del objeto en puntos. |
| [setSize(double value)](#setSize-double) | Establece un valor double entre 0.0 y 1.0 que representa el tamaño de la reflexión como un porcentaje del objeto reflejado. |
| [setTransparency(double value)](#setTransparency-double) | Establece un valor double entre 0.0 (opaco) y 1.0 (claro) que representa el grado de transparencia del efecto de reflexión. |
### getBlur() {#getBlur}
```
public double getBlur()
```


Obtiene un valor double que especifica el grado del efecto de desenfoque aplicado al efecto de reflexión en puntos. El valor predeterminado es 0.0.

 **Examples:** 

Muestra cómo interactuar con el efecto de forma de reflexión.

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
double - Un valor double que especifica el grado del efecto de desenfoque aplicado al efecto de reflexión en puntos.
### getDistance() {#getDistance}
```
public double getDistance()
```


Obtiene un valor double que especifica la cantidad de separación de la imagen reflejada del objeto en puntos. El valor predeterminado es 0.0.

 **Examples:** 

Muestra cómo interactuar con el efecto de forma de reflexión.

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
double - Un valor double que especifica la cantidad de separación de la imagen reflejada del objeto en puntos.
### getSize() {#getSize}
```
public double getSize()
```


Obtiene un valor double entre 0.0 y 1.0 que representa el tamaño de la reflexión como un porcentaje del objeto reflejado. El valor predeterminado es 0.0.

 **Examples:** 

Muestra cómo interactuar con el efecto de forma de reflexión.

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
double - Un valor double entre 0.0 y 1.0 que representa el tamaño de la reflexión como un porcentaje del objeto reflejado.
### getTransparency() {#getTransparency}
```
public double getTransparency()
```


Obtiene un valor double entre 0.0 (opaco) y 1.0 (claro) que representa el grado de transparencia del efecto de reflexión. El valor predeterminado es 0.0.

 **Examples:** 

Muestra cómo interactuar con el efecto de forma de reflexión.

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
double - Un valor double entre 0.0 (opaco) y 1.0 (claro) que representa el grado de transparencia del efecto de reflexión.
### remove() {#remove}
```
public void remove()
```


Elimina [ReflectionFormat](../../com.aspose.words/reflectionformat/) del objeto padre.

 **Examples:** 

Muestra cómo interactuar con el efecto de forma de reflexión.

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


Establece un valor double que especifica el grado del efecto de desenfoque aplicado al efecto de reflexión en puntos. El valor predeterminado es 0.0.

 **Examples:** 

Muestra cómo interactuar con el efecto de forma de reflexión.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | Un valor double que especifica el grado del efecto de desenfoque aplicado al efecto de reflexión en puntos. |

### setDistance(double value) {#setDistance-double}
```
public void setDistance(double value)
```


Establece un valor doble que especifica la cantidad de separación de la imagen reflejada del objeto en puntos. El valor predeterminado es 0.0.

 **Examples:** 

Muestra cómo interactuar con el efecto de forma de reflexión.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | Un valor doble que especifica la cantidad de separación de la imagen reflejada del objeto en puntos. |

### setSize(double value) {#setSize-double}
```
public void setSize(double value)
```


Establece un valor doble entre 0.0 y 1.0 que representa el tamaño de la reflexión como un porcentaje del objeto reflejado. El valor predeterminado es 0.0.

 **Examples:** 

Muestra cómo interactuar con el efecto de forma de reflexión.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | Un valor doble entre 0.0 y 1.0 que representa el tamaño de la reflexión como un porcentaje del objeto reflejado. |

### setTransparency(double value) {#setTransparency-double}
```
public void setTransparency(double value)
```


Establece un valor doble entre 0.0 (opaco) y 1.0 (claro) que representa el grado de transparencia del efecto de reflexión. El valor predeterminado es 0.0.

 **Examples:** 

Muestra cómo interactuar con el efecto de forma de reflexión.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | Un valor doble entre 0.0 (opaco) y 1.0 (claro) que representa el grado de transparencia del efecto de reflexión. |

