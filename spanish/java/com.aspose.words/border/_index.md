---
title: "Borde"
linktitle: "Borde"
second_title: "Aspose.Words para Java"
description: "Representa un borde de un objeto en Java."
type: docs
weight: 46
url: /es/java/com.aspose.words/border/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.InternableComplexAttr](../../com.aspose.words/internablecomplexattr/)

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class Border extends InternableComplexAttr implements Cloneable
```

Representa un borde de un objeto.

Para obtener más información, visite el artículo de documentación [ Programming with Documents ][Programming with Documents].

 **Remarks:** 

Los bordes pueden aplicarse a varios elementos del documento, incluidos párrafos, secuencias de texto dentro de un párrafo o una celda de tabla.

 **Examples:** 

Muestra cómo insertar una cadena rodeada por un borde en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

Muestra cómo insertar un párrafo con un borde superior.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Border topBorder = builder.getParagraphFormat().getBorders().getByBorderType(BorderType.TOP);
 topBorder.setLineWidth(4.0d);
 topBorder.setLineStyle(LineStyle.DASH_SMALL_GAP);
 // Set ThemeColor only when LineWidth or LineStyle setted.
 topBorder.setThemeColor(ThemeColor.ACCENT_1);
 topBorder.setTintAndShade(0.25d);

 builder.writeln("Text with a top border.");

 doc.save(getArtifactsDir() + "Border.ParagraphTopBorder.docx");
 
```


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Métodos

