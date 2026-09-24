---
title: "Sombras"
linktitle: "Sombras"
second_title: "Aspose.Words para Java"
description: "Contiene atributos de sombreado para un objeto en Java."
type: docs
weight: 609
url: /es/java/com.aspose.words/shading/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.InternableComplexAttr](../../com.aspose.words/internablecomplexattr/)

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class Shading extends InternableComplexAttr implements Cloneable
```

Contiene atributos de sombreado para un objeto.

Para obtener más información, visite el artículo de documentación [ Programming with Documents ][Programming with Documents].

 **Examples:** 

Muestra cómo aplicar el color del borde y de sombreado al crear una tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Start a table and set a default color/thickness for its borders.
 Table table = builder.startTable();
 table.setBorders(LineStyle.SINGLE, 2.0, Color.BLACK);

 // Create a row with two cells with different background colors.
 builder.insertCell();
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.RED);
 builder.writeln("Row 1, Cell 1.");
 builder.insertCell();
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Row 1, Cell 2.");
 builder.endRow();

 // Reset cell formatting to disable the background colors
 // set a custom border thickness for all new cells created by the builder,
 // then build a second row.
 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().getBorders().getLeft().setLineWidth(4.0);
 builder.getCellFormat().getBorders().getRight().setLineWidth(4.0);
 builder.getCellFormat().getBorders().getTop().setLineWidth(4.0);
 builder.getCellFormat().getBorders().getBottom().setLineWidth(4.0);

 builder.insertCell();
 builder.writeln("Row 2, Cell 1.");
 builder.insertCell();
 builder.writeln("Row 2, Cell 2.");

 doc.save(getArtifactsDir() + "DocumentBuilder.TableBordersAndShading.docx");
 
```

Muestra cómo decorar texto con bordes y sombreado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BorderCollection borders = builder.getParagraphFormat().getBorders();
 borders.setDistanceFromText(20.0);
 borders.getByBorderType(BorderType.LEFT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.RIGHT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.TOP).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.BOTTOM).setLineStyle(LineStyle.DOUBLE);

 Shading shading = builder.getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_DIAGONAL_CROSS);
 shading.setBackgroundPatternColor(new Color(240, 128, 128));  // Light Coral
 shading.setForegroundPatternColor(new Color(255, 160, 122));  // Light Salmon

 builder.write("This paragraph is formatted with a double border and shading.");
 doc.save(getArtifactsDir() + "DocumentBuilder.ApplyBordersAndShading.docx");
 
