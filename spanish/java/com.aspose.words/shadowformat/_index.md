---
title: "ShadowFormat"
linktitle: "ShadowFormat"
second_title: "Aspose.Words para Java"
description: "Representa el formato de sombra para un objeto en Java."
type: docs
weight: 610
url: /es/java/com.aspose.words/shadowformat/
---

**Inheritance:**
java.lang.Object
```
public class ShadowFormat
```

Representa el formato de sombra para un objeto.

Para obtener más información, visite el artículo de documentación [ Working with Graphic Elements ][Working with Graphic Elements].

 **Examples:** 

Muestra cómo obtener el color de la sombra.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```


[Working with Graphic Elements]: https://docs.aspose.com/words/java/working-with-graphic-elements/
## Métodos

| Método | Descripción |
| --- | --- |
| [clear()](#clear) | Borra el formato de sombra. |
| [getColor()](#getColor) | Obtiene un objeto java.awt.Color que representa el color de la sombra. |
| [getTransparency()](#getTransparency) | Obtiene el grado de transparencia del efecto de sombra como un valor entre 0.0 (opaco) y 1.0 (claro). |
| [getType()](#getType) | Obtiene el [ShadowType](../../com.aspose.words/shadowtype/) especificado para ShadowFormat. |
| [getVisible()](#getVisible) | Devuelve  true  si el formato aplicado a esta instancia es visible. |
| [setColor(Color value)](#setColor-java.awt.Color) | Establece un objeto java.awt.Color que representa el color de la sombra. |
| [setTransparency(double value)](#setTransparency-double) | Establece el grado de transparencia del efecto de sombra como un valor entre 0.0 (opaco) y 1.0 (claro). |
| [setType(int value)](#setType-int) | Establece el [ShadowType](../../com.aspose.words/shadowtype/) especificado para ShadowFormat. |
### clear() {#clear}
```
public void clear()
```


Borra el formato de sombra.

 **Examples:** 

Muestra cómo trabajar con el formato de sombra para la forma.

```

 Document doc = new Document(getMyDir() + "Shape stroke pattern border.docx");
 Shape shape = (Shape)doc.getChildNodes(NodeType.SHAPE, true).get(0);

 if (shape.getShadowFormat().getVisible() && shape.getShadowFormat().getType() == ShadowType.SHADOW_2)
     shape.getShadowFormat().setType(ShadowType.SHADOW_7);

 if (shape.getShadowFormat().getType() == ShadowType.SHADOW_MIXED)
     shape.getShadowFormat().clear();
 
```

### getColor() {#getColor}
```
public Color getColor()
```


Obtiene un objeto java.awt.Color que representa el color de la sombra. El valor predeterminado es java.awt.Color\#getBlack().getBlack().

 **Examples:** 

Muestra cómo obtener el color de la sombra.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

Muestra cómo establecer un color con transparencia.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 ShadowFormat shadowFormat = shape.getShadowFormat();
 shadowFormat.setType(ShadowType.SHADOW_21);
 shadowFormat.setColor(Color.RED);
 shadowFormat.setTransparency(0.8);

 doc.save(getArtifactsDir() + "Shape.ShadowFormatTransparency.docx");
 
```

**Returns:**
java.awt.Color - Un objeto java.awt.Color que representa el color de la sombra.
### getTransparency() {#getTransparency}
```
public double getTransparency()
```


Obtiene el grado de transparencia del efecto de sombra como un valor entre 0.0 (opaco) y 1.0 (claro). El valor predeterminado es 0.0.

 **Examples:** 

Muestra cómo establecer un color con transparencia.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 ShadowFormat shadowFormat = shape.getShadowFormat();
 shadowFormat.setType(ShadowType.SHADOW_21);
 shadowFormat.setColor(Color.RED);
 shadowFormat.setTransparency(0.8);

 doc.save(getArtifactsDir() + "Shape.ShadowFormatTransparency.docx");
 