| Método | Descripción |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Restablece las propiedades del borde a los valores predeterminados. |
| [equals(Border rhs)](#equals-com.aspose.words.Border) | Determina si el borde especificado es igual en valor al borde actual. |
| [equals(Object obj)](#equals-java.lang.Object) | Determina si el objeto especificado es igual en valor al objeto actual. |
| [getColor()](#getColor) | Obtiene el color del borde. |
| [getDistanceFromText()](#getDistanceFromText) | Obtiene la distancia del borde al texto o al borde de la página en puntos. |
| [getLineStyle()](#getLineStyle) | Obtiene el estilo del borde. |
| [getLineWidth()](#getLineWidth) | Obtiene el ancho del borde en puntos. |
| [getShadow()](#getShadow) | Obtiene un valor que indica si el borde tiene sombra. |
| [getThemeColor()](#getThemeColor) | Obtiene el color del tema en el esquema de colores aplicado que está asociado con este objeto Border. |
| [getTintAndShade()](#getTintAndShade) | Obtiene un valor double que aclara o oscurece un color. |
| [hashCode()](#hashCode) |  |
| [isInheritedComplexAttr()](#isInheritedComplexAttr) |  |
| [isVisible()](#isVisible) | Devuelve  true  si el [getLineStyle()](../../com.aspose.words/border/\#getLineStyle) / [setLineStyle(int)](../../com.aspose.words/border/\#setLineStyle-int) no es [LineStyle.NONE](../../com.aspose.words/linestyle/\#NONE). |
| [setColor(Color value)](#setColor-java.awt.Color) | Establece el color del borde. |
| [setDistanceFromText(double value)](#setDistanceFromText-double) | Establece la distancia del borde al texto o al borde de la página en puntos. |
| [setLineStyle(int value)](#setLineStyle-int) | Establece el estilo del borde. |
| [setLineWidth(double value)](#setLineWidth-double) | Establece el ancho del borde en puntos. |
| [setShadow(boolean value)](#setShadow-boolean) | Establece un valor que indica si el borde tiene sombra. |
| [setThemeColor(int value)](#setThemeColor-int) | Establece el color del tema en el esquema de colores aplicado que está asociado con este objeto Border. |
| [setTintAndShade(double value)](#setTintAndShade-double) | Establece un valor double que aclara o oscurece un color. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Restablece las propiedades del borde a los valores predeterminados.

 **Remarks:** 

Cuando las propiedades del borde se restablecen a los valores predeterminados, el borde es invisible.

 **Examples:** 

Muestra cómo eliminar bordes de un párrafo.

```

 Document doc = new Document(getMyDir() + "Borders.docx");

 // Each paragraph has an individual set of borders.
 // We can access the settings for the appearance of these borders via the paragraph format object.
 BorderCollection borders = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBorders();

 Assert.assertEquals(Color.RED.getRGB(), borders.get(0).getColor().getRGB());
 Assert.assertEquals(3.0d, borders.get(0).getLineWidth());
 Assert.assertEquals(LineStyle.SINGLE, borders.get(0).getLineStyle());
 Assert.assertTrue(borders.get(0).isVisible());

 // We can remove a border at once by running the ClearFormatting method.
 // Running this method on every border of a paragraph will remove all its borders.
 for (Border border : borders)
     border.clearFormatting();

 Assert.assertEquals(0, borders.get(0).getColor().getRGB());
 Assert.assertEquals(0.0d, borders.get(0).getLineWidth());
 Assert.assertEquals(LineStyle.NONE, borders.get(0).getLineStyle());
 Assert.assertFalse(borders.get(0).isVisible());

 doc.save(getArtifactsDir() + "Border.ClearFormatting.docx");
 
```

### equals(Border rhs) {#equals-com.aspose.words.Border}
```
public boolean equals(Border rhs)
```


Determina si el borde especificado es igual en valor al borde actual.

 **Examples:** 

Muestra cómo las colecciones de bordes pueden compartir elementos.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Paragraph 1.");
 builder.write("Paragraph 2.");

 // Since we used the same border configuration while creating
 // these paragraphs, their border collections share the same elements.
 BorderCollection firstParagraphBorders = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBorders();
 BorderCollection secondParagraphBorders = builder.getCurrentParagraph().getParagraphFormat().getBorders();
 for (int i = 0; i < firstParagraphBorders.getCount(); i++) {
     Assert.assertTrue(firstParagraphBorders.get(i).equals(secondParagraphBorders.get(i)));
     Assert.assertEquals(firstParagraphBorders.get(i).hashCode(), secondParagraphBorders.get(i).hashCode());
     Assert.assertFalse(firstParagraphBorders.get(i).isVisible());
 }

 for (Border border : secondParagraphBorders)
     border.setLineStyle(LineStyle.DOT_DASH);

 // After changing the line style of the borders in just the second paragraph,
 // the border collections no longer share the same elements.
 for (int i = 0; i < firstParagraphBorders.getCount(); i++) {
     Assert.assertFalse(firstParagraphBorders.get(i).equals(secondParagraphBorders.get(i)));
     Assert.assertNotEquals(firstParagraphBorders.get(i).hashCode(), secondParagraphBorders.get(i).hashCode());

     // Changing the appearance of an empty border makes it visible.
     Assert.assertTrue(secondParagraphBorders.get(i).isVisible());
 }

 doc.save(getArtifactsDir() + "Border.SharedElements.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| rhs | [Border](../../com.aspose.words/border/) |  |

**Returns:**
boolean
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Determina si el objeto especificado es igual en valor al objeto actual.

 **Examples:** 

Muestra cómo las colecciones de bordes pueden compartir elementos.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Paragraph 1.");
 builder.write("Paragraph 2.");

 // Since we used the same border configuration while creating
 // these paragraphs, their border collections share the same elements.
 BorderCollection firstParagraphBorders = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBorders();
 BorderCollection secondParagraphBorders = builder.getCurrentParagraph().getParagraphFormat().getBorders();
 for (int i = 0; i < firstParagraphBorders.getCount(); i++) {
     Assert.assertTrue(firstParagraphBorders.get(i).equals(secondParagraphBorders.get(i)));
     Assert.assertEquals(firstParagraphBorders.get(i).hashCode(), secondParagraphBorders.get(i).hashCode());
     Assert.assertFalse(firstParagraphBorders.get(i).isVisible());
 }

 for (Border border : secondParagraphBorders)
     border.setLineStyle(LineStyle.DOT_DASH);

 // After changing the line style of the borders in just the second paragraph,
 // the border collections no longer share the same elements.
 for (int i = 0; i < firstParagraphBorders.getCount(); i++) {
     Assert.assertFalse(firstParagraphBorders.get(i).equals(secondParagraphBorders.get(i)));
     Assert.assertNotEquals(firstParagraphBorders.get(i).hashCode(), secondParagraphBorders.get(i).hashCode());

     // Changing the appearance of an empty border makes it visible.
     Assert.assertTrue(secondParagraphBorders.get(i).isVisible());
 }

 doc.save(getArtifactsDir() + "Border.SharedElements.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getColor() {#getColor}
```
public Color getColor()
```


Obtiene el color del borde.

 **Examples:** 

Muestra cómo insertar una cadena rodeada por un borde en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

**Returns:**
java.awt.Color - El color del borde.
### getDistanceFromText() {#getDistanceFromText}
```
public double getDistanceFromText()
```


Obtiene la distancia del borde al texto o al borde de la página en puntos.

 **Remarks:** 

No tiene efecto y se restablecerá automáticamente a cero para los bordes de las celdas de tabla.

 **Examples:** 

Muestra cómo crear un borde de banda azul ancha en la parte superior de la primera página.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setBorderAlwaysInFront(false);
 pageSetup.setBorderDistanceFrom(PageBorderDistanceFrom.PAGE_EDGE);
 pageSetup.setBorderAppliesTo(PageBorderAppliesTo.FIRST_PAGE);

 Border border = pageSetup.getBorders().getByBorderType(BorderType.TOP);
 border.setLineStyle(LineStyle.SINGLE);
 border.setLineWidth(30.0);
 border.setColor(Color.BLUE);
 border.setDistanceFromText(0.0);

 doc.save(getArtifactsDir() + "PageSetup.PageBorderProperties.docx");
 
```

**Returns:**
double - Distancia del borde al texto o al borde de la página en puntos.
### getLineStyle() {#getLineStyle}
```
public int getLineStyle()
```


Obtiene el estilo del borde.

 **Remarks:** 

Si estableces el estilo de línea a none, entonces el ancho de línea se cambia automáticamente a cero.

 **Examples:** 

Muestra cómo insertar una cadena rodeada por un borde en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

**Returns:**
int - El estilo del borde. El valor devuelto es una de las constantes [LineStyle](../../com.aspose.words/linestyle/).
### getLineWidth() {#getLineWidth}
```
public double getLineWidth()
```


Obtiene el ancho del borde en puntos.

 **Remarks:** 

Si estableces un ancho de línea mayor que cero cuando el estilo de línea es none, el estilo de línea se cambia automáticamente a línea simple.

 **Examples:** 

Muestra cómo insertar una cadena rodeada por un borde en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

**Returns:**
double - El ancho del borde en puntos.
### getShadow() {#getShadow}
```
public boolean getShadow()
```


Obtiene un valor que indica si el borde tiene sombra.

 **Remarks:** 

En Microsoft Word, para que un borde tenga sombra, los bordes en los cuatro lados (izquierda, arriba, derecha e inferior) deben ser del mismo tipo, ancho, color y todos deben tener la propiedad Shadow establecida en  true .

 **Examples:** 

Muestra cómo crear un borde de página ondulado verde con sombra.

```

 Document doc = new Document();
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 pageSetup.getBorders().setLineStyle(LineStyle.DOUBLE_WAVE);
 pageSetup.getBorders().setLineWidth(2.0);
 pageSetup.getBorders().setColor(Color.GREEN);
 pageSetup.getBorders().setDistanceFromText(24.0);
 pageSetup.getBorders().setShadow(true);

 doc.save(getArtifactsDir() + "PageSetup.PageBorders.docx");
 
```

**Returns:**
boolean - Un valor que indica si el borde tiene sombra.
### getThemeColor() {#getThemeColor}
```
public int getThemeColor()
```


Obtiene el color del tema en el esquema de colores aplicado que está asociado con este objeto Border.

 **Examples:** 

Muestra cómo insertar un párrafo con un borde superior.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Border topBorder = builder.getParagraphFormat().getBorders().getByBorderType(BorderType.TOP);
 topBorder.setLineWidth(4.0d);
 topBorder.setLineStyle(LineStyle.DASH_SMALL_GAP);
 // Set ThemeColor only when LineWidth or LineStyle setted.
 topBorder.setThemeColor(ThemeColor.ACCENT_1);
 topBorder.setTintAndShade(0.25d);

 builder.writeln("Text with a top border.");

 doc.save(getArtifactsDir() + "Border.ParagraphTopBorder.docx");
 
```

**Returns:**
int - El color del tema en el esquema de colores aplicado que está asociado con este objeto Border. El valor devuelto es una de las constantes [ThemeColor](../../com.aspose.words/themecolor/).
### getTintAndShade() {#getTintAndShade}
```
public double getTintAndShade()
```


Obtiene un valor double que aclara o oscurece un color.

**Returns:**
double - Un valor double que aclara o oscurece un color.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### isInheritedComplexAttr() {#isInheritedComplexAttr}
```
public boolean isInheritedComplexAttr()
```




**Returns:**
boolean
### isVisible() {#isVisible}
```
public boolean isVisible()
```


Devuelve  true  si el [getLineStyle()](../../com.aspose.words/border/\#getLineStyle) / [setLineStyle(int)](../../com.aspose.words/border/\#setLineStyle-int) no es [LineStyle.NONE](../../com.aspose.words/linestyle/\#NONE).

 **Examples:** 

Muestra cómo eliminar bordes de un párrafo.

```

 Document doc = new Document(getMyDir() + "Borders.docx");

 // Each paragraph has an individual set of borders.
 // We can access the settings for the appearance of these borders via the paragraph format object.
 BorderCollection borders = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBorders();

 Assert.assertEquals(Color.RED.getRGB(), borders.get(0).getColor().getRGB());
 Assert.assertEquals(3.0d, borders.get(0).getLineWidth());
 Assert.assertEquals(LineStyle.SINGLE, borders.get(0).getLineStyle());
 Assert.assertTrue(borders.get(0).isVisible());

 // We can remove a border at once by running the ClearFormatting method.
 // Running this method on every border of a paragraph will remove all its borders.
 for (Border border : borders)
     border.clearFormatting();

 Assert.assertEquals(0, borders.get(0).getColor().getRGB());
 Assert.assertEquals(0.0d, borders.get(0).getLineWidth());
 Assert.assertEquals(LineStyle.NONE, borders.get(0).getLineStyle());
 Assert.assertFalse(borders.get(0).isVisible());

 doc.save(getArtifactsDir() + "Border.ClearFormatting.docx");
 
```

**Returns:**
boolean -  true  si el [getLineStyle()](../../com.aspose.words/border/\#getLineStyle) / [setLineStyle(int)](../../com.aspose.words/border/\#setLineStyle-int) no es [LineStyle.NONE](../../com.aspose.words/linestyle/\#NONE).
### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Establece el color del borde.

 **Examples:** 

Muestra cómo insertar una cadena rodeada por un borde en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.awt.Color | El color del borde. |

### setDistanceFromText(double value) {#setDistanceFromText-double}
```
public void setDistanceFromText(double value)
```


Establece la distancia del borde al texto o al borde de la página en puntos.

 **Remarks:** 

No tiene efecto y se restablecerá automáticamente a cero para los bordes de las celdas de tabla.

 **Examples:** 

Muestra cómo crear un borde de banda azul ancha en la parte superior de la primera página.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setBorderAlwaysInFront(false);
 pageSetup.setBorderDistanceFrom(PageBorderDistanceFrom.PAGE_EDGE);
 pageSetup.setBorderAppliesTo(PageBorderAppliesTo.FIRST_PAGE);

 Border border = pageSetup.getBorders().getByBorderType(BorderType.TOP);
 border.setLineStyle(LineStyle.SINGLE);
 border.setLineWidth(30.0);
 border.setColor(Color.BLUE);
 border.setDistanceFromText(0.0);

 doc.save(getArtifactsDir() + "PageSetup.PageBorderProperties.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | Distancia del borde al texto o al borde de la página en puntos. |

### setLineStyle(int value) {#setLineStyle-int}
```
public void setLineStyle(int value)
```


Establece el estilo del borde.

 **Remarks:** 

Si estableces el estilo de línea a none, entonces el ancho de línea se cambia automáticamente a cero.

 **Examples:** 

Muestra cómo insertar una cadena rodeada por un borde en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El estilo del borde. El valor debe ser una de las constantes [LineStyle](../../com.aspose.words/linestyle/). |

### setLineWidth(double value) {#setLineWidth-double}
```
public void setLineWidth(double value)
```


Establece el ancho del borde en puntos.

 **Remarks:** 

Si estableces un ancho de línea mayor que cero cuando el estilo de línea es none, el estilo de línea se cambia automáticamente a línea simple.

 **Examples:** 

Muestra cómo insertar una cadena rodeada por un borde en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | El ancho del borde en puntos. |

### setShadow(boolean value) {#setShadow-boolean}
```
public void setShadow(boolean value)
```


Establece un valor que indica si el borde tiene sombra.

 **Remarks:** 

En Microsoft Word, para que un borde tenga sombra, los bordes en los cuatro lados (izquierda, arriba, derecha e inferior) deben ser del mismo tipo, ancho, color y todos deben tener la propiedad Shadow establecida en  true .

 **Examples:** 

Muestra cómo crear un borde de página ondulado verde con sombra.

```

 Document doc = new Document();
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 pageSetup.getBorders().setLineStyle(LineStyle.DOUBLE_WAVE);
 pageSetup.getBorders().setLineWidth(2.0);
 pageSetup.getBorders().setColor(Color.GREEN);
 pageSetup.getBorders().setDistanceFromText(24.0);
 pageSetup.getBorders().setShadow(true);

 doc.save(getArtifactsDir() + "PageSetup.PageBorders.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Un valor que indica si el borde tiene sombra. |

### setThemeColor(int value) {#setThemeColor-int}
```
public void setThemeColor(int value)
```


Establece el color del tema en el esquema de colores aplicado que está asociado con este objeto Border.

 **Examples:** 

Muestra cómo insertar un párrafo con un borde superior.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Border topBorder = builder.getParagraphFormat().getBorders().getByBorderType(BorderType.TOP);
 topBorder.setLineWidth(4.0d);
 topBorder.setLineStyle(LineStyle.DASH_SMALL_GAP);
 // Set ThemeColor only when LineWidth or LineStyle setted.
 topBorder.setThemeColor(ThemeColor.ACCENT_1);
 topBorder.setTintAndShade(0.25d);

 builder.writeln("Text with a top border.");

 doc.save(getArtifactsDir() + "Border.ParagraphTopBorder.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El color del tema en el esquema de colores aplicado que está asociado con este objeto Border. El valor debe ser una de las constantes [ThemeColor](../../com.aspose.words/themecolor/). |

### setTintAndShade(double value) {#setTintAndShade-double}
```
public void setTintAndShade(double value)
```


Establece un valor double que aclara o oscurece un color.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | Un valor double que aclara o oscurece un color. |