```


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Métodos

| Método | Descripción |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Elimina el sombreado del objeto. |
| [equals(Shading rhs)](#equals-com.aspose.words.Shading) | Determina si el [Shading](../../com.aspose.words/shading/) especificado es igual en valor al [Shading](../../com.aspose.words/shading/) actual. |
| [equals(Object obj)](#equals-java.lang.Object) | Determina si el objeto especificado es igual en valor al objeto actual. |
| [getBackgroundPatternColor()](#getBackgroundPatternColor) | Obtiene el color que se aplica al fondo del objeto [Shading](../../com.aspose.words/shading/). |
| [getBackgroundPatternThemeColor()](#getBackgroundPatternThemeColor) | Obtiene el color del tema del patrón de fondo en el esquema de colores aplicado que está asociado con este objeto [Shading](../../com.aspose.words/shading/). |
| [getBackgroundTintAndShade()](#getBackgroundTintAndShade) | Obtiene un valor doble que aclara u oscurece un color de tema de fondo. |
| [getForegroundPatternColor()](#getForegroundPatternColor) | Obtiene el color que se aplica al primer plano del objeto [Shading](../../com.aspose.words/shading/). |
| [getForegroundPatternThemeColor()](#getForegroundPatternThemeColor) | Obtiene el color del tema del patrón de primer plano en el esquema de colores aplicado que está asociado con este objeto [Shading](../../com.aspose.words/shading/). |
| [getForegroundTintAndShade()](#getForegroundTintAndShade) | Obtiene un valor doble que aclara u oscurece un color de tema de primer plano. |
| [getTexture()](#getTexture) | Obtiene la textura del sombreado. |
| [hashCode()](#hashCode) |  |
| [isInheritedComplexAttr()](#isInheritedComplexAttr) |  |
| [setBackgroundPatternColor(Color value)](#setBackgroundPatternColor-java.awt.Color) | Establece el color que se aplica al fondo del objeto [Shading](../../com.aspose.words/shading/). |
| [setBackgroundPatternThemeColor(int value)](#setBackgroundPatternThemeColor-int) | Establece el color del tema del patrón de fondo en el esquema de colores aplicado que está asociado con este objeto [Shading](../../com.aspose.words/shading/). |
| [setBackgroundTintAndShade(double value)](#setBackgroundTintAndShade-double) | Establece un valor doble que aclara u oscurece un color de tema de fondo. |
| [setForegroundPatternColor(Color value)](#setForegroundPatternColor-java.awt.Color) | Establece el color que se aplica al primer plano del objeto [Shading](../../com.aspose.words/shading/). |
| [setForegroundPatternThemeColor(int value)](#setForegroundPatternThemeColor-int) | Establece el color del tema del patrón de primer plano en el esquema de colores aplicado que está asociado con este objeto [Shading](../../com.aspose.words/shading/). |
| [setForegroundTintAndShade(double value)](#setForegroundTintAndShade-double) | Establece un valor doble que aclara u oscurece un color de tema de primer plano. |
| [setTexture(int value)](#setTexture-int) | Establece la textura del sombreado. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Elimina el sombreado del objeto.

 **Examples:** 

Muestra cómo crear una tabla con bordes personalizados.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

### equals(Shading rhs) {#equals-com.aspose.words.Shading}
```
public boolean equals(Shading rhs)
```


Determina si el [Shading](../../com.aspose.words/shading/) especificado es igual en valor al [Shading](../../com.aspose.words/shading/) actual.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| rhs | [Shading](../../com.aspose.words/shading/) |  |

**Returns:**
boolean
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Determina si el objeto especificado es igual en valor al objeto actual.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getBackgroundPatternColor() {#getBackgroundPatternColor}
```
public Color getBackgroundPatternColor()
```


Obtiene el color que se aplica al fondo del objeto [Shading](../../com.aspose.words/shading/).

 **Examples:** 

Muestra cómo decorar texto con bordes y sombreado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BorderCollection borders = builder.getParagraphFormat().getBorders();
 borders.setDistanceFromText(20.0);
 borders.getByBorderType(BorderType.LEFT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.RIGHT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.TOP).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.BOTTOM).setLineStyle(LineStyle.DOUBLE);

 Shading shading = builder.getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_DIAGONAL_CROSS);
 shading.setBackgroundPatternColor(new Color(240, 128, 128));  // Light Coral
 shading.setForegroundPatternColor(new Color(255, 160, 122));  // Light Salmon

 builder.write("This paragraph is formatted with a double border and shading.");
 doc.save(getArtifactsDir() + "DocumentBuilder.ApplyBordersAndShading.docx");
 
```

**Returns:**
java.awt.Color - El color que se aplica al fondo del objeto [Shading](../../com.aspose.words/shading/).
### getBackgroundPatternThemeColor() {#getBackgroundPatternThemeColor}
```
public int getBackgroundPatternThemeColor()
```


Obtiene el color del tema del patrón de fondo en el esquema de colores aplicado que está asociado con este objeto [Shading](../../com.aspose.words/shading/).

 **Examples:** 

Muestra cómo establecer colores de primer plano y fondo para la textura del sombreado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shading shading = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_12_PT_5_PERCENT);
 shading.setForegroundPatternThemeColor(ThemeColor.DARK_1);
 shading.setBackgroundPatternThemeColor(ThemeColor.DARK_2);

 shading.setForegroundTintAndShade(0.5);
 shading.setBackgroundTintAndShade(-0.2);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5d);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.writeln("Foreground and background pattern colors for shading texture.");

 doc.save(getArtifactsDir() + "Font.ForegroundAndBackground.docx");
 
```

**Returns:**
int - El color del tema del patrón de fondo en el esquema de colores aplicado que está asociado con este objeto [Shading](../../com.aspose.words/shading/). El valor devuelto es una de las constantes [ThemeColor](../../com.aspose.words/themecolor/).
### getBackgroundTintAndShade() {#getBackgroundTintAndShade}
```
public double getBackgroundTintAndShade()
```


Obtiene un valor doble que aclara u oscurece un color de tema de fondo.

**Returns:**
double - Un valor doble que aclara u oscurece un color de tema de fondo.
### getForegroundPatternColor() {#getForegroundPatternColor}
```
public Color getForegroundPatternColor()
```


Obtiene el color que se aplica al primer plano del objeto [Shading](../../com.aspose.words/shading/).

 **Examples:** 

Muestra cómo decorar texto con bordes y sombreado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BorderCollection borders = builder.getParagraphFormat().getBorders();
 borders.setDistanceFromText(20.0);
 borders.getByBorderType(BorderType.LEFT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.RIGHT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.TOP).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.BOTTOM).setLineStyle(LineStyle.DOUBLE);

 Shading shading = builder.getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_DIAGONAL_CROSS);
 shading.setBackgroundPatternColor(new Color(240, 128, 128));  // Light Coral
 shading.setForegroundPatternColor(new Color(255, 160, 122));  // Light Salmon

 builder.write("This paragraph is formatted with a double border and shading.");
 doc.save(getArtifactsDir() + "DocumentBuilder.ApplyBordersAndShading.docx");
 
```

