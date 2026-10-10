---
title: "HorizontalRuleFormat"
linktitle: "HorizontalRuleFormat"
second_title: "Aspose.Words para Java"
description: "Representa el formato de regla horizontal en Java."
type: docs
weight: 376
url: /es/java/com.aspose.words/horizontalruleformat/
---

**Inheritance:**
java.lang.Object
```
public class HorizontalRuleFormat
```

Representa el formato de la regla horizontal.

Para obtener más información, visite el artículo de documentación [ Working with Shapes ][Working with Shapes].

 **Examples:** 

Muestra cómo insertar una forma de regla horizontal y personalizar su formato.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```


[Working with Shapes]: https://docs.aspose.com/words/java/working-with-shapes/
## Métodos

| Método | Descripción |
| --- | --- |
| [getAlignment()](#getAlignment) | Obtiene la alineación de la regla horizontal. |
| [getColor()](#getColor) | Obtiene el color del pincel que rellena la regla horizontal. |
| [getHeight()](#getHeight) | Obtiene la altura de la regla horizontal. |
| [getNoShade()](#getNoShade) | Indica la presencia de sombreado 3D para la regla horizontal. |
| [getWidthPercent()](#getWidthPercent) | Obtiene la longitud de la regla horizontal especificada expresada como un porcentaje del ancho de la ventana. |
| [setAlignment(int value)](#setAlignment-int) | Establece la alineación de la regla horizontal. |
| [setColor(Color value)](#setColor-java.awt.Color) | Establece el color del pincel que rellena la regla horizontal. |
| [setHeight(double value)](#setHeight-double) | Establece la altura de la regla horizontal. |
| [setNoShade(boolean value)](#setNoShade-boolean) | Indica la presencia de sombreado 3D para la regla horizontal. |
| [setWidthPercent(double value)](#setWidthPercent-double) | Establece la longitud de la regla horizontal especificada expresada como un porcentaje del ancho de la ventana. |
### getAlignment() {#getAlignment}
```
public int getAlignment()
```


Obtiene la alineación de la regla horizontal.

 **Remarks:** 

El valor predeterminado es [HorizontalRuleAlignment.LEFT](../../com.aspose.words/horizontalrulealignment/\#LEFT).

 **Examples:** 

Muestra cómo insertar una forma de regla horizontal y personalizar su formato.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Returns:**
int - La alineación de la regla horizontal. El valor devuelto es una de las constantes de [HorizontalRuleAlignment](../../com.aspose.words/horizontalrulealignment/).
### getColor() {#getColor}
```
public Color getColor()
```


Obtiene el color del pincel que rellena la regla horizontal.

 **Remarks:** 

Este es un acceso directo a la propiedad [Fill.getColor()](../../com.aspose.words/fill/\#getColor) / [Fill.setColor(java.awt.Color)](../../com.aspose.words/fill/\#setColor-java.awt.Color).

El valor predeterminado es java.awt.Color\#getGray().getGray().

 **Examples:** 

Muestra cómo insertar una forma de regla horizontal y personalizar su formato.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Returns:**
java.awt.Color - El color del pincel que rellena la regla horizontal.
### getHeight() {#getHeight}
```
public double getHeight()
```


Obtiene la altura de la regla horizontal.

**Returns:**
double - La altura de la regla horizontal.
### getNoShade() {#getNoShade}
```
public boolean getNoShade()
```


Indica la presencia de sombreado 3D para la regla horizontal. Si  true , entonces la regla horizontal no tiene sombreado 3D y se utiliza un color sólido.

 **Remarks:** 

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo insertar una forma de regla horizontal y personalizar su formato.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getWidthPercent() {#getWidthPercent}
```
public double getWidthPercent()
```


Obtiene la longitud de la regla horizontal especificada expresada como un porcentaje del ancho de la ventana.

**Returns:**
double - La longitud de la regla horizontal especificada expresada como un porcentaje del ancho de la ventana.
### setAlignment(int value) {#setAlignment-int}
```
public void setAlignment(int value)
```


Establece la alineación de la regla horizontal.

 **Remarks:** 

El valor predeterminado es [HorizontalRuleAlignment.LEFT](../../com.aspose.words/horizontalrulealignment/\#LEFT).

 **Examples:** 

Muestra cómo insertar una forma de regla horizontal y personalizar su formato.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | La alineación de la regla horizontal. El valor debe ser uno de los constantes de [HorizontalRuleAlignment](../../com.aspose.words/horizontalrulealignment/). |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Establece el color del pincel que rellena la regla horizontal.

 **Remarks:** 

Este es un acceso directo a la propiedad [Fill.getColor()](../../com.aspose.words/fill/\#getColor) / [Fill.setColor(java.awt.Color)](../../com.aspose.words/fill/\#setColor-java.awt.Color).

El valor predeterminado es java.awt.Color\#getGray().getGray().

 **Examples:** 

Muestra cómo insertar una forma de regla horizontal y personalizar su formato.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.awt.Color | El color del pincel que rellena la regla horizontal. |

### setHeight(double value) {#setHeight-double}
```
public void setHeight(double value)
```


Establece la altura de la regla horizontal.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | La altura de la regla horizontal. |

### setNoShade(boolean value) {#setNoShade-boolean}
```
public void setNoShade(boolean value)
```


Indica la presencia de sombreado 3D para la regla horizontal. Si  true , entonces la regla horizontal no tiene sombreado 3D y se utiliza un color sólido.

 **Remarks:** 

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo insertar una forma de regla horizontal y personalizar su formato.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setWidthPercent(double value) {#setWidthPercent-double}
```
public void setWidthPercent(double value)
```


Establece la longitud de la regla horizontal especificada expresada como un porcentaje del ancho de la ventana.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | La longitud de la regla horizontal especificada expresada como un porcentaje del ancho de la ventana. |