```

**Returns:**
double - El grado de transparencia del efecto de sombra como un valor entre 0.0 (opaco) y 1.0 (claro).
### getType() {#getType}
```
public int getType()
```


Obtiene el [ShadowType](../../com.aspose.words/shadowtype/) especificado para ShadowFormat.

 **Remarks:** 

Establecer un nuevo tipo de sombra restablecerá los valores de Color y Transparencia a sus valores predeterminados. Por lo tanto, tiene sentido establecer primero el tipo de sombra deseado y solo después los valores de Color y Transparencia.

 **Examples:** 

Muestra cómo obtener el color de la sombra.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

**Returns:**
int - El [ShadowType](../../com.aspose.words/shadowtype/) especificado para ShadowFormat. El valor devuelto es una de las constantes [ShadowType](../../com.aspose.words/shadowtype/).
### getVisible() {#getVisible}
```
public boolean getVisible()
```


Devuelve  true  si el formato aplicado a esta instancia es visible.

 **Remarks:** 

A diferencia de [clear()](../../com.aspose.words/shadowformat/\#clear), asignar  false  a Visible no borra el formato, solo oculta el efecto de forma.

 **Examples:** 

Muestra cómo trabajar con el formato de sombra para la forma.

```

 Document doc = new Document(getMyDir() + "Shape stroke pattern border.docx");
 Shape shape = (Shape)doc.getChildNodes(NodeType.SHAPE, true).get(0);

 if (shape.getShadowFormat().getVisible() && shape.getShadowFormat().getType() == ShadowType.SHADOW_2)
     shape.getShadowFormat().setType(ShadowType.SHADOW_7);

 if (shape.getShadowFormat().getType() == ShadowType.SHADOW_MIXED)
     shape.getShadowFormat().clear();
 
```

**Returns:**
boolean -  true  si el formato aplicado a esta instancia es visible.
### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Establece un objeto java.awt.Color que representa el color de la sombra. El valor predeterminado es java.awt.Color\#getBlack().getBlack().

 **Examples:** 

Muestra cómo obtener el color de la sombra.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

Muestra cómo establecer un color con transparencia.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 ShadowFormat shadowFormat = shape.getShadowFormat();
 shadowFormat.setType(ShadowType.SHADOW_21);
 shadowFormat.setColor(Color.RED);
 shadowFormat.setTransparency(0.8);

 doc.save(getArtifactsDir() + "Shape.ShadowFormatTransparency.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.awt.Color | Un objeto java.awt.Color que representa el color de la sombra. |

### setTransparency(double value) {#setTransparency-double}
```
public void setTransparency(double value)
```


Establece el grado de transparencia del efecto de sombra como un valor entre 0.0 (opaco) y 1.0 (claro). El valor predeterminado es 0.0.

 **Examples:** 

Muestra cómo establecer un color con transparencia.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 ShadowFormat shadowFormat = shape.getShadowFormat();
 shadowFormat.setType(ShadowType.SHADOW_21);
 shadowFormat.setColor(Color.RED);
 shadowFormat.setTransparency(0.8);

 doc.save(getArtifactsDir() + "Shape.ShadowFormatTransparency.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | El grado de transparencia del efecto de sombra como un valor entre 0.0 (opaco) y 1.0 (claro). |

### setType(int value) {#setType-int}
```
public void setType(int value)
```


Establece el [ShadowType](../../com.aspose.words/shadowtype/) especificado para ShadowFormat.

 **Remarks:** 

Establecer un nuevo tipo de sombra restablecerá los valores de Color y Transparencia a sus valores predeterminados. Por lo tanto, tiene sentido establecer primero el tipo de sombra deseado y solo después los valores de Color y Transparencia.

 **Examples:** 

Muestra cómo obtener el color de la sombra.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El [ShadowType](../../com.aspose.words/shadowtype/) especificado para ShadowFormat. El valor debe ser una de las constantes [ShadowType](../../com.aspose.words/shadowtype/). |