**Returns:**
java.awt.Color - El color que se aplica al primer plano del objeto [Shading](../../com.aspose.words/shading/).
### getForegroundPatternThemeColor() {#getForegroundPatternThemeColor}
```
public int getForegroundPatternThemeColor()
```


Obtiene el color del tema del patrón de primer plano en el esquema de colores aplicado que está asociado con este objeto [Shading](../../com.aspose.words/shading/).

 **Examples:** 

Muestra cómo establecer colores de primer plano y fondo para la textura del sombreado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shading shading = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_12_PT_5_PERCENT);
 shading.setForegroundPatternThemeColor(ThemeColor.DARK_1);
 shading.setBackgroundPatternThemeColor(ThemeColor.DARK_2);

 shading.setForegroundTintAndShade(0.5);
 shading.setBackgroundTintAndShade(-0.2);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5d);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.writeln("Foreground and background pattern colors for shading texture.");

 doc.save(getArtifactsDir() + "Font.ForegroundAndBackground.docx");
 
```

**Returns:**
int - El color del tema del patrón de primer plano en el esquema de colores aplicado que está asociado con este objeto [Shading](../../com.aspose.words/shading/). El valor devuelto es una de las constantes [ThemeColor](../../com.aspose.words/themecolor/).
### getForegroundTintAndShade() {#getForegroundTintAndShade}
```
public double getForegroundTintAndShade()
```


Obtiene un valor doble que aclara u oscurece un color de tema de primer plano.

**Returns:**
double - Un valor double que aclara o oscurece un color de tema de primer plano.
### getTexture() {#getTexture}
```
public int getTexture()
```


Obtiene la textura del sombreado.

 **Examples:** 

Muestra cómo decorar texto con bordes y sombreado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BorderCollection borders = builder.getParagraphFormat().getBorders();
 borders.setDistanceFromText(20.0);
 borders.getByBorderType(BorderType.LEFT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.RIGHT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.TOP).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.BOTTOM).setLineStyle(LineStyle.DOUBLE);

 Shading shading = builder.getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_DIAGONAL_CROSS);
 shading.setBackgroundPatternColor(new Color(240, 128, 128));  // Light Coral
 shading.setForegroundPatternColor(new Color(255, 160, 122));  // Light Salmon

 builder.write("This paragraph is formatted with a double border and shading.");
 doc.save(getArtifactsDir() + "DocumentBuilder.ApplyBordersAndShading.docx");
 
```

**Returns:**
int - La textura de sombreado. El valor devuelto es uno de los constantes de [TextureIndex](../../com.aspose.words/textureindex/).
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
### setBackgroundPatternColor(Color value) {#setBackgroundPatternColor-java.awt.Color}
```
public void setBackgroundPatternColor(Color value)
```


Establece el color que se aplica al fondo del objeto [Shading](../../com.aspose.words/shading/).

 **Examples:** 

Muestra cómo decorar texto con bordes y sombreado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BorderCollection borders = builder.getParagraphFormat().getBorders();
 borders.setDistanceFromText(20.0);
 borders.getByBorderType(BorderType.LEFT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.RIGHT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.TOP).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.BOTTOM).setLineStyle(LineStyle.DOUBLE);

 Shading shading = builder.getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_DIAGONAL_CROSS);
 shading.setBackgroundPatternColor(new Color(240, 128, 128));  // Light Coral
 shading.setForegroundPatternColor(new Color(255, 160, 122));  // Light Salmon

 builder.write("This paragraph is formatted with a double border and shading.");
 doc.save(getArtifactsDir() + "DocumentBuilder.ApplyBordersAndShading.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | java.awt.Color | El color que se aplica al fondo del objeto [Shading](../../com.aspose.words/shading/). |

### setBackgroundPatternThemeColor(int value) {#setBackgroundPatternThemeColor-int}
```
public void setBackgroundPatternThemeColor(int value)
```


Establece el color del tema del patrón de fondo en el esquema de colores aplicado que está asociado con este objeto [Shading](../../com.aspose.words/shading/).

 **Examples:** 

Muestra cómo establecer colores de primer plano y fondo para la textura del sombreado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shading shading = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_12_PT_5_PERCENT);
 shading.setForegroundPatternThemeColor(ThemeColor.DARK_1);
 shading.setBackgroundPatternThemeColor(ThemeColor.DARK_2);

 shading.setForegroundTintAndShade(0.5);
 shading.setBackgroundTintAndShade(-0.2);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5d);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.writeln("Foreground and background pattern colors for shading texture.");

 doc.save(getArtifactsDir() + "Font.ForegroundAndBackground.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El color de tema del patrón de fondo en el esquema de colores aplicado que está asociado a este objeto [Shading](../../com.aspose.words/shading/). El valor debe ser uno de los constantes de [ThemeColor](../../com.aspose.words/themecolor/). |

### setBackgroundTintAndShade(double value) {#setBackgroundTintAndShade-double}
```
public void setBackgroundTintAndShade(double value)
```


Establece un valor doble que aclara u oscurece un color de tema de fondo.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | Un valor double que aclara o oscurece un color de tema de fondo. |

### setForegroundPatternColor(Color value) {#setForegroundPatternColor-java.awt.Color}
```
public void setForegroundPatternColor(Color value)
```


Establece el color que se aplica al primer plano del objeto [Shading](../../com.aspose.words/shading/).

 **Examples:** 

Muestra cómo decorar texto con bordes y sombreado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BorderCollection borders = builder.getParagraphFormat().getBorders();
 borders.setDistanceFromText(20.0);
 borders.getByBorderType(BorderType.LEFT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.RIGHT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.TOP).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.BOTTOM).setLineStyle(LineStyle.DOUBLE);

 Shading shading = builder.getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_DIAGONAL_CROSS);
 shading.setBackgroundPatternColor(new Color(240, 128, 128));  // Light Coral
 shading.setForegroundPatternColor(new Color(255, 160, 122));  // Light Salmon

 builder.write("This paragraph is formatted with a double border and shading.");
 doc.save(getArtifactsDir() + "DocumentBuilder.ApplyBordersAndShading.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | java.awt.Color | El color que se aplica al primer plano del objeto [Shading](../../com.aspose.words/shading/). |

### setForegroundPatternThemeColor(int value) {#setForegroundPatternThemeColor-int}
```
public void setForegroundPatternThemeColor(int value)
```


Establece el color del tema del patrón de primer plano en el esquema de colores aplicado que está asociado con este objeto [Shading](../../com.aspose.words/shading/).

 **Examples:** 

Muestra cómo establecer colores de primer plano y fondo para la textura del sombreado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shading shading = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_12_PT_5_PERCENT);
 shading.setForegroundPatternThemeColor(ThemeColor.DARK_1);
 shading.setBackgroundPatternThemeColor(ThemeColor.DARK_2);

 shading.setForegroundTintAndShade(0.5);
 shading.setBackgroundTintAndShade(-0.2);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5d);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.writeln("Foreground and background pattern colors for shading texture.");

 doc.save(getArtifactsDir() + "Font.ForegroundAndBackground.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El color de tema del patrón de primer plano en el esquema de colores aplicado que está asociado a este objeto [Shading](../../com.aspose.words/shading/). El valor debe ser uno de los constantes de [ThemeColor](../../com.aspose.words/themecolor/). |

### setForegroundTintAndShade(double value) {#setForegroundTintAndShade-double}
```
public void setForegroundTintAndShade(double value)
```


Establece un valor doble que aclara u oscurece un color de tema de primer plano.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | Un valor double que aclara o oscurece un color de tema de primer plano. |

### setTexture(int value) {#setTexture-int}
```
public void setTexture(int value)
```


Establece la textura del sombreado.

 **Examples:** 

Muestra cómo decorar texto con bordes y sombreado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BorderCollection borders = builder.getParagraphFormat().getBorders();
 borders.setDistanceFromText(20.0);
 borders.getByBorderType(BorderType.LEFT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.RIGHT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.TOP).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.BOTTOM).setLineStyle(LineStyle.DOUBLE);

 Shading shading = builder.getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_DIAGONAL_CROSS);
 shading.setBackgroundPatternColor(new Color(240, 128, 128));  // Light Coral
 shading.setForegroundPatternColor(new Color(255, 160, 122));  // Light Salmon

 builder.write("This paragraph is formatted with a double border and shading.");
 doc.save(getArtifactsDir() + "DocumentBuilder.ApplyBordersAndShading.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | La textura de sombreado. El valor debe ser uno de los constantes de [TextureIndex](../../com.aspose.words/textureindex/). |

