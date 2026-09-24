---
title: "Font"
linktitle: "Font"
second_title: "Aspose.Words para Java"
description: "Contiene atributos de fuente como nombre de fuente, tamaño de fuente, color, etc., para un objeto en Java."
type: docs
weight: 319
url: /es/java/com.aspose.words/font/
---

**Inheritance:**
java.lang.Object
```
public class Font
```

Contiene atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) para un objeto.

Para obtener más información, visite el artículo de documentación [ Working with Fonts ][Working with Fonts].

 **Remarks:** 

No crea instancias de la clase [Font](../../com.aspose.words/font/) directamente. Simplemente usa [Font](../../com.aspose.words/font/) para acceder a las propiedades de fuente de varios objetos, como [Run](../../com.aspose.words/run/), [Paragraph](../../com.aspose.words/paragraph/), [Style](../../com.aspose.words/style/), [DocumentBuilder](../../com.aspose.words/documentbuilder/).

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

Muestra cómo formatear una secuencia de texto usando su propiedad de fuente.

```

 Document doc = new Document();
 Run run = new Run(doc, "Hello world!");

 Font font = run.getFont();
 font.setName("Courier New");
 font.setSize(36.0);
 font.setHighlightColor(Color.YELLOW);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(run);
 doc.save(getArtifactsDir() + "Font.CreateFormattedRun.docx");
 
```

Muestra cómo crear y usar un estilo de párrafo con formato de lista.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a custom paragraph style.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle1");
 style.getFont().setSize(24.0);
 style.getFont().setName("Verdana");
 style.getParagraphFormat().setSpaceAfter(12.0);

 // Create a list and make sure the paragraphs that use this style will use this list.
 style.getListFormat().setList(doc.getLists().add(ListTemplate.BULLET_DEFAULT));
 style.getListFormat().setListLevelNumber(0);

 // Apply the paragraph style to the document builder's current paragraph, and then add some text.
 builder.getParagraphFormat().setStyle(style);
 builder.writeln("Hello World: MyStyle1, bulleted list.");

 // Change the document builder's style to one that has no list formatting and write another paragraph.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln("Hello World: Normal.");

 builder.getDocument().save(getArtifactsDir() + "Styles.ParagraphStyleBulletedList.docx");
 
```


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## Métodos

| Método | Descripción |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Restablece el formato de fuente a los valores predeterminados. |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int) |  |
| [fetchInheritedShadingAttr(int key)](#fetchInheritedShadingAttr-int) |  |
| [getAllCaps()](#getAllCaps) | Verdadero si la fuente está formateada en mayúsculas. |
| [getAutoColor()](#getAutoColor) | Devuelve el color calculado actual del texto (negro o blanco) que se usará para 'color automático'. |
| [getBidi()](#getBidi) | Especifica si el contenido de este run debe tener características de derecha a izquierda. |
| [getBold()](#getBold) | True si la fuente está formateada en negrita. |
| [getBoldBi()](#getBoldBi) | Verdadero si el texto de derecha a izquierda está formateado en negrita. |
| [getBorder()](#getBorder) | Devuelve un objeto [Border](../../com.aspose.words/border/) que especifica el borde para la fuente. |
| [getColor()](#getColor) | Obtiene el color de la fuente. |
| [getComplexScript()](#getComplexScript) | Especifica si el contenido de este run debe tratarse como texto de escritura compleja sin importar sus valores de caracteres Unicode al determinar el formato de este run. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int) |  |
| [getDoubleStrikeThrough()](#getDoubleStrikeThrough) | Verdadero si la fuente está formateada con doble tachado. |
| [getEmboss()](#getEmboss) | Verdadero si la fuente está formateada como relieve. |
| [getEmphasisMark()](#getEmphasisMark) | Obtiene la marca de énfasis aplicada a este formato. |
| [getEngrave()](#getEngrave) | Verdadero si la fuente está formateada como grabada. |
| [getFill()](#getFill) | Obtiene el formato de relleno para la [Font](../../com.aspose.words/font/). |
| [getFillType()](#getFillType) |  |
| [getFillableBackColor()](#getFillableBackColor) |  |
| [getFillableBackThemeColor()](#getFillableBackThemeColor) |  |
| [getFillableBackTintAndShade()](#getFillableBackTintAndShade) |  |
| [getFillableBaseForeColor()](#getFillableBaseForeColor) |  |
| [getFillableForeColor()](#getFillableForeColor) |  |
| [getFillableForeThemeColor()](#getFillableForeThemeColor) |  |
| [getFillableForeTintAndShade()](#getFillableForeTintAndShade) |  |
| [getFillableImageBytes()](#getFillableImageBytes) |  |
| [getFillableTransparency()](#getFillableTransparency) |  |
| [getFillableVisible()](#getFillableVisible) |  |
| [getFilledColor()](#getFilledColor) |  |
| [getGradientAngle()](#getGradientAngle) |  |
| [getGradientStops()](#getGradientStops) |  |
| [getGradientStyle()](#getGradientStyle) |  |
| [getGradientVariant()](#getGradientVariant) |  |
| [getHidden()](#getHidden) | Verdadero si la fuente está formateada como texto oculto. |
| [getHighlightColor()](#getHighlightColor) | Obtiene el color de resaltado (marcador). |
| [getItalic()](#getItalic) | Verdadero si la fuente está formateada en cursiva. |
| [getItalicBi()](#getItalicBi) | Verdadero si el texto de derecha a izquierda está formateado como cursiva. |
| [getKerning()](#getKerning) | Obtiene el tamaño de fuente en el que comienza el kerning. |
| [getLineSpacing()](#getLineSpacing) | Devuelve el interlineado de esta fuente (en puntos). |
| [getLocaleId()](#getLocaleId) | Obtiene el identificador de configuración regional (idioma) de los caracteres formateados. |
| [getLocaleIdBi()](#getLocaleIdBi) | Obtiene el identificador de configuración regional (idioma) de los caracteres formateados de derecha a izquierda. |
| [getLocaleIdFarEast()](#getLocaleIdFarEast) | Obtiene el identificador de configuración regional (idioma) de los caracteres asiáticos formateados. |
| [getName()](#getName) | Obtiene el nombre de la fuente. |
| [getNameAscii()](#getNameAscii) | Obtiene la fuente utilizada para texto latino (caracteres con códigos de carácter del 0 (cero) al 127). |
| [getNameBi()](#getNameBi) | Obtiene el nombre de la fuente en un documento de idioma de derecha a izquierda. |
| [getNameFarEast()](#getNameFarEast) | Obtiene un nombre de fuente de Asia Oriental. |
| [getNameOther()](#getNameOther) | Obtiene la fuente utilizada para caracteres con códigos de carácter del 128 al 255. |
| [getNoProofing()](#getNoProofing) | Verdadero cuando los caracteres formateados no deben revisarse ortográficamente. |
| [getNumberSpacing()](#getNumberSpacing) | Obtiene el tipo de espaciado del número que se muestra. |
| [getOldOn()](#getOldOn) |  |
| [getOldOpacity()](#getOldOpacity) |  |
| [getOutline()](#getOutline) | Verdadero si la fuente está formateada como contorno. |
| [getPatternType()](#getPatternType) |  |
| [getPosition()](#getPosition) | Obtiene la posición del texto (en puntos) relativa a la línea base. |
| [getPresetTexture()](#getPresetTexture) |  |
| [getRotateWithObject()](#getRotateWithObject) |  |
| [getScaling()](#getScaling) | Obtiene el escalado del ancho de los caracteres en porcentaje. |
| [getShading()](#getShading) | Devuelve un objeto [Shading](../../com.aspose.words/shading/) que se refiere al formato de sombreado de la fuente. |
| [getShadow()](#getShadow) | Verdadero si la fuente está formateada como sombreada. |
| [getSize()](#getSize) | Obtiene el tamaño de fuente en puntos. |
| [getSizeBi()](#getSizeBi) | Obtiene el tamaño de fuente en puntos utilizado en un documento de derecha a izquierda. |
| [getSmallCaps()](#getSmallCaps) | Verdadero si la fuente está formateada en letras capitales pequeñas. |
| [getSnapToGrid()](#getSnapToGrid) | Especifica si la fuente actual debe usar la configuración de caracteres por línea de la cuadrícula del documento al diseñar. |
| [getSpacing()](#getSpacing) | Obtiene el espaciado (en puntos) entre caracteres. |
| [getStrikeThrough()](#getStrikeThrough) | Verdadero si la fuente está formateada como texto tachado. |
| [getStyle()](#getStyle) | Obtiene el estilo de carácter aplicado a este formato. |
| [getStyleIdentifier()](#getStyleIdentifier) | Obtiene el identificador de estilo independiente de la configuración regional del estilo de carácter aplicado a este formato. |
| [getStyleName()](#getStyleName) | Obtiene el nombre del estilo de carácter aplicado a este formato. |
| [getSubscript()](#getSubscript) | Verdadero si la fuente está formateada como subíndice. |
| [getSuperscript()](#getSuperscript) | Verdadero si la fuente está formateada como superíndice. |
| [getTextEffect()](#getTextEffect) | Obtiene el efecto de animación de la fuente. |
| [getTextureAlignment()](#getTextureAlignment) |  |
| [getThemeColor()](#getThemeColor) | Obtiene el color del tema en el esquema de colores aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/). |
| [getThemeFont()](#getThemeFont) | Obtiene la fuente del tema en el esquema de fuentes aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/). |
| [getThemeFontAscii()](#getThemeFontAscii) | Obtiene la fuente del tema utilizada para texto latino (caracteres con códigos de carácter de 0 (cero) a 127) en el esquema de fuentes aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/). |
| [getThemeFontBi()](#getThemeFontBi) | Obtiene la fuente del tema en el esquema de fuentes aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/) en un documento de idioma de derecha a izquierda. |
| [getThemeFontFarEast()](#getThemeFontFarEast) | Obtiene la fuente del tema de Asia Oriental en el esquema de fuentes aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/). |
| [getThemeFontOther()](#getThemeFontOther) | Obtiene la fuente del tema utilizada para caracteres con códigos de carácter de 128 a 255 en el esquema de fuentes aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/). |
| [getTintAndShade()](#getTintAndShade) | Obtiene un valor double que aclara o oscurece un color. |
| [getUnderline()](#getUnderline) | Obtiene el tipo de subrayado aplicado a la fuente. |
| [getUnderlineColor()](#getUnderlineColor) | Obtiene el color del subrayado aplicado a la fuente. |
| [hasDmlEffect(int dmlEffectType)](#hasDmlEffect-int) |  |
| [oneColorGradient(int style, int variant, double degree)](#oneColorGradient-int-int-double) |  |
| [patterned(int patternType)](#patterned-int) |  |
| [presetTextured(int presetTexture)](#presetTextured-int) |  |
| [setAllCaps(boolean value)](#setAllCaps-boolean) | Verdadero si la fuente está formateada en mayúsculas. |
| [setBidi(boolean value)](#setBidi-boolean) | Especifica si el contenido de este run debe tener características de derecha a izquierda. |
| [setBold(boolean value)](#setBold-boolean) | True si la fuente está formateada en negrita. |
| [setBoldBi(boolean value)](#setBoldBi-boolean) | Verdadero si el texto de derecha a izquierda está formateado en negrita. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object) |  |
| [setColor(Color value)](#setColor-java.awt.Color) | Establece el color de la fuente. |
| [setComplexScript(boolean value)](#setComplexScript-boolean) | Especifica si el contenido de este run debe tratarse como texto de escritura compleja sin importar sus valores de caracteres Unicode al determinar el formato de este run. |
| [setDoubleStrikeThrough(boolean value)](#setDoubleStrikeThrough-boolean) | Verdadero si la fuente está formateada con doble tachado. |
| [setEmboss(boolean value)](#setEmboss-boolean) | Verdadero si la fuente está formateada como relieve. |
| [setEmphasisMark(int value)](#setEmphasisMark-int) | Establece la marca de énfasis aplicada a este formato. |
| [setEngrave(boolean value)](#setEngrave-boolean) | Verdadero si la fuente está formateada como grabada. |
| [setFillableBackColor(Color value)](#setFillableBackColor-java.awt.Color) |  |
| [setFillableBackThemeColor(int value)](#setFillableBackThemeColor-int) |  |
| [setFillableBackTintAndShade(double value)](#setFillableBackTintAndShade-double) |  |
| [setFillableForeColor(Color value)](#setFillableForeColor-java.awt.Color) |  |
| [setFillableForeThemeColor(int value)](#setFillableForeThemeColor-int) |  |
| [setFillableForeTintAndShade(double value)](#setFillableForeTintAndShade-double) |  |
| [setFillableTransparency(double value)](#setFillableTransparency-double) |  |
| [setFillableVisible(boolean value)](#setFillableVisible-boolean) |  |
| [setFilledColor(Color value)](#setFilledColor-java.awt.Color) |  |
| [setGradientAngle(double value)](#setGradientAngle-double) |  |
| [setHidden(boolean value)](#setHidden-boolean) | Verdadero si la fuente está formateada como texto oculto. |
| [setHighlightColor(Color value)](#setHighlightColor-java.awt.Color) | Establece el color de resaltado (marcador). |
| [setImage(byte[] imageBytes)](#setImage-byte) |  |
| [setItalic(boolean value)](#setItalic-boolean) | Verdadero si la fuente está formateada en cursiva. |
| [setItalicBi(boolean value)](#setItalicBi-boolean) | Verdadero si el texto de derecha a izquierda está formateado como cursiva. |
| [setKerning(double value)](#setKerning-double) | Establece el tamaño de fuente en el que comienza el kerning. |
| [setLocaleId(int value)](#setLocaleId-int) | Establece el identificador de configuración regional (idioma) de los caracteres formateados. |
| [setLocaleIdBi(int value)](#setLocaleIdBi-int) | Establece el identificador de configuración regional (idioma) de los caracteres formateados de derecha a izquierda. |
| [setLocaleIdFarEast(int value)](#setLocaleIdFarEast-int) | Establece el identificador de configuración regional (idioma) de los caracteres asiáticos formateados. |
| [setName(String value)](#setName-java.lang.String) | Establece el nombre de la fuente. |
| [setNameAscii(String value)](#setNameAscii-java.lang.String) | Establece la fuente utilizada para texto latino (caracteres con códigos de carácter de 0 (cero) a 127). |
| [setNameBi(String value)](#setNameBi-java.lang.String) | Establece el nombre de la fuente en un documento de idioma de derecha a izquierda. |
| [setNameFarEast(String value)](#setNameFarEast-java.lang.String) | Establece un nombre de fuente de Asia Oriental. |
| [setNameOther(String value)](#setNameOther-java.lang.String) | Establece la fuente utilizada para los caracteres con códigos de carácter de 128 a 255. |
| [setNoProofing(boolean value)](#setNoProofing-boolean) | Verdadero cuando los caracteres formateados no deben revisarse ortográficamente. |
| [setNumberSpacing(int value)](#setNumberSpacing-int) | Establece el tipo de espaciado del número que se muestra. |
| [setOldOn(boolean value)](#setOldOn-boolean) |  |
| [setOldOpacity(double value)](#setOldOpacity-double) |  |
| [setOutline(boolean value)](#setOutline-boolean) | Verdadero si la fuente está formateada como contorno. |
| [setPosition(double value)](#setPosition-double) | Establece la posición del texto (en puntos) relativa a la línea base. |
| [setRotateWithObject(boolean value)](#setRotateWithObject-boolean) |  |
| [setScaling(int value)](#setScaling-int) | Establece la escala del ancho de carácter en porcentaje. |
| [setShadow(boolean value)](#setShadow-boolean) | Verdadero si la fuente está formateada como sombreada. |
| [setSize(double value)](#setSize-double) | Establece el tamaño de la fuente en puntos. |
| [setSizeBi(double value)](#setSizeBi-double) | Establece el tamaño de la fuente en puntos utilizado en un documento de derecha a izquierda. |
| [setSmallCaps(boolean value)](#setSmallCaps-boolean) | Verdadero si la fuente está formateada en letras capitales pequeñas. |
| [setSnapToGrid(boolean value)](#setSnapToGrid-boolean) | Especifica si la fuente actual debe usar la configuración de caracteres por línea de la cuadrícula del documento al diseñar. |
| [setSpacing(double value)](#setSpacing-double) | Establece el espaciado (en puntos) entre caracteres. |
| [setStrikeThrough(boolean value)](#setStrikeThrough-boolean) | Verdadero si la fuente está formateada como texto tachado. |
| [setStyle(Style value)](#setStyle-com.aspose.words.Style) | Establece el estilo de carácter aplicado a este formato. |
| [setStyleIdentifier(int value)](#setStyleIdentifier-int) | Establece el identificador de estilo independiente de la configuración regional del estilo de carácter aplicado a este formato. |
| [setStyleName(String value)](#setStyleName-java.lang.String) | Establece el nombre del estilo de carácter aplicado a este formato. |
| [setSubscript(boolean value)](#setSubscript-boolean) | Verdadero si la fuente está formateada como subíndice. |
| [setSuperscript(boolean value)](#setSuperscript-boolean) | Verdadero si la fuente está formateada como superíndice. |
| [setTextEffect(int value)](#setTextEffect-int) | Establece el efecto de animación de la fuente. |
| [setTextureAlignment(int value)](#setTextureAlignment-int) |  |
| [setThemeColor(int value)](#setThemeColor-int) | Establece el color del tema en el esquema de colores aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/). |
| [setThemeFont(int value)](#setThemeFont-int) | Establece la fuente del tema en el esquema de fuentes aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/). |
| [setThemeFontAscii(int value)](#setThemeFontAscii-int) | Establece la fuente del tema utilizada para texto latino (caracteres con códigos de carácter de 0 (cero) a 127) en el esquema de fuentes aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/). |
| [setThemeFontBi(int value)](#setThemeFontBi-int) | Establece la fuente del tema en el esquema de fuentes aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/) en un documento de idioma de derecha a izquierda. |
| [setThemeFontFarEast(int value)](#setThemeFontFarEast-int) | Establece la fuente del tema de Asia Oriental en el esquema de fuentes aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/). |
| [setThemeFontOther(int value)](#setThemeFontOther-int) | Establece la fuente del tema utilizada para caracteres con códigos de carácter de 128 a 255 en el esquema de fuentes aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/). |
| [setTintAndShade(double value)](#setTintAndShade-double) | Establece un valor double que aclara o oscurece un color. |
| [setUnderline(int value)](#setUnderline-int) | Establece el tipo de subrayado aplicado a la fuente. |
| [setUnderlineColor(Color value)](#setUnderlineColor-java.awt.Color) | Establece el color del subrayado aplicado a la fuente. |
| [solid()](#solid) |  |
| [twoColorGradient(int style, int variant)](#twoColorGradient-int-int) |  |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Restablece el formato de fuente a los valores predeterminados.

 **Remarks:** 

Elimina todo el formato de fuente especificado explícitamente en el objeto del que se obtuvo [Font](../../com.aspose.words/font/) para que el formato de fuente se herede del padre apropiado.

 **Examples:** 

Muestra cómo insertar un campo de hipervínculo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("For more information, please visit the ");

 // Insert a hyperlink and emphasize it with custom formatting.
 // The hyperlink will be a clickable piece of text which will take us to the location specified in the URL.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 builder.insertHyperlink("Google website", "https://www.google.com", false);
 builder.getFont().clearFormatting();
 builder.writeln(".");

 // Ctrl + left clicking the link in the text in Microsoft Word will take us to the URL via a new web browser window.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlink.docx");
 
```

### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int}
```
public Object fetchInheritedBorderAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedShadingAttr(int key) {#fetchInheritedShadingAttr-int}
```
public Object fetchInheritedShadingAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getAllCaps() {#getAllCaps}
```
public boolean getAllCaps()
```


Verdadero si la fuente está formateada en mayúsculas.

 **Examples:** 

Muestra cómo formatear una ejecución para mostrar su contenido en mayúsculas.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // There are two ways of getting a run to display its lowercase text in uppercase without changing the contents.
 // 1 -  Set the AllCaps flag to display all characters in regular capitals:
 Run run = new Run(doc, "all capitals");
 run.getFont().setAllCaps(true);
 para.appendChild(run);

 para = (Paragraph) para.getParentNode().appendChild(new Paragraph(doc));

 // 2 -  Set the SmallCaps flag to display all characters in small capitals:
 // If a character is lower case, it will appear in its upper case form
 // but will have the same height as the lower case (the font's x-height).
 // Characters that were in upper case originally will look the same.
 run = new Run(doc, "Small Capitals");
 run.getFont().setSmallCaps(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.Caps.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getAutoColor() {#getAutoColor}
```
public Color getAutoColor()
```


Devuelve el color calculado actual del texto (negro o blanco) que se usará para 'color automático'. Si el color no es 'automático', entonces devuelve [getColor()](../../com.aspose.words/font/\#getColor) / [setColor(java.awt.Color)](../../com.aspose.words/font/\#setColor-java.awt.Color).

 **Remarks:** 

Cuando el texto tiene 'color automático', el color real del texto se calcula automáticamente para que sea legible sobre el color de fondo. Al cambiar el color de fondo, el color del texto cambiará automáticamente a negro o blanco en MS Word para maximizar la legibilidad.

 **Examples:** 

Muestra cómo mejorar la legibilidad seleccionando automáticamente el color del texto según el brillo de su fondo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // If a run's Font object does not specify text color, it will automatically
 // select either black or white depending on the background color's color.
 Assert.assertEquals(0, builder.getFont().getColor().getRGB());

 // The default color for text is black. If the color of the background is dark, black text will be difficult to see.
 // To solve this problem, the AutoColor property will display this text in white.
 builder.getFont().getShading().setBackgroundPatternColor(Color.BLUE);

 builder.writeln("The text color automatically chosen for this run is white.");

 Assert.assertEquals(Color.WHITE.getRGB(), doc.getFirstSection().getBody().getParagraphs().get(0).getRuns().get(0).getFont().getAutoColor().getRGB());

 // If we change the background to a light color, black will be a more
 // suitable text color than white so that the auto color will display it in black.
 builder.getFont().getShading().setBackgroundPatternColor(Color.RED);

 builder.writeln("The text color automatically chosen for this run is black.");

 Assert.assertEquals(Color.BLACK.getRGB(), doc.getFirstSection().getBody().getParagraphs().get(1).getRuns().get(0).getFont().getAutoColor().getRGB());

 doc.save(getArtifactsDir() + "Font.SetFontAutoColor.docx");
 
```

**Returns:**
java.awt.Color - El color calculado actual del texto (negro o blanco) que se usará para 'auto color'.
### getBidi() {#getBidi}
```
public boolean getBidi()
```


Especifica si el contenido de este run debe tener características de derecha a izquierda.

 **Remarks:** 

Esta propiedad, cuando está activada, no debe usarse con texto fuertemente de izquierda a derecha. Cualquier comportamiento bajo esa condición no está especificado. Esta propiedad, cuando está desactivada, no debe usarse con texto fuertemente de derecha a izquierda. Cualquier comportamiento bajo esa condición no está especificado.

Cuando se muestra el contenido de esta ejecución, todos los caracteres deben tratarse como caracteres de script complejo para fines de formato. Esto significa que [getBoldBi()](../../com.aspose.words/font/\#getBoldBi) / [setBoldBi(boolean)](../../com.aspose.words/font/\#setBoldBi-boolean), [getItalicBi()](../../com.aspose.words/font/\#getItalicBi) / [setItalicBi(boolean)](../../com.aspose.words/font/\#setItalicBi-boolean), [getSizeBi()](../../com.aspose.words/font/\#getSizeBi) / [setSizeBi(double)](../../com.aspose.words/font/\#setSizeBi-double) y un nombre de fuente correspondiente se usarán al renderizar esta ejecución.

Además, cuando se muestra el contenido de esta ejecución, esta propiedad actúa como una sobrescritura de derecha a izquierda para los caracteres que se clasifican como "tipos débiles" y "tipos neutrales".

 **Examples:** 

Muestra cómo definir conjuntos separados de configuraciones de fuente para texto de derecha a izquierda, y texto de derecha a izquierda.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getBold() {#getBold}
```
public boolean getBold()
```


True si la fuente está formateada en negrita.

 **Examples:** 

Muestra cómo insertar texto con formato usando DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getBoldBi() {#getBoldBi}
```
public boolean getBoldBi()
```


Verdadero si el texto de derecha a izquierda está formateado en negrita.

 **Examples:** 

Muestra cómo definir conjuntos separados de configuraciones de fuente para texto de derecha a izquierda, y texto de derecha a izquierda.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getBorder() {#getBorder}
```
public Border getBorder()
```


Devuelve un objeto [Border](../../com.aspose.words/border/) que especifica el borde para la fuente.

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
[Border](../../com.aspose.words/border/) - A [Border](../../com.aspose.words/border/) object that specifies border for the font.
### getColor() {#getColor}
```
public Color getColor()
```


Obtiene el color de la fuente.

 **Examples:** 

Muestra cómo insertar texto con formato usando DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

Muestra cómo insertar un campo de hipervínculo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("For more information, please visit the ");

 // Insert a hyperlink and emphasize it with custom formatting.
 // The hyperlink will be a clickable piece of text which will take us to the location specified in the URL.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 builder.insertHyperlink("Google website", "https://www.google.com", false);
 builder.getFont().clearFormatting();
 builder.writeln(".");

 // Ctrl + left clicking the link in the text in Microsoft Word will take us to the URL via a new web browser window.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlink.docx");
 
```

**Returns:**
java.awt.Color - El color de la fuente.
### getComplexScript() {#getComplexScript}
```
public boolean getComplexScript()
```


Especifica si el contenido de este run debe tratarse como texto de escritura compleja sin importar sus valores de caracteres Unicode al determinar el formato de este run.

 **Examples:** 

Muestra cómo agregar texto que siempre se trata como script complejo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setComplexScript(true);

 builder.writeln("Text treated as complex script.");

 doc.save(getArtifactsDir() + "Font.ComplexScript.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int}
```
public Object getDirectBorderAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDoubleStrikeThrough() {#getDoubleStrikeThrough}
```
public boolean getDoubleStrikeThrough()
```


Verdadero si la fuente está formateada con doble tachado.

 **Examples:** 

Muestra cómo agregar una línea tachada al texto.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 Run run = new Run(doc, "Text with a single-line strikethrough.");
 run.getFont().setStrikeThrough(true);
 para.appendChild(run);

 para = (Paragraph) para.getParentNode().appendChild(new Paragraph(doc));

 run = new Run(doc, "Text with a double-line strikethrough.");
 run.getFont().setDoubleStrikeThrough(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.StrikeThrough.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getEmboss() {#getEmboss}
```
public boolean getEmboss()
```


Verdadero si la fuente está formateada como relieve.

 **Examples:** 

Muestra cómo aplicar efectos de grabado/relieve al texto.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(36.0);
 builder.getFont().setColor(Color.WHITE);

 // Below are two ways of using shadows to apply a 3D-like effect to the text.
 // 1 -  Engrave text to make it look like the letters are sunken into the page:
 builder.getFont().setEngrave(true);

 builder.writeln("This text is engraved.");

 // 2 -  Emboss text to make it look like the letters pop out of the page:
 builder.getFont().setEngrave(false);
 builder.getFont().setEmboss(true);

 builder.writeln("This text is embossed.");

 doc.save(getArtifactsDir() + "Font.EngraveEmboss.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getEmphasisMark() {#getEmphasisMark}
```
public int getEmphasisMark()
```


Obtiene la marca de énfasis aplicada a este formato.

 **Examples:** 

Muestra cómo agregar un carácter adicional renderizado arriba/abajo del glifo-carácter.

```

 DocumentBuilder builder = new DocumentBuilder();

 // Possible types of emphasis mark:
 // https://apireference.aspose.com/words/net/aspose.words/emphasismark
 builder.getFont().setEmphasisMark(emphasisMark);

 builder.write("Emphasis text");
 builder.writeln();
 builder.getFont().clearFormatting();
 builder.write("Simple text");

 builder.getDocument().save(getArtifactsDir() + "Fonts.SetEmphasisMark.docx");
 
```

**Returns:**
int - La marca de énfasis aplicada a este formato. El valor devuelto es una de las constantes de [EmphasisMark](../../com.aspose.words/emphasismark/).
### getEngrave() {#getEngrave}
```
public boolean getEngrave()
```


Verdadero si la fuente está formateada como grabada.

 **Examples:** 

Muestra cómo aplicar efectos de grabado/relieve al texto.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(36.0);
 builder.getFont().setColor(Color.WHITE);

 // Below are two ways of using shadows to apply a 3D-like effect to the text.
 // 1 -  Engrave text to make it look like the letters are sunken into the page:
 builder.getFont().setEngrave(true);

 builder.writeln("This text is engraved.");

 // 2 -  Emboss text to make it look like the letters pop out of the page:
 builder.getFont().setEngrave(false);
 builder.getFont().setEmboss(true);

 builder.writeln("This text is embossed.");

 doc.save(getArtifactsDir() + "Font.EngraveEmboss.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getFill() {#getFill}
```
public Fill getFill()
```


Obtiene el formato de relleno para la [Font](../../com.aspose.words/font/).

 **Examples:** 

Muestra cómo convertir cualquiera de los rellenos de nuevo a un relleno sólido.

```

 Document doc = new Document(getMyDir() + "Two color gradient.docx");

 // Get Fill object for Font of the first Run.
 Fill fill = doc.getFirstSection().getBody().getParagraphs().get(0).getRuns().get(0).getFont().getFill();

 // Check Fill properties of the Font.
 System.out.println(MessageFormat.format("The type of the fill is: {0}",fill.getFillType()));
 System.out.println(MessageFormat.format("The foreground color of the fill is: {0}",fill.getForeColor()));
 System.out.println(MessageFormat.format("The fill is transparent at {0}%",fill.getTransparency() * 100.0));

 // Change type of the fill to Solid with uniform green color.
 fill.solid(Color.GREEN);
 System.out.println("\nThe fill is changed:");
 System.out.println(MessageFormat.format("The type of the fill is: {0}",fill.getFillType()));
 System.out.println(MessageFormat.format("The foreground color of the fill is: {0}",fill.getForeColor()));
 System.out.println(MessageFormat.format("The fill transparency is {0}%",fill.getTransparency() * 100.0));

 doc.save(getArtifactsDir() + "Drawing.FillSolid.docx");
 
```

**Returns:**
[Fill](../../com.aspose.words/fill/) - Fill formatting for the [Font](../../com.aspose.words/font/).
### getFillType() {#getFillType}
```
public int getFillType()
```




**Returns:**
int
### getFillableBackColor() {#getFillableBackColor}
```
public Color getFillableBackColor()
```




**Returns:**
java.awt.Color
### getFillableBackThemeColor() {#getFillableBackThemeColor}
```
public int getFillableBackThemeColor()
```




**Returns:**
int
### getFillableBackTintAndShade() {#getFillableBackTintAndShade}
```
public double getFillableBackTintAndShade()
```




**Returns:**
double
### getFillableBaseForeColor() {#getFillableBaseForeColor}
```
public Color getFillableBaseForeColor()
```




**Returns:**
java.awt.Color
### getFillableForeColor() {#getFillableForeColor}
```
public Color getFillableForeColor()
```




**Returns:**
java.awt.Color
### getFillableForeThemeColor() {#getFillableForeThemeColor}
```
public int getFillableForeThemeColor()
```




**Returns:**
int
### getFillableForeTintAndShade() {#getFillableForeTintAndShade}
```
public double getFillableForeTintAndShade()
```




**Returns:**
double
### getFillableImageBytes() {#getFillableImageBytes}
```
public byte[] getFillableImageBytes()
```




**Returns:**
byte[]
### getFillableTransparency() {#getFillableTransparency}
```
public double getFillableTransparency()
```




**Returns:**
double
### getFillableVisible() {#getFillableVisible}
```
public boolean getFillableVisible()
```




**Returns:**
boolean
### getFilledColor() {#getFilledColor}
```
public Color getFilledColor()
```




**Returns:**
java.awt.Color
### getGradientAngle() {#getGradientAngle}
```
public double getGradientAngle()
```




**Returns:**
double
### getGradientStops() {#getGradientStops}
```
public GradientStopCollection getGradientStops()
```




**Returns:**
[GradientStopCollection](../../com.aspose.words/gradientstopcollection/)
### getGradientStyle() {#getGradientStyle}
```
public int getGradientStyle()
```




**Returns:**
int
### getGradientVariant() {#getGradientVariant}
```
public int getGradientVariant()
```




**Returns:**
int
### getHidden() {#getHidden}
```
public boolean getHidden()
```


Verdadero si la fuente está formateada como texto oculto.

 **Examples:** 

Muestra cómo crear una ejecución de texto oculto.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // With the Hidden flag set to true, any text that we create using this Font object will be invisible in the document.
 // We will not see or highlight hidden text unless we enable the "Hidden text" option
 // found in Microsoft Word via "File" -> "Options" -> "Display". The text will still be there,
 // and we will be able to access this text programmatically.
 // It is not advised to use this method to hide sensitive information.
 builder.getFont().setHidden(true);
 builder.getFont().setSize(36.0);

 builder.writeln("This text will not be visible in the document.");

 doc.save(getArtifactsDir() + "Font.Hidden.docx");
 
```

Muestra cómo usar una implementación de DocumentVisitor para eliminar todo el contenido oculto de un documento.

```

 public void removeHiddenContentFromDocument() throws Exception {
     Document doc = new Document(getMyDir() + "Hidden content.docx");
     RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

     // Below are three types of fields which can accept a document visitor,
     // which will allow it to visit the accepting node, and then traverse its child nodes in a depth-first manner.
     // 1 -  Paragraph node:
     Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 4, true);
     para.accept(hiddenContentRemover);

     // 2 -  Table node:
     Table table = doc.getFirstSection().getBody().getTables().get(0);
     table.accept(hiddenContentRemover);

     // 3 -  Document node:
     doc.accept(hiddenContentRemover);

     doc.save(getArtifactsDir() + "Font.RemoveHiddenContentFromDocument.docx");
 }

 /// 
 /// Removes all visited nodes marked as "hidden content".
 /// 
 public static class RemoveHiddenContentVisitor extends DocumentVisitor {
     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(FieldStart fieldStart) {
         if (fieldStart.getFont().getHidden())
             fieldStart.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(FieldEnd fieldEnd) {
         if (fieldEnd.getFont().getHidden())
             fieldEnd.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(FieldSeparator fieldSeparator) {
         if (fieldSeparator.getFont().getHidden())
             fieldSeparator.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(Run run) {
         if (run.getFont().getHidden())
             run.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(Paragraph paragraph) {
         if (paragraph.getParagraphBreakFont().getHidden())
             paragraph.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FormField is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         if (formField.getFont().getHidden())
             formField.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a GroupShape is encountered in the document.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         if (groupShape.getFont().getHidden())
             groupShape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Shape is encountered in the document.
     /// 
     public int visitShapeStart(Shape shape) {
         if (shape.getFont().getHidden())
             shape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Comment is encountered in the document.
     /// 
     public int visitCommentStart(Comment comment) {
         if (comment.getFont().getHidden())
             comment.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Footnote is encountered in the document.
     /// 
     public int visitFootnoteStart(Footnote footnote) {
         if (footnote.getFont().getHidden())
             footnote.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SpecialCharacter is encountered in the document.
     /// 
     public int visitSpecialChar(SpecialChar specialChar) {
         if (specialChar.getFont().getHidden())
             specialChar.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Table node is ended in the document.
     /// 
     public int visitTableEnd(Table table) {
         // The content inside table cells may have the hidden content flag, but the tables themselves cannot.
         // If this table had nothing but hidden content, this visitor would have removed all of it,
         // and there would be no child nodes left.
         // Thus, we can also treat the table itself as hidden content and remove it.
         // Tables which are empty but do not have hidden content will have cells with empty paragraphs inside,
         // which this visitor will not remove.
         if (!table.hasChildNodes())
             table.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Cell node is ended in the document.
     /// 
     public int visitCellEnd(Cell cell) {
         if (!cell.hasChildNodes() && cell.getParentNode() != null)
             cell.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Row node is ended in the document.
     /// 
     public int visitRowEnd(Row row) {
         if (!row.hasChildNodes() && row.getParentNode() != null)
             row.remove();

         return VisitorAction.CONTINUE;
     }
 }
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getHighlightColor() {#getHighlightColor}
```
public Color getHighlightColor()
```


Obtiene el color de resaltado (marcador).

 **Examples:** 

Muestra cómo formatear una secuencia de texto usando su propiedad de fuente.

```

 Document doc = new Document();
 Run run = new Run(doc, "Hello world!");

 Font font = run.getFont();
 font.setName("Courier New");
 font.setSize(36.0);
 font.setHighlightColor(Color.YELLOW);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(run);
 doc.save(getArtifactsDir() + "Font.CreateFormattedRun.docx");
 
```

**Returns:**
java.awt.Color - El color de resaltado (marcador).
### getItalic() {#getItalic}
```
public boolean getItalic()
```


Verdadero si la fuente está formateada en cursiva.

 **Examples:** 

Muestra cómo escribir texto en cursiva usando un document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(36.0);
 builder.getFont().setItalic(true);
 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "Font.Italic.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getItalicBi() {#getItalicBi}
```
public boolean getItalicBi()
```


Verdadero si el texto de derecha a izquierda está formateado como cursiva.

 **Examples:** 

Muestra cómo definir conjuntos separados de configuraciones de fuente para texto de derecha a izquierda, y texto de derecha a izquierda.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getKerning() {#getKerning}
```
public double getKerning()
```


Obtiene el tamaño de fuente en el que comienza el kerning.

 **Examples:** 

Muestra cómo especificar el tamaño de fuente en el que el kerning comienza a tener efecto.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setName("Arial Black");

 // Set the builder's font size, and minimum size at which kerning will take effect.
 // The font size falls below the kerning threshold, so the run bellow will not have kerning.
 builder.getFont().setSize(18.0);
 builder.getFont().setKerning(24.0);

 builder.writeln("TALLY. (Kerning not applied)");

 // Set the kerning threshold so that the builder's current font size is above it.
 // Any text we add from this point will have kerning applied. The spaces between characters
 // will be adjusted, normally resulting in a slightly more aesthetically pleasing text run.
 builder.getFont().setKerning(12.0);

 builder.writeln("TALLY. (Kerning applied)");

 doc.save(getArtifactsDir() + "Font.Kerning.docx");
 
```

**Returns:**
double - El tamaño de fuente en el que comienza el kerning.
### getLineSpacing() {#getLineSpacing}
```
public double getLineSpacing()
```


Devuelve el interlineado de esta fuente (en puntos).

 **Examples:** 

Muestra cómo obtener el interlineado de una fuente, en puntos.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set different fonts for the DocumentBuilder, and verify their line spacing.
 builder.getFont().setName("Calibri");
 Assert.assertEquals(13.7d, builder.getFont().getLineSpacing(), 1);

 builder.getFont().setName("Times New Roman");
 Assert.assertEquals(13.7d, builder.getFont().getLineSpacing(), 1);
 
```

**Returns:**
double - Interlineado de esta fuente (en puntos).
### getLocaleId() {#getLocaleId}
```
public int getLocaleId()
```


Obtiene el identificador de configuración regional (idioma) de los caracteres formateados.

 **Remarks:** 

Para la lista de identificadores de configuración regional, consulte https://msdn.microsoft.com/en-us/library/cc233965.aspx

 **Examples:** 

Muestra cómo establecer la configuración regional del texto que estamos agregando con un document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // If we set the font's locale to English and insert some Russian text,
 // the English locale spell checker will not recognize the text and detect it as a spelling error.
 builder.getFont().setLocaleId(1033);
 builder.writeln("\u041f\u0440\u0438\u0432\u0435\u0442!");

 // Set a matching locale for the text that we are about to add to apply the appropriate spell checker.
 builder.getFont().setLocaleId(1049);
 builder.writeln("\u041f\u0440\u0438\u0432\u0435\u0442!");

 doc.save(getArtifactsDir() + "Font.LocaleId.docx");
 
```

**Returns:**
int - El identificador de configuración regional (idioma) de los caracteres formateados.
### getLocaleIdBi() {#getLocaleIdBi}
```
public int getLocaleIdBi()
```


Obtiene el identificador de configuración regional (idioma) de los caracteres formateados de derecha a izquierda.

 **Remarks:** 

Para la lista de identificadores de configuración regional, consulte https://msdn.microsoft.com/en-us/library/cc233965.aspx

 **Examples:** 

Muestra cómo definir conjuntos separados de configuraciones de fuente para texto de derecha a izquierda, y texto de derecha a izquierda.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Returns:**
int - El identificador de configuración regional (idioma) de los caracteres formateados de derecha a izquierda.
### getLocaleIdFarEast() {#getLocaleIdFarEast}
```
public int getLocaleIdFarEast()
```


Obtiene el identificador de configuración regional (idioma) de los caracteres asiáticos formateados.

 **Remarks:** 

Para la lista de identificadores de configuración regional, consulte https://msdn.microsoft.com/en-us/library/cc233965.aspx

 **Examples:** 

Muestra cómo insertar y formatear texto en un idioma del Lejano Oriente.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font settings that the document builder will apply to any text that it inserts.
 builder.getFont().setName("Courier New");
 builder.getFont().setLocaleId(1033);

 // Name "FarEast" equivalents for our font and locale.
 // If the builder inserts Asian characters with this Font configuration, then each run that contains
 // these characters will display them using the "FarEast" font/locale instead of the default.
 // This could be useful when a western font does not have ideal representations for Asian characters.
 builder.getFont().setNameFarEast("SimSun");
 builder.getFont().setLocaleIdFarEast(2052);

 // This text will be displayed in the default font/locale.
 builder.writeln("Hello world!");

 // Since these are Asian characters, this run will apply our "FarEast" font/locale equivalents.
 builder.writeln("\u4f60\u597d\u4e16\u754c");

 doc.save(getArtifactsDir() + "Font.FarEast.docx");
 
```

**Returns:**
int - El identificador de configuración regional (idioma) de los caracteres asiáticos formateados.
### getName() {#getName}
```
public String getName()
```


Obtiene el nombre de la fuente.

 **Remarks:** 

Al obtener, devuelve [getNameAscii()](../../com.aspose.words/font/\#getNameAscii) / [setNameAscii(java.lang.String)](../../com.aspose.words/font/\#setNameAscii-java.lang.String).

Al establecer, asigna [getNameAscii()](../../com.aspose.words/font/\#getNameAscii) / [setNameAscii(java.lang.String)](../../com.aspose.words/font/\#setNameAscii-java.lang.String), [getNameBi()](../../com.aspose.words/font/\#getNameBi) / [setNameBi(java.lang.String)](../../com.aspose.words/font/\#setNameBi-java.lang.String), [getNameFarEast()](../../com.aspose.words/font/\#getNameFarEast) / [setNameFarEast(java.lang.String)](../../com.aspose.words/font/\#setNameFarEast-java.lang.String) y [getNameOther()](../../com.aspose.words/font/\#getNameOther) / [setNameOther(java.lang.String)](../../com.aspose.words/font/\#setNameOther-java.lang.String) al valor especificado.

 **Examples:** 

Muestra cómo insertar texto con formato usando DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

Muestra cómo formatear una secuencia de texto usando su propiedad de fuente.

```

 Document doc = new Document();
 Run run = new Run(doc, "Hello world!");

 Font font = run.getFont();
 font.setName("Courier New");
 font.setSize(36.0);
 font.setHighlightColor(Color.YELLOW);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(run);
 doc.save(getArtifactsDir() + "Font.CreateFormattedRun.docx");
 
```

**Returns:**
java.lang.String - El nombre de la fuente.
### getNameAscii() {#getNameAscii}
```
public String getNameAscii()
```


Obtiene la fuente utilizada para texto latino (caracteres con códigos de carácter del 0 (cero) al 127).

 **Examples:** 

Muestra cómo Microsoft Word puede combinar dos fuentes diferentes en un segmento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Suppose a run that we use the builder to insert while using this font configuration
 // contains characters within the ASCII characters' range. In that case,
 // it will display those characters using this font.
 builder.getFont().setNameAscii("Calibri");

 // With no other font specified, the builder will also apply this font to all characters that it inserts.
 Assert.assertEquals("Calibri", builder.getFont().getName());

 // Specify a font to use for all characters outside of the ASCII range.
 // Ideally, this font should have a glyph for each required non-ASCII character code.
 builder.getFont().setNameOther("Courier New");

 // Insert a run with one word consisting of ASCII characters, and one word with all characters outside that range.
 // Each character will be displayed using either of the fonts, depending on.
 builder.writeln("Hello, \u041f\u0440\u0438\u0432\u0435\u0442");

 doc.save(getArtifactsDir() + "Font.NameAscii.docx");
 
```

**Returns:**
java.lang.String - La fuente utilizada para texto latino (caracteres con códigos de carácter desde 0 (cero) hasta 127).
### getNameBi() {#getNameBi}
```
public String getNameBi()
```


Obtiene el nombre de la fuente en un documento de idioma de derecha a izquierda.

 **Examples:** 

Muestra cómo definir conjuntos separados de configuraciones de fuente para texto de derecha a izquierda, y texto de derecha a izquierda.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Returns:**
java.lang.String - El nombre de la fuente en un documento de idioma de derecha a izquierda.
### getNameFarEast() {#getNameFarEast}
```
public String getNameFarEast()
```


Obtiene un nombre de fuente de Asia Oriental.

 **Examples:** 

Muestra cómo insertar y formatear texto en un idioma del Lejano Oriente.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font settings that the document builder will apply to any text that it inserts.
 builder.getFont().setName("Courier New");
 builder.getFont().setLocaleId(1033);

 // Name "FarEast" equivalents for our font and locale.
 // If the builder inserts Asian characters with this Font configuration, then each run that contains
 // these characters will display them using the "FarEast" font/locale instead of the default.
 // This could be useful when a western font does not have ideal representations for Asian characters.
 builder.getFont().setNameFarEast("SimSun");
 builder.getFont().setLocaleIdFarEast(2052);

 // This text will be displayed in the default font/locale.
 builder.writeln("Hello world!");

 // Since these are Asian characters, this run will apply our "FarEast" font/locale equivalents.
 builder.writeln("\u4f60\u597d\u4e16\u754c");

 doc.save(getArtifactsDir() + "Font.FarEast.docx");
 
```

**Returns:**
java.lang.String - Un nombre de fuente de Asia Oriental.
### getNameOther() {#getNameOther}
```
public String getNameOther()
```


Obtiene la fuente utilizada para caracteres con códigos de carácter del 128 al 255.

 **Examples:** 

Muestra cómo Microsoft Word puede combinar dos fuentes diferentes en un segmento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Suppose a run that we use the builder to insert while using this font configuration
 // contains characters within the ASCII characters' range. In that case,
 // it will display those characters using this font.
 builder.getFont().setNameAscii("Calibri");

 // With no other font specified, the builder will also apply this font to all characters that it inserts.
 Assert.assertEquals("Calibri", builder.getFont().getName());

 // Specify a font to use for all characters outside of the ASCII range.
 // Ideally, this font should have a glyph for each required non-ASCII character code.
 builder.getFont().setNameOther("Courier New");

 // Insert a run with one word consisting of ASCII characters, and one word with all characters outside that range.
 // Each character will be displayed using either of the fonts, depending on.
 builder.writeln("Hello, \u041f\u0440\u0438\u0432\u0435\u0442");

 doc.save(getArtifactsDir() + "Font.NameAscii.docx");
 
```

**Returns:**
java.lang.String - La fuente utilizada para caracteres con códigos de carácter desde 128 hasta 255.
### getNoProofing() {#getNoProofing}
```
public boolean getNoProofing()
```


Verdadero cuando los caracteres formateados no deben revisarse ortográficamente.

 **Examples:** 

Muestra cómo evitar que el texto sea revisado ortográficamente por Microsoft Word.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Normally, Microsoft Word emphasizes spelling errors with a jagged red underline.
 // We can un-set the "NoProofing" flag to create a portion of text that
 // bypasses the spell checker while completely disabling it.
 builder.getFont().setNoProofing(true);

 builder.writeln("Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

 doc.save(getArtifactsDir() + "Font.NoProofing.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getNumberSpacing() {#getNumberSpacing}
```
public int getNumberSpacing()
```


Obtiene el tipo de espaciado del número que se muestra.

 **Examples:** 

Muestra cómo establecer el tipo de espaciado del número.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // This effect is only supported in newer versions of MS Word.
 doc.getCompatibilityOptions().optimizeFor(MsWordVersion.WORD_2019);

 builder.write("1 ");
 builder.write("This is an example");

 Run run = doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0);
 if (run.getFont().getNumberSpacing() == NumSpacing.DEFAULT)
     run.getFont().setNumberSpacing(NumSpacing.PROPORTIONAL);

 doc.save(getArtifactsDir() + "Fonts.NumberSpacing.docx");
 
```

**Returns:**
int - El tipo de espaciado del número que se muestra. El valor devuelto es una de las constantes de [NumSpacing](../../com.aspose.words/numspacing/).
### getOldOn() {#getOldOn}
```
public boolean getOldOn()
```




**Returns:**
boolean
### getOldOpacity() {#getOldOpacity}
```
public double getOldOpacity()
```




**Returns:**
double
### getOutline() {#getOutline}
```
public boolean getOutline()
```


Verdadero si la fuente está formateada como contorno.

 **Examples:** 

Muestra cómo crear un segmento de texto formateado como contorno.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set the Outline flag to change the text's fill color to white and
 // leave a thin outline around each character in the original color of the text.
 builder.getFont().setOutline(true);
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setSize(36.0);

 builder.writeln("This text has an outline.");

 doc.save(getArtifactsDir() + "Font.Outline.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getPatternType() {#getPatternType}
```
public int getPatternType()
```




**Returns:**
int
### getPosition() {#getPosition}
```
public double getPosition()
```


Obtiene la posición del texto (en puntos) relativa a la línea base. Un número positivo eleva el texto, y un número negativo lo baja.

 **Examples:** 

Muestra cómo formatear el texto para desplazar su posición.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // Raise this run of text 5 points above the baseline.
 Run run = new Run(doc, "Raised text. ");
 run.getFont().setPosition(5.0);
 para.appendChild(run);

 // Lower this run of text 10 points below the baseline.
 run = new Run(doc, "Lowered text. ");
 run.getFont().setPosition(-10);
 para.appendChild(run);

 // Add a run of normal text.
 run = new Run(doc, "Text in its default position. ");
 para.appendChild(run);

 // Add a run of text that appears as subscript.
 run = new Run(doc, "Subscript. ");
 run.getFont().setSubscript(true);
 para.appendChild(run);

 // Add a run of text that appears as superscript.
 run = new Run(doc, "Superscript.");
 run.getFont().setSuperscript(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.PositionSubscript.docx");
 
```

**Returns:**
double - La posición del texto (en puntos) relativa a la línea base.
### getPresetTexture() {#getPresetTexture}
```
public int getPresetTexture()
```




**Returns:**
int
### getRotateWithObject() {#getRotateWithObject}
```
public boolean getRotateWithObject()
```




**Returns:**
boolean
### getScaling() {#getScaling}
```
public int getScaling()
```


Obtiene el escalado del ancho de los caracteres en porcentaje.

 **Examples:** 

Muestra cómo establecer el escalado horizontal y el espaciado para los caracteres.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add run of text and increase character width to 150%.
 builder.getFont().setScaling(150);
 builder.writeln("Wide characters");

 // Add run of text and add 1pt of extra horizontal spacing between each character.
 builder.getFont().setSpacing(1.0);
 builder.writeln("Expanded by 1pt");

 // Add run of text and bring characters closer together by 1pt.
 builder.getFont().setSpacing(-1);
 builder.writeln("Condensed by 1pt");

 doc.save(getArtifactsDir() + "Font.ScalingSpacing.docx");
 
```

**Returns:**
int - Escalado del ancho de carácter en porcentaje.
### getShading() {#getShading}
```
public Shading getShading()
```


Devuelve un objeto [Shading](../../com.aspose.words/shading/) que se refiere al formato de sombreado de la fuente.

 **Examples:** 

Muestra cómo aplicar sombreado al texto creado por un generador de documentos.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setColor(Color.WHITE);

 // One way to make the text created using our white font color visible
 // is to apply a background shading effect.
 Shading shading = builder.getFont().getShading();
 shading.setTexture(TextureIndex.TEXTURE_DIAGONAL_UP);
 shading.setBackgroundPatternColor(Color.RED);
 shading.setForegroundPatternColor(Color.BLUE);

 builder.writeln("White text on an orange background with a two-tone texture.");

 doc.save(getArtifactsDir() + "Font.Shading.docx");
 
```

**Returns:**
[Shading](../../com.aspose.words/shading/) - A [Shading](../../com.aspose.words/shading/) object that refers to the shading formatting for the font.
### getShadow() {#getShadow}
```
public boolean getShadow()
```


Verdadero si la fuente está formateada como sombreada.

 **Examples:** 

Muestra cómo crear un segmento de texto formateado con sombra.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set the Shadow flag to apply an offset shadow effect,
 // making it look like the letters are floating above the page.
 builder.getFont().setShadow(true);
 builder.getFont().setSize(36.0);

 builder.writeln("This text has a shadow.");

 doc.save(getArtifactsDir() + "Font.Shadow.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getSize() {#getSize}
```
public double getSize()
```


Obtiene el tamaño de fuente en puntos.

 **Examples:** 

Muestra cómo insertar texto con formato usando DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

Muestra cómo formatear una secuencia de texto usando su propiedad de fuente.

```

 Document doc = new Document();
 Run run = new Run(doc, "Hello world!");

 Font font = run.getFont();
 font.setName("Courier New");
 font.setSize(36.0);
 font.setHighlightColor(Color.YELLOW);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(run);
 doc.save(getArtifactsDir() + "Font.CreateFormattedRun.docx");
 
```

**Returns:**
double - El tamaño de la fuente en puntos.
### getSizeBi() {#getSizeBi}
```
public double getSizeBi()
```


Obtiene el tamaño de fuente en puntos utilizado en un documento de derecha a izquierda.

 **Examples:** 

Muestra cómo definir conjuntos separados de configuraciones de fuente para texto de derecha a izquierda, y texto de derecha a izquierda.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Returns:**
double - El tamaño de la fuente en puntos utilizado en un documento de derecha a izquierda.
### getSmallCaps() {#getSmallCaps}
```
public boolean getSmallCaps()
```


Verdadero si la fuente está formateada en letras capitales pequeñas.

 **Examples:** 

Muestra cómo formatear una ejecución para mostrar su contenido en mayúsculas.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // There are two ways of getting a run to display its lowercase text in uppercase without changing the contents.
 // 1 -  Set the AllCaps flag to display all characters in regular capitals:
 Run run = new Run(doc, "all capitals");
 run.getFont().setAllCaps(true);
 para.appendChild(run);

 para = (Paragraph) para.getParentNode().appendChild(new Paragraph(doc));

 // 2 -  Set the SmallCaps flag to display all characters in small capitals:
 // If a character is lower case, it will appear in its upper case form
 // but will have the same height as the lower case (the font's x-height).
 // Characters that were in upper case originally will look the same.
 run = new Run(doc, "Small Capitals");
 run.getFont().setSmallCaps(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.Caps.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getSnapToGrid() {#getSnapToGrid}
```
public boolean getSnapToGrid()
```


Especifica si la fuente actual debe usar la configuración de caracteres por línea de la cuadrícula del documento al diseñar.

**Returns:**
boolean - El valor  boolean  correspondiente.
### getSpacing() {#getSpacing}
```
public double getSpacing()
```


Obtiene el espaciado (en puntos) entre caracteres.

 **Examples:** 

Muestra cómo establecer el escalado horizontal y el espaciado para los caracteres.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add run of text and increase character width to 150%.
 builder.getFont().setScaling(150);
 builder.writeln("Wide characters");

 // Add run of text and add 1pt of extra horizontal spacing between each character.
 builder.getFont().setSpacing(1.0);
 builder.writeln("Expanded by 1pt");

 // Add run of text and bring characters closer together by 1pt.
 builder.getFont().setSpacing(-1);
 builder.writeln("Condensed by 1pt");

 doc.save(getArtifactsDir() + "Font.ScalingSpacing.docx");
 
```

**Returns:**
double - El espaciado (en puntos) entre caracteres.
### getStrikeThrough() {#getStrikeThrough}
```
public boolean getStrikeThrough()
```


Verdadero si la fuente está formateada como texto tachado.

 **Examples:** 

Muestra cómo agregar una línea tachada al texto.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 Run run = new Run(doc, "Text with a single-line strikethrough.");
 run.getFont().setStrikeThrough(true);
 para.appendChild(run);

 para = (Paragraph) para.getParentNode().appendChild(new Paragraph(doc));

 run = new Run(doc, "Text with a double-line strikethrough.");
 run.getFont().setDoubleStrikeThrough(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.StrikeThrough.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getStyle() {#getStyle}
```
public Style getStyle()
```


Obtiene el estilo de carácter aplicado a este formato.

 **Examples:** 

Aplica un subrayado doble a todos los segmentos en un documento que están formateados con estilos de carácter personalizados.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a custom style and apply it to text created using a document builder.
 Style style = doc.getStyles().add(StyleType.CHARACTER, "MyStyle");
 style.getFont().setColor(Color.RED);
 style.getFont().setName("Courier New");

 builder.getFont().setStyleName("MyStyle");
 builder.write("This text is in a custom style.");

 // Iterate over every run and add a double underline to every custom style.
 for (Run run : (Iterable) doc.getChildNodes(NodeType.RUN, true)) {
     Style charStyle = run.getFont().getStyle();

     if (!charStyle.getBuiltIn())
         run.getFont().setUnderline(Underline.DOUBLE);
 }

 doc.save(getArtifactsDir() + "Font.Style.docx");
 
```

**Returns:**
[Style](../../com.aspose.words/style/) - The character style applied to this formatting.
### getStyleIdentifier() {#getStyleIdentifier}
```
public int getStyleIdentifier()
```


Obtiene el identificador de estilo independiente de la configuración regional del estilo de carácter aplicado a este formato.

 **Examples:** 

Muestra cómo cambiar el estilo del texto existente.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways of referencing styles.
 // 1 -  Using the style name:
 builder.getFont().setStyleName("Emphasis");
 builder.writeln("Text originally in \"Emphasis\" style");

 // 2 -  Using a built-in style identifier:
 builder.getFont().setStyleIdentifier(StyleIdentifier.INTENSE_EMPHASIS);
 builder.writeln("Text originally in \"Intense Emphasis\" style");

 // Convert all uses of one style to another,
 // using the above methods to reference old and new styles.
 for (Run run : (Iterable) doc.getChildNodes(NodeType.RUN, true)) {
     if (run.getFont().getStyleName().equals("Emphasis"))
         run.getFont().setStyleName("Strong");

     if (((run.getFont().getStyleIdentifier()) == (StyleIdentifier.INTENSE_EMPHASIS)))
         run.getFont().setStyleIdentifier(StyleIdentifier.STRONG);
 }

 doc.save(getArtifactsDir() + "Font.ChangeStyle.docx");
 
```

**Returns:**
int - El identificador de estilo independiente de la configuración regional del estilo de carácter aplicado a este formato. El valor devuelto es una de las constantes de [StyleIdentifier](../../com.aspose.words/styleidentifier/).
### getStyleName() {#getStyleName}
```
public String getStyleName()
```


Obtiene el nombre del estilo de carácter aplicado a este formato.

 **Examples:** 

Muestra cómo cambiar el estilo del texto existente.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways of referencing styles.
 // 1 -  Using the style name:
 builder.getFont().setStyleName("Emphasis");
 builder.writeln("Text originally in \"Emphasis\" style");

 // 2 -  Using a built-in style identifier:
 builder.getFont().setStyleIdentifier(StyleIdentifier.INTENSE_EMPHASIS);
 builder.writeln("Text originally in \"Intense Emphasis\" style");

 // Convert all uses of one style to another,
 // using the above methods to reference old and new styles.
 for (Run run : (Iterable) doc.getChildNodes(NodeType.RUN, true)) {
     if (run.getFont().getStyleName().equals("Emphasis"))
         run.getFont().setStyleName("Strong");

     if (((run.getFont().getStyleIdentifier()) == (StyleIdentifier.INTENSE_EMPHASIS)))
         run.getFont().setStyleIdentifier(StyleIdentifier.STRONG);
 }

 doc.save(getArtifactsDir() + "Font.ChangeStyle.docx");
 
```

**Returns:**
java.lang.String - El nombre del estilo de carácter aplicado a este formato.
### getSubscript() {#getSubscript}
```
public boolean getSubscript()
```


Verdadero si la fuente está formateada como subíndice.

 **Examples:** 

Muestra cómo formatear el texto para desplazar su posición.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // Raise this run of text 5 points above the baseline.
 Run run = new Run(doc, "Raised text. ");
 run.getFont().setPosition(5.0);
 para.appendChild(run);

 // Lower this run of text 10 points below the baseline.
 run = new Run(doc, "Lowered text. ");
 run.getFont().setPosition(-10);
 para.appendChild(run);

 // Add a run of normal text.
 run = new Run(doc, "Text in its default position. ");
 para.appendChild(run);

 // Add a run of text that appears as subscript.
 run = new Run(doc, "Subscript. ");
 run.getFont().setSubscript(true);
 para.appendChild(run);

 // Add a run of text that appears as superscript.
 run = new Run(doc, "Superscript.");
 run.getFont().setSuperscript(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.PositionSubscript.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getSuperscript() {#getSuperscript}
```
public boolean getSuperscript()
```


Verdadero si la fuente está formateada como superíndice.

 **Examples:** 

Muestra cómo formatear el texto para desplazar su posición.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // Raise this run of text 5 points above the baseline.
 Run run = new Run(doc, "Raised text. ");
 run.getFont().setPosition(5.0);
 para.appendChild(run);

 // Lower this run of text 10 points below the baseline.
 run = new Run(doc, "Lowered text. ");
 run.getFont().setPosition(-10);
 para.appendChild(run);

 // Add a run of normal text.
 run = new Run(doc, "Text in its default position. ");
 para.appendChild(run);

 // Add a run of text that appears as subscript.
 run = new Run(doc, "Subscript. ");
 run.getFont().setSubscript(true);
 para.appendChild(run);

 // Add a run of text that appears as superscript.
 run = new Run(doc, "Superscript.");
 run.getFont().setSuperscript(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.PositionSubscript.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getTextEffect() {#getTextEffect}
```
public int getTextEffect()
```


Obtiene el efecto de animación de la fuente.

 **Examples:** 

Muestra cómo aplicar un efecto visual a una ejecución.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(36.0);
 builder.getFont().setTextEffect(TextEffect.SPARKLE_TEXT);

 builder.writeln("Text with a sparkle effect.");

 // Older versions of Microsoft Word only support font animation effects.
 doc.save(getArtifactsDir() + "Font.SparklingText.doc");
 
```

**Returns:**
int - El efecto de animación de la fuente. El valor devuelto es una de las constantes de [TextEffect](../../com.aspose.words/texteffect/).
### getTextureAlignment() {#getTextureAlignment}
```
public int getTextureAlignment()
```




**Returns:**
int
### getThemeColor() {#getThemeColor}
```
public int getThemeColor()
```


Obtiene el color del tema en el esquema de colores aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/).

 **Examples:** 

Muestra cómo trabajar con fuentes de tema y colores.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

Muestra cómo crear y usar estilos temáticos.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln();

 // Create some style with theme font properties.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "ThemedStyle");
 style.getFont().setThemeFont(ThemeFont.MAJOR);
 style.getFont().setThemeColor(ThemeColor.ACCENT_5);
 style.getFont().setTintAndShade(0.3);

 builder.getParagraphFormat().setStyleName("ThemedStyle");
 builder.writeln("Text with themed style");
 
```

**Returns:**
int - El color del tema en el esquema de colores aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/). El valor devuelto es una de las constantes de [ThemeColor](../../com.aspose.words/themecolor/).
### getThemeFont() {#getThemeFont}
```
public int getThemeFont()
```


Obtiene la fuente del tema en el esquema de fuentes aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/).

 **Examples:** 

Muestra cómo trabajar con fuentes de tema y colores.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

Muestra cómo crear y usar estilos temáticos.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln();

 // Create some style with theme font properties.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "ThemedStyle");
 style.getFont().setThemeFont(ThemeFont.MAJOR);
 style.getFont().setThemeColor(ThemeColor.ACCENT_5);
 style.getFont().setTintAndShade(0.3);

 builder.getParagraphFormat().setStyleName("ThemedStyle");
 builder.writeln("Text with themed style");
 
```

**Returns:**
int - La fuente del tema en el esquema de fuentes aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/). El valor devuelto es una de las constantes de [ThemeFont](../../com.aspose.words/themefont/).
### getThemeFontAscii() {#getThemeFontAscii}
```
public int getThemeFontAscii()
```


Obtiene la fuente del tema utilizada para texto latino (caracteres con códigos de carácter de 0 (cero) a 127) en el esquema de fuentes aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/).

 **Examples:** 

Muestra cómo trabajar con fuentes de tema y colores.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

**Returns:**
int - La fuente temática utilizada para texto latino (caracteres con códigos de carácter de 0 (cero) a 127) en el esquema de fuentes aplicado que está asociado con este [Font](../../com.aspose.words/font/) objeto. El valor devuelto es una de las constantes [ThemeFont](../../com.aspose.words/themefont/).
### getThemeFontBi() {#getThemeFontBi}
```
public int getThemeFontBi()
```


Obtiene la fuente del tema en el esquema de fuentes aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/) en un documento de idioma de derecha a izquierda.

 **Examples:** 

Muestra cómo trabajar con fuentes de tema y colores.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

**Returns:**
int - La fuente temática en el esquema de fuentes aplicado que está asociado con este [Font](../../com.aspose.words/font/) objeto en un documento de idioma de derecha a izquierda. El valor devuelto es una de las constantes [ThemeFont](../../com.aspose.words/themefont/).
### getThemeFontFarEast() {#getThemeFontFarEast}
```
public int getThemeFontFarEast()
```


Obtiene la fuente del tema de Asia Oriental en el esquema de fuentes aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/).

 **Examples:** 

Muestra cómo trabajar con fuentes de tema y colores.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

**Returns:**
int - La fuente temática de Asia Oriental en el esquema de fuentes aplicado que está asociado con este [Font](../../com.aspose.words/font/) objeto. El valor devuelto es una de las constantes [ThemeFont](../../com.aspose.words/themefont/).
### getThemeFontOther() {#getThemeFontOther}
```
public int getThemeFontOther()
```


Obtiene la fuente del tema utilizada para caracteres con códigos de carácter de 128 a 255 en el esquema de fuentes aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/).

 **Examples:** 

Muestra cómo trabajar con fuentes de tema y colores.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

**Returns:**
int - La fuente temática utilizada para caracteres con códigos de carácter de 128 a 255 en el esquema de fuentes aplicado que está asociado con este [Font](../../com.aspose.words/font/) objeto. El valor devuelto es una de las constantes [ThemeFont](../../com.aspose.words/themefont/).
### getTintAndShade() {#getTintAndShade}
```
public double getTintAndShade()
```


Obtiene un valor double que aclara o oscurece un color.

**Returns:**
double - Un valor double que aclara o oscurece un color.
### getUnderline() {#getUnderline}
```
public int getUnderline()
```


Obtiene el tipo de subrayado aplicado a la fuente.

 **Examples:** 

Muestra cómo insertar texto con formato usando DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

Muestra cómo insertar un campo de hipervínculo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("For more information, please visit the ");

 // Insert a hyperlink and emphasize it with custom formatting.
 // The hyperlink will be a clickable piece of text which will take us to the location specified in the URL.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 builder.insertHyperlink("Google website", "https://www.google.com", false);
 builder.getFont().clearFormatting();
 builder.writeln(".");

 // Ctrl + left clicking the link in the text in Microsoft Word will take us to the URL via a new web browser window.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlink.docx");
 
```

Muestra cómo configurar el estilo y el color de un subrayado de texto.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setUnderline(Underline.DOTTED);
 builder.getFont().setUnderlineColor(Color.RED);

 builder.writeln("Underlined text.");

 doc.save(getArtifactsDir() + "Font.Underlines.docx");
 
```

**Returns:**
int - El tipo de subrayado aplicado a la fuente. El valor devuelto es una de las constantes [Underline](../../com.aspose.words/underline/).
### getUnderlineColor() {#getUnderlineColor}
```
public Color getUnderlineColor()
```


Obtiene el color del subrayado aplicado a la fuente.

 **Examples:** 

Muestra cómo configurar el estilo y el color de un subrayado de texto.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setUnderline(Underline.DOTTED);
 builder.getFont().setUnderlineColor(Color.RED);

 builder.writeln("Underlined text.");

 doc.save(getArtifactsDir() + "Font.Underlines.docx");
 
```

**Returns:**
java.awt.Color - El color del subrayado aplicado a la fuente.
### hasDmlEffect(int dmlEffectType) {#hasDmlEffect-int}
```
public boolean hasDmlEffect(int dmlEffectType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| dmlEffectType | int |  |

**Returns:**
boolean
### oneColorGradient(int style, int variant, double degree) {#oneColorGradient-int-int-double}
```
public void oneColorGradient(int style, int variant, double degree)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| estilo | int |  |
| variant | int |  |
| degree | double |  |

### patterned(int patternType) {#patterned-int}
```
public void patterned(int patternType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| patternType | int |  |

### presetTextured(int presetTexture) {#presetTextured-int}
```
public void presetTextured(int presetTexture)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| presetTexture | int |  |

### setAllCaps(boolean value) {#setAllCaps-boolean}
```
public void setAllCaps(boolean value)
```


Verdadero si la fuente está formateada en mayúsculas.

 **Examples:** 

Muestra cómo formatear una ejecución para mostrar su contenido en mayúsculas.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // There are two ways of getting a run to display its lowercase text in uppercase without changing the contents.
 // 1 -  Set the AllCaps flag to display all characters in regular capitals:
 Run run = new Run(doc, "all capitals");
 run.getFont().setAllCaps(true);
 para.appendChild(run);

 para = (Paragraph) para.getParentNode().appendChild(new Paragraph(doc));

 // 2 -  Set the SmallCaps flag to display all characters in small capitals:
 // If a character is lower case, it will appear in its upper case form
 // but will have the same height as the lower case (the font's x-height).
 // Characters that were in upper case originally will look the same.
 run = new Run(doc, "Small Capitals");
 run.getFont().setSmallCaps(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.Caps.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setBidi(boolean value) {#setBidi-boolean}
```
public void setBidi(boolean value)
```


Especifica si el contenido de este run debe tener características de derecha a izquierda.

 **Remarks:** 

Esta propiedad, cuando está activada, no debe usarse con texto fuertemente de izquierda a derecha. Cualquier comportamiento bajo esa condición no está especificado. Esta propiedad, cuando está desactivada, no debe usarse con texto fuertemente de derecha a izquierda. Cualquier comportamiento bajo esa condición no está especificado.

Cuando se muestra el contenido de esta ejecución, todos los caracteres deben tratarse como caracteres de script complejo para fines de formato. Esto significa que [getBoldBi()](../../com.aspose.words/font/\#getBoldBi) / [setBoldBi(boolean)](../../com.aspose.words/font/\#setBoldBi-boolean), [getItalicBi()](../../com.aspose.words/font/\#getItalicBi) / [setItalicBi(boolean)](../../com.aspose.words/font/\#setItalicBi-boolean), [getSizeBi()](../../com.aspose.words/font/\#getSizeBi) / [setSizeBi(double)](../../com.aspose.words/font/\#setSizeBi-double) y un nombre de fuente correspondiente se usarán al renderizar esta ejecución.

Además, cuando se muestra el contenido de esta ejecución, esta propiedad actúa como una sobrescritura de derecha a izquierda para los caracteres que se clasifican como "tipos débiles" y "tipos neutrales".

 **Examples:** 

Muestra cómo definir conjuntos separados de configuraciones de fuente para texto de derecha a izquierda, y texto de derecha a izquierda.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setBold(boolean value) {#setBold-boolean}
```
public void setBold(boolean value)
```


True si la fuente está formateada en negrita.

 **Examples:** 

Muestra cómo insertar texto con formato usando DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setBoldBi(boolean value) {#setBoldBi-boolean}
```
public void setBoldBi(boolean value)
```


Verdadero si el texto de derecha a izquierda está formateado en negrita.

 **Examples:** 

Muestra cómo definir conjuntos separados de configuraciones de fuente para texto de derecha a izquierda, y texto de derecha a izquierda.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |
| valor | java.lang.Object |  |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Establece el color de la fuente.

 **Examples:** 

Muestra cómo insertar texto con formato usando DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

Muestra cómo insertar un campo de hipervínculo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("For more information, please visit the ");

 // Insert a hyperlink and emphasize it with custom formatting.
 // The hyperlink will be a clickable piece of text which will take us to the location specified in the URL.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 builder.insertHyperlink("Google website", "https://www.google.com", false);
 builder.getFont().clearFormatting();
 builder.writeln(".");

 // Ctrl + left clicking the link in the text in Microsoft Word will take us to the URL via a new web browser window.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlink.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.awt.Color | El color de la fuente. |

### setComplexScript(boolean value) {#setComplexScript-boolean}
```
public void setComplexScript(boolean value)
```


Especifica si el contenido de este run debe tratarse como texto de escritura compleja sin importar sus valores de caracteres Unicode al determinar el formato de este run.

 **Examples:** 

Muestra cómo agregar texto que siempre se trata como script complejo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setComplexScript(true);

 builder.writeln("Text treated as complex script.");

 doc.save(getArtifactsDir() + "Font.ComplexScript.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setDoubleStrikeThrough(boolean value) {#setDoubleStrikeThrough-boolean}
```
public void setDoubleStrikeThrough(boolean value)
```


Verdadero si la fuente está formateada con doble tachado.

 **Examples:** 

Muestra cómo agregar una línea tachada al texto.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 Run run = new Run(doc, "Text with a single-line strikethrough.");
 run.getFont().setStrikeThrough(true);
 para.appendChild(run);

 para = (Paragraph) para.getParentNode().appendChild(new Paragraph(doc));

 run = new Run(doc, "Text with a double-line strikethrough.");
 run.getFont().setDoubleStrikeThrough(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.StrikeThrough.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setEmboss(boolean value) {#setEmboss-boolean}
```
public void setEmboss(boolean value)
```


Verdadero si la fuente está formateada como relieve.

 **Examples:** 

Muestra cómo aplicar efectos de grabado/relieve al texto.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(36.0);
 builder.getFont().setColor(Color.WHITE);

 // Below are two ways of using shadows to apply a 3D-like effect to the text.
 // 1 -  Engrave text to make it look like the letters are sunken into the page:
 builder.getFont().setEngrave(true);

 builder.writeln("This text is engraved.");

 // 2 -  Emboss text to make it look like the letters pop out of the page:
 builder.getFont().setEngrave(false);
 builder.getFont().setEmboss(true);

 builder.writeln("This text is embossed.");

 doc.save(getArtifactsDir() + "Font.EngraveEmboss.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setEmphasisMark(int value) {#setEmphasisMark-int}
```
public void setEmphasisMark(int value)
```


Establece la marca de énfasis aplicada a este formato.

 **Examples:** 

Muestra cómo agregar un carácter adicional renderizado arriba/abajo del glifo-carácter.

```

 DocumentBuilder builder = new DocumentBuilder();

 // Possible types of emphasis mark:
 // https://apireference.aspose.com/words/net/aspose.words/emphasismark
 builder.getFont().setEmphasisMark(emphasisMark);

 builder.write("Emphasis text");
 builder.writeln();
 builder.getFont().clearFormatting();
 builder.write("Simple text");

 builder.getDocument().save(getArtifactsDir() + "Fonts.SetEmphasisMark.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | La marca de énfasis aplicada a este formato. El valor debe ser una de las constantes [EmphasisMark](../../com.aspose.words/emphasismark/). |

### setEngrave(boolean value) {#setEngrave-boolean}
```
public void setEngrave(boolean value)
```


Verdadero si la fuente está formateada como grabada.

 **Examples:** 

Muestra cómo aplicar efectos de grabado/relieve al texto.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(36.0);
 builder.getFont().setColor(Color.WHITE);

 // Below are two ways of using shadows to apply a 3D-like effect to the text.
 // 1 -  Engrave text to make it look like the letters are sunken into the page:
 builder.getFont().setEngrave(true);

 builder.writeln("This text is engraved.");

 // 2 -  Emboss text to make it look like the letters pop out of the page:
 builder.getFont().setEngrave(false);
 builder.getFont().setEmboss(true);

 builder.writeln("This text is embossed.");

 doc.save(getArtifactsDir() + "Font.EngraveEmboss.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setFillableBackColor(Color value) {#setFillableBackColor-java.awt.Color}
```
public void setFillableBackColor(Color value)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.awt.Color |  |

### setFillableBackThemeColor(int value) {#setFillableBackThemeColor-int}
```
public void setFillableBackThemeColor(int value)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int |  |

### setFillableBackTintAndShade(double value) {#setFillableBackTintAndShade-double}
```
public void setFillableBackTintAndShade(double value)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double |  |

### setFillableForeColor(Color value) {#setFillableForeColor-java.awt.Color}
```
public void setFillableForeColor(Color value)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.awt.Color |  |

### setFillableForeThemeColor(int value) {#setFillableForeThemeColor-int}
```
public void setFillableForeThemeColor(int value)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int |  |

### setFillableForeTintAndShade(double value) {#setFillableForeTintAndShade-double}
```
public void setFillableForeTintAndShade(double value)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double |  |

### setFillableTransparency(double value) {#setFillableTransparency-double}
```
public void setFillableTransparency(double value)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double |  |

### setFillableVisible(boolean value) {#setFillableVisible-boolean}
```
public void setFillableVisible(boolean value)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean |  |

### setFilledColor(Color value) {#setFilledColor-java.awt.Color}
```
public void setFilledColor(Color value)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.awt.Color |  |

### setGradientAngle(double value) {#setGradientAngle-double}
```
public void setGradientAngle(double value)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double |  |

### setHidden(boolean value) {#setHidden-boolean}
```
public void setHidden(boolean value)
```


Verdadero si la fuente está formateada como texto oculto.

 **Examples:** 

Muestra cómo crear una ejecución de texto oculto.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // With the Hidden flag set to true, any text that we create using this Font object will be invisible in the document.
 // We will not see or highlight hidden text unless we enable the "Hidden text" option
 // found in Microsoft Word via "File" -> "Options" -> "Display". The text will still be there,
 // and we will be able to access this text programmatically.
 // It is not advised to use this method to hide sensitive information.
 builder.getFont().setHidden(true);
 builder.getFont().setSize(36.0);

 builder.writeln("This text will not be visible in the document.");

 doc.save(getArtifactsDir() + "Font.Hidden.docx");
 
```

Muestra cómo usar una implementación de DocumentVisitor para eliminar todo el contenido oculto de un documento.

```

 public void removeHiddenContentFromDocument() throws Exception {
     Document doc = new Document(getMyDir() + "Hidden content.docx");
     RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

     // Below are three types of fields which can accept a document visitor,
     // which will allow it to visit the accepting node, and then traverse its child nodes in a depth-first manner.
     // 1 -  Paragraph node:
     Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 4, true);
     para.accept(hiddenContentRemover);

     // 2 -  Table node:
     Table table = doc.getFirstSection().getBody().getTables().get(0);
     table.accept(hiddenContentRemover);

     // 3 -  Document node:
     doc.accept(hiddenContentRemover);

     doc.save(getArtifactsDir() + "Font.RemoveHiddenContentFromDocument.docx");
 }

 /// 
 /// Removes all visited nodes marked as "hidden content".
 /// 
 public static class RemoveHiddenContentVisitor extends DocumentVisitor {
     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(FieldStart fieldStart) {
         if (fieldStart.getFont().getHidden())
             fieldStart.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(FieldEnd fieldEnd) {
         if (fieldEnd.getFont().getHidden())
             fieldEnd.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(FieldSeparator fieldSeparator) {
         if (fieldSeparator.getFont().getHidden())
             fieldSeparator.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(Run run) {
         if (run.getFont().getHidden())
             run.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(Paragraph paragraph) {
         if (paragraph.getParagraphBreakFont().getHidden())
             paragraph.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FormField is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         if (formField.getFont().getHidden())
             formField.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a GroupShape is encountered in the document.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         if (groupShape.getFont().getHidden())
             groupShape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Shape is encountered in the document.
     /// 
     public int visitShapeStart(Shape shape) {
         if (shape.getFont().getHidden())
             shape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Comment is encountered in the document.
     /// 
     public int visitCommentStart(Comment comment) {
         if (comment.getFont().getHidden())
             comment.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Footnote is encountered in the document.
     /// 
     public int visitFootnoteStart(Footnote footnote) {
         if (footnote.getFont().getHidden())
             footnote.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SpecialCharacter is encountered in the document.
     /// 
     public int visitSpecialChar(SpecialChar specialChar) {
         if (specialChar.getFont().getHidden())
             specialChar.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Table node is ended in the document.
     /// 
     public int visitTableEnd(Table table) {
         // The content inside table cells may have the hidden content flag, but the tables themselves cannot.
         // If this table had nothing but hidden content, this visitor would have removed all of it,
         // and there would be no child nodes left.
         // Thus, we can also treat the table itself as hidden content and remove it.
         // Tables which are empty but do not have hidden content will have cells with empty paragraphs inside,
         // which this visitor will not remove.
         if (!table.hasChildNodes())
             table.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Cell node is ended in the document.
     /// 
     public int visitCellEnd(Cell cell) {
         if (!cell.hasChildNodes() && cell.getParentNode() != null)
             cell.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Row node is ended in the document.
     /// 
     public int visitRowEnd(Row row) {
         if (!row.hasChildNodes() && row.getParentNode() != null)
             row.remove();

         return VisitorAction.CONTINUE;
     }
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setHighlightColor(Color value) {#setHighlightColor-java.awt.Color}
```
public void setHighlightColor(Color value)
```


Establece el color de resaltado (marcador).

 **Examples:** 

Muestra cómo formatear una secuencia de texto usando su propiedad de fuente.

```

 Document doc = new Document();
 Run run = new Run(doc, "Hello world!");

 Font font = run.getFont();
 font.setName("Courier New");
 font.setSize(36.0);
 font.setHighlightColor(Color.YELLOW);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(run);
 doc.save(getArtifactsDir() + "Font.CreateFormattedRun.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.awt.Color | El color de resaltado (marcador). |

### setImage(byte[] imageBytes) {#setImage-byte}
```
public void setImage(byte[] imageBytes)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| imageBytes | byte[] |  |

### setItalic(boolean value) {#setItalic-boolean}
```
public void setItalic(boolean value)
```


Verdadero si la fuente está formateada en cursiva.

 **Examples:** 

Muestra cómo escribir texto en cursiva usando un document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(36.0);
 builder.getFont().setItalic(true);
 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "Font.Italic.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setItalicBi(boolean value) {#setItalicBi-boolean}
```
public void setItalicBi(boolean value)
```


Verdadero si el texto de derecha a izquierda está formateado como cursiva.

 **Examples:** 

Muestra cómo definir conjuntos separados de configuraciones de fuente para texto de derecha a izquierda, y texto de derecha a izquierda.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setKerning(double value) {#setKerning-double}
```
public void setKerning(double value)
```


Establece el tamaño de fuente en el que comienza el kerning.

 **Examples:** 

Muestra cómo especificar el tamaño de fuente en el que el kerning comienza a tener efecto.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setName("Arial Black");

 // Set the builder's font size, and minimum size at which kerning will take effect.
 // The font size falls below the kerning threshold, so the run bellow will not have kerning.
 builder.getFont().setSize(18.0);
 builder.getFont().setKerning(24.0);

 builder.writeln("TALLY. (Kerning not applied)");

 // Set the kerning threshold so that the builder's current font size is above it.
 // Any text we add from this point will have kerning applied. The spaces between characters
 // will be adjusted, normally resulting in a slightly more aesthetically pleasing text run.
 builder.getFont().setKerning(12.0);

 builder.writeln("TALLY. (Kerning applied)");

 doc.save(getArtifactsDir() + "Font.Kerning.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | El tamaño de fuente a partir del cual comienza el kerning. |

### setLocaleId(int value) {#setLocaleId-int}
```
public void setLocaleId(int value)
```


Establece el identificador de configuración regional (idioma) de los caracteres formateados.

 **Remarks:** 

Para la lista de identificadores de configuración regional, consulte https://msdn.microsoft.com/en-us/library/cc233965.aspx

 **Examples:** 

Muestra cómo establecer la configuración regional del texto que estamos agregando con un document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // If we set the font's locale to English and insert some Russian text,
 // the English locale spell checker will not recognize the text and detect it as a spelling error.
 builder.getFont().setLocaleId(1033);
 builder.writeln("\u041f\u0440\u0438\u0432\u0435\u0442!");

 // Set a matching locale for the text that we are about to add to apply the appropriate spell checker.
 builder.getFont().setLocaleId(1049);
 builder.writeln("\u041f\u0440\u0438\u0432\u0435\u0442!");

 doc.save(getArtifactsDir() + "Font.LocaleId.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El identificador de configuración regional (idioma) de los caracteres formateados. |

### setLocaleIdBi(int value) {#setLocaleIdBi-int}
```
public void setLocaleIdBi(int value)
```


Establece el identificador de configuración regional (idioma) de los caracteres formateados de derecha a izquierda.

 **Remarks:** 

Para la lista de identificadores de configuración regional, consulte https://msdn.microsoft.com/en-us/library/cc233965.aspx

 **Examples:** 

Muestra cómo definir conjuntos separados de configuraciones de fuente para texto de derecha a izquierda, y texto de derecha a izquierda.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El identificador de configuración regional (idioma) de los caracteres formateados de derecha a izquierda. |

### setLocaleIdFarEast(int value) {#setLocaleIdFarEast-int}
```
public void setLocaleIdFarEast(int value)
```


Establece el identificador de configuración regional (idioma) de los caracteres asiáticos formateados.

 **Remarks:** 

Para la lista de identificadores de configuración regional, consulte https://msdn.microsoft.com/en-us/library/cc233965.aspx

 **Examples:** 

Muestra cómo insertar y formatear texto en un idioma del Lejano Oriente.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font settings that the document builder will apply to any text that it inserts.
 builder.getFont().setName("Courier New");
 builder.getFont().setLocaleId(1033);

 // Name "FarEast" equivalents for our font and locale.
 // If the builder inserts Asian characters with this Font configuration, then each run that contains
 // these characters will display them using the "FarEast" font/locale instead of the default.
 // This could be useful when a western font does not have ideal representations for Asian characters.
 builder.getFont().setNameFarEast("SimSun");
 builder.getFont().setLocaleIdFarEast(2052);

 // This text will be displayed in the default font/locale.
 builder.writeln("Hello world!");

 // Since these are Asian characters, this run will apply our "FarEast" font/locale equivalents.
 builder.writeln("\u4f60\u597d\u4e16\u754c");

 doc.save(getArtifactsDir() + "Font.FarEast.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El identificador de configuración regional (idioma) de los caracteres asiáticos formateados. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Establece el nombre de la fuente.

 **Remarks:** 

Al obtener, devuelve [getNameAscii()](../../com.aspose.words/font/\#getNameAscii) / [setNameAscii(java.lang.String)](../../com.aspose.words/font/\#setNameAscii-java.lang.String).

Al establecer, asigna [getNameAscii()](../../com.aspose.words/font/\#getNameAscii) / [setNameAscii(java.lang.String)](../../com.aspose.words/font/\#setNameAscii-java.lang.String), [getNameBi()](../../com.aspose.words/font/\#getNameBi) / [setNameBi(java.lang.String)](../../com.aspose.words/font/\#setNameBi-java.lang.String), [getNameFarEast()](../../com.aspose.words/font/\#getNameFarEast) / [setNameFarEast(java.lang.String)](../../com.aspose.words/font/\#setNameFarEast-java.lang.String) y [getNameOther()](../../com.aspose.words/font/\#getNameOther) / [setNameOther(java.lang.String)](../../com.aspose.words/font/\#setNameOther-java.lang.String) al valor especificado.

 **Examples:** 

Muestra cómo insertar texto con formato usando DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

Muestra cómo formatear una secuencia de texto usando su propiedad de fuente.

```

 Document doc = new Document();
 Run run = new Run(doc, "Hello world!");

 Font font = run.getFont();
 font.setName("Courier New");
 font.setSize(36.0);
 font.setHighlightColor(Color.YELLOW);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(run);
 doc.save(getArtifactsDir() + "Font.CreateFormattedRun.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El nombre de la fuente. |

### setNameAscii(String value) {#setNameAscii-java.lang.String}
```
public void setNameAscii(String value)
```


Establece la fuente utilizada para texto latino (caracteres con códigos de carácter de 0 (cero) a 127).

 **Examples:** 

Muestra cómo Microsoft Word puede combinar dos fuentes diferentes en un segmento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Suppose a run that we use the builder to insert while using this font configuration
 // contains characters within the ASCII characters' range. In that case,
 // it will display those characters using this font.
 builder.getFont().setNameAscii("Calibri");

 // With no other font specified, the builder will also apply this font to all characters that it inserts.
 Assert.assertEquals("Calibri", builder.getFont().getName());

 // Specify a font to use for all characters outside of the ASCII range.
 // Ideally, this font should have a glyph for each required non-ASCII character code.
 builder.getFont().setNameOther("Courier New");

 // Insert a run with one word consisting of ASCII characters, and one word with all characters outside that range.
 // Each character will be displayed using either of the fonts, depending on.
 builder.writeln("Hello, \u041f\u0440\u0438\u0432\u0435\u0442");

 doc.save(getArtifactsDir() + "Font.NameAscii.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | La fuente utilizada para texto latino (caracteres con códigos de carácter de 0 (cero) a 127). |

### setNameBi(String value) {#setNameBi-java.lang.String}
```
public void setNameBi(String value)
```


Establece el nombre de la fuente en un documento de idioma de derecha a izquierda.

 **Examples:** 

Muestra cómo definir conjuntos separados de configuraciones de fuente para texto de derecha a izquierda, y texto de derecha a izquierda.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El nombre de la fuente en un documento de idioma de derecha a izquierda. |

### setNameFarEast(String value) {#setNameFarEast-java.lang.String}
```
public void setNameFarEast(String value)
```


Establece un nombre de fuente de Asia Oriental.

 **Examples:** 

Muestra cómo insertar y formatear texto en un idioma del Lejano Oriente.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font settings that the document builder will apply to any text that it inserts.
 builder.getFont().setName("Courier New");
 builder.getFont().setLocaleId(1033);

 // Name "FarEast" equivalents for our font and locale.
 // If the builder inserts Asian characters with this Font configuration, then each run that contains
 // these characters will display them using the "FarEast" font/locale instead of the default.
 // This could be useful when a western font does not have ideal representations for Asian characters.
 builder.getFont().setNameFarEast("SimSun");
 builder.getFont().setLocaleIdFarEast(2052);

 // This text will be displayed in the default font/locale.
 builder.writeln("Hello world!");

 // Since these are Asian characters, this run will apply our "FarEast" font/locale equivalents.
 builder.writeln("\u4f60\u597d\u4e16\u754c");

 doc.save(getArtifactsDir() + "Font.FarEast.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | Un nombre de fuente de Asia Oriental. |

### setNameOther(String value) {#setNameOther-java.lang.String}
```
public void setNameOther(String value)
```


Establece la fuente utilizada para los caracteres con códigos de carácter de 128 a 255.

 **Examples:** 

Muestra cómo Microsoft Word puede combinar dos fuentes diferentes en un segmento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Suppose a run that we use the builder to insert while using this font configuration
 // contains characters within the ASCII characters' range. In that case,
 // it will display those characters using this font.
 builder.getFont().setNameAscii("Calibri");

 // With no other font specified, the builder will also apply this font to all characters that it inserts.
 Assert.assertEquals("Calibri", builder.getFont().getName());

 // Specify a font to use for all characters outside of the ASCII range.
 // Ideally, this font should have a glyph for each required non-ASCII character code.
 builder.getFont().setNameOther("Courier New");

 // Insert a run with one word consisting of ASCII characters, and one word with all characters outside that range.
 // Each character will be displayed using either of the fonts, depending on.
 builder.writeln("Hello, \u041f\u0440\u0438\u0432\u0435\u0442");

 doc.save(getArtifactsDir() + "Font.NameAscii.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | La fuente utilizada para caracteres con códigos de carácter de 128 a 255. |

### setNoProofing(boolean value) {#setNoProofing-boolean}
```
public void setNoProofing(boolean value)
```


Verdadero cuando los caracteres formateados no deben revisarse ortográficamente.

 **Examples:** 

Muestra cómo evitar que el texto sea revisado ortográficamente por Microsoft Word.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Normally, Microsoft Word emphasizes spelling errors with a jagged red underline.
 // We can un-set the "NoProofing" flag to create a portion of text that
 // bypasses the spell checker while completely disabling it.
 builder.getFont().setNoProofing(true);

 builder.writeln("Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

 doc.save(getArtifactsDir() + "Font.NoProofing.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setNumberSpacing(int value) {#setNumberSpacing-int}
```
public void setNumberSpacing(int value)
```


Establece el tipo de espaciado del número que se muestra.

 **Examples:** 

Muestra cómo establecer el tipo de espaciado del número.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // This effect is only supported in newer versions of MS Word.
 doc.getCompatibilityOptions().optimizeFor(MsWordVersion.WORD_2019);

 builder.write("1 ");
 builder.write("This is an example");

 Run run = doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0);
 if (run.getFont().getNumberSpacing() == NumSpacing.DEFAULT)
     run.getFont().setNumberSpacing(NumSpacing.PROPORTIONAL);

 doc.save(getArtifactsDir() + "Fonts.NumberSpacing.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El tipo de espaciado del número que se muestra. El valor debe ser una de las constantes [NumSpacing](../../com.aspose.words/numspacing/). |

### setOldOn(boolean value) {#setOldOn-boolean}
```
public void setOldOn(boolean value)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean |  |

### setOldOpacity(double value) {#setOldOpacity-double}
```
public void setOldOpacity(double value)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double |  |

### setOutline(boolean value) {#setOutline-boolean}
```
public void setOutline(boolean value)
```


Verdadero si la fuente está formateada como contorno.

 **Examples:** 

Muestra cómo crear un segmento de texto formateado como contorno.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set the Outline flag to change the text's fill color to white and
 // leave a thin outline around each character in the original color of the text.
 builder.getFont().setOutline(true);
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setSize(36.0);

 builder.writeln("This text has an outline.");

 doc.save(getArtifactsDir() + "Font.Outline.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setPosition(double value) {#setPosition-double}
```
public void setPosition(double value)
```


Establece la posición del texto (en puntos) relativa a la línea base. Un número positivo eleva el texto, y un número negativo lo baja.

 **Examples:** 

Muestra cómo formatear el texto para desplazar su posición.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // Raise this run of text 5 points above the baseline.
 Run run = new Run(doc, "Raised text. ");
 run.getFont().setPosition(5.0);
 para.appendChild(run);

 // Lower this run of text 10 points below the baseline.
 run = new Run(doc, "Lowered text. ");
 run.getFont().setPosition(-10);
 para.appendChild(run);

 // Add a run of normal text.
 run = new Run(doc, "Text in its default position. ");
 para.appendChild(run);

 // Add a run of text that appears as subscript.
 run = new Run(doc, "Subscript. ");
 run.getFont().setSubscript(true);
 para.appendChild(run);

 // Add a run of text that appears as superscript.
 run = new Run(doc, "Superscript.");
 run.getFont().setSuperscript(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.PositionSubscript.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | La posición del texto (en puntos) relativa a la línea base. |

### setRotateWithObject(boolean value) {#setRotateWithObject-boolean}
```
public void setRotateWithObject(boolean value)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean |  |

### setScaling(int value) {#setScaling-int}
```
public void setScaling(int value)
```


Establece la escala del ancho de carácter en porcentaje.

 **Examples:** 

Muestra cómo establecer el escalado horizontal y el espaciado para los caracteres.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add run of text and increase character width to 150%.
 builder.getFont().setScaling(150);
 builder.writeln("Wide characters");

 // Add run of text and add 1pt of extra horizontal spacing between each character.
 builder.getFont().setSpacing(1.0);
 builder.writeln("Expanded by 1pt");

 // Add run of text and bring characters closer together by 1pt.
 builder.getFont().setSpacing(-1);
 builder.writeln("Condensed by 1pt");

 doc.save(getArtifactsDir() + "Font.ScalingSpacing.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | Escalado del ancho de carácter en porcentaje. |

### setShadow(boolean value) {#setShadow-boolean}
```
public void setShadow(boolean value)
```


Verdadero si la fuente está formateada como sombreada.

 **Examples:** 

Muestra cómo crear un segmento de texto formateado con sombra.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set the Shadow flag to apply an offset shadow effect,
 // making it look like the letters are floating above the page.
 builder.getFont().setShadow(true);
 builder.getFont().setSize(36.0);

 builder.writeln("This text has a shadow.");

 doc.save(getArtifactsDir() + "Font.Shadow.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setSize(double value) {#setSize-double}
```
public void setSize(double value)
```


Establece el tamaño de la fuente en puntos.

 **Examples:** 

Muestra cómo insertar texto con formato usando DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

Muestra cómo formatear una secuencia de texto usando su propiedad de fuente.

```

 Document doc = new Document();
 Run run = new Run(doc, "Hello world!");

 Font font = run.getFont();
 font.setName("Courier New");
 font.setSize(36.0);
 font.setHighlightColor(Color.YELLOW);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(run);
 doc.save(getArtifactsDir() + "Font.CreateFormattedRun.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | El tamaño de la fuente en puntos. |

### setSizeBi(double value) {#setSizeBi-double}
```
public void setSizeBi(double value)
```


Establece el tamaño de la fuente en puntos utilizado en un documento de derecha a izquierda.

 **Examples:** 

Muestra cómo definir conjuntos separados de configuraciones de fuente para texto de derecha a izquierda, y texto de derecha a izquierda.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | El tamaño de fuente en puntos usado en un documento de derecha a izquierda. |

### setSmallCaps(boolean value) {#setSmallCaps-boolean}
```
public void setSmallCaps(boolean value)
```


Verdadero si la fuente está formateada en letras capitales pequeñas.

 **Examples:** 

Muestra cómo formatear una ejecución para mostrar su contenido en mayúsculas.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // There are two ways of getting a run to display its lowercase text in uppercase without changing the contents.
 // 1 -  Set the AllCaps flag to display all characters in regular capitals:
 Run run = new Run(doc, "all capitals");
 run.getFont().setAllCaps(true);
 para.appendChild(run);

 para = (Paragraph) para.getParentNode().appendChild(new Paragraph(doc));

 // 2 -  Set the SmallCaps flag to display all characters in small capitals:
 // If a character is lower case, it will appear in its upper case form
 // but will have the same height as the lower case (the font's x-height).
 // Characters that were in upper case originally will look the same.
 run = new Run(doc, "Small Capitals");
 run.getFont().setSmallCaps(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.Caps.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setSnapToGrid(boolean value) {#setSnapToGrid-boolean}
```
public void setSnapToGrid(boolean value)
```


Especifica si la fuente actual debe usar la configuración de caracteres por línea de la cuadrícula del documento al diseñar.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setSpacing(double value) {#setSpacing-double}
```
public void setSpacing(double value)
```


Establece el espaciado (en puntos) entre caracteres.

 **Examples:** 

Muestra cómo establecer el escalado horizontal y el espaciado para los caracteres.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add run of text and increase character width to 150%.
 builder.getFont().setScaling(150);
 builder.writeln("Wide characters");

 // Add run of text and add 1pt of extra horizontal spacing between each character.
 builder.getFont().setSpacing(1.0);
 builder.writeln("Expanded by 1pt");

 // Add run of text and bring characters closer together by 1pt.
 builder.getFont().setSpacing(-1);
 builder.writeln("Condensed by 1pt");

 doc.save(getArtifactsDir() + "Font.ScalingSpacing.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | El espaciado (en puntos) entre caracteres. |

### setStrikeThrough(boolean value) {#setStrikeThrough-boolean}
```
public void setStrikeThrough(boolean value)
```


Verdadero si la fuente está formateada como texto tachado.

 **Examples:** 

Muestra cómo agregar una línea tachada al texto.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 Run run = new Run(doc, "Text with a single-line strikethrough.");
 run.getFont().setStrikeThrough(true);
 para.appendChild(run);

 para = (Paragraph) para.getParentNode().appendChild(new Paragraph(doc));

 run = new Run(doc, "Text with a double-line strikethrough.");
 run.getFont().setDoubleStrikeThrough(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.StrikeThrough.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setStyle(Style value) {#setStyle-com.aspose.words.Style}
```
public void setStyle(Style value)
```


Establece el estilo de carácter aplicado a este formato.

 **Examples:** 

Aplica un subrayado doble a todos los segmentos en un documento que están formateados con estilos de carácter personalizados.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a custom style and apply it to text created using a document builder.
 Style style = doc.getStyles().add(StyleType.CHARACTER, "MyStyle");
 style.getFont().setColor(Color.RED);
 style.getFont().setName("Courier New");

 builder.getFont().setStyleName("MyStyle");
 builder.write("This text is in a custom style.");

 // Iterate over every run and add a double underline to every custom style.
 for (Run run : (Iterable) doc.getChildNodes(NodeType.RUN, true)) {
     Style charStyle = run.getFont().getStyle();

     if (!charStyle.getBuiltIn())
         run.getFont().setUnderline(Underline.DOUBLE);
 }

 doc.save(getArtifactsDir() + "Font.Style.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | [Style](../../com.aspose.words/style/) | El estilo de carácter aplicado a este formato. |

### setStyleIdentifier(int value) {#setStyleIdentifier-int}
```
public void setStyleIdentifier(int value)
```


Establece el identificador de estilo independiente de la configuración regional del estilo de carácter aplicado a este formato.

 **Examples:** 

Muestra cómo cambiar el estilo del texto existente.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways of referencing styles.
 // 1 -  Using the style name:
 builder.getFont().setStyleName("Emphasis");
 builder.writeln("Text originally in \"Emphasis\" style");

 // 2 -  Using a built-in style identifier:
 builder.getFont().setStyleIdentifier(StyleIdentifier.INTENSE_EMPHASIS);
 builder.writeln("Text originally in \"Intense Emphasis\" style");

 // Convert all uses of one style to another,
 // using the above methods to reference old and new styles.
 for (Run run : (Iterable) doc.getChildNodes(NodeType.RUN, true)) {
     if (run.getFont().getStyleName().equals("Emphasis"))
         run.getFont().setStyleName("Strong");

     if (((run.getFont().getStyleIdentifier()) == (StyleIdentifier.INTENSE_EMPHASIS)))
         run.getFont().setStyleIdentifier(StyleIdentifier.STRONG);
 }

 doc.save(getArtifactsDir() + "Font.ChangeStyle.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El identificador de estilo independiente de la configuración regional del estilo de carácter aplicado a este formato. El valor debe ser uno de los constantes [StyleIdentifier](../../com.aspose.words/styleidentifier/). |

### setStyleName(String value) {#setStyleName-java.lang.String}
```
public void setStyleName(String value)
```


Establece el nombre del estilo de carácter aplicado a este formato.

 **Examples:** 

Muestra cómo cambiar el estilo del texto existente.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways of referencing styles.
 // 1 -  Using the style name:
 builder.getFont().setStyleName("Emphasis");
 builder.writeln("Text originally in \"Emphasis\" style");

 // 2 -  Using a built-in style identifier:
 builder.getFont().setStyleIdentifier(StyleIdentifier.INTENSE_EMPHASIS);
 builder.writeln("Text originally in \"Intense Emphasis\" style");

 // Convert all uses of one style to another,
 // using the above methods to reference old and new styles.
 for (Run run : (Iterable) doc.getChildNodes(NodeType.RUN, true)) {
     if (run.getFont().getStyleName().equals("Emphasis"))
         run.getFont().setStyleName("Strong");

     if (((run.getFont().getStyleIdentifier()) == (StyleIdentifier.INTENSE_EMPHASIS)))
         run.getFont().setStyleIdentifier(StyleIdentifier.STRONG);
 }

 doc.save(getArtifactsDir() + "Font.ChangeStyle.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El nombre del estilo de carácter aplicado a este formato. |

### setSubscript(boolean value) {#setSubscript-boolean}
```
public void setSubscript(boolean value)
```


Verdadero si la fuente está formateada como subíndice.

 **Examples:** 

Muestra cómo formatear el texto para desplazar su posición.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // Raise this run of text 5 points above the baseline.
 Run run = new Run(doc, "Raised text. ");
 run.getFont().setPosition(5.0);
 para.appendChild(run);

 // Lower this run of text 10 points below the baseline.
 run = new Run(doc, "Lowered text. ");
 run.getFont().setPosition(-10);
 para.appendChild(run);

 // Add a run of normal text.
 run = new Run(doc, "Text in its default position. ");
 para.appendChild(run);

 // Add a run of text that appears as subscript.
 run = new Run(doc, "Subscript. ");
 run.getFont().setSubscript(true);
 para.appendChild(run);

 // Add a run of text that appears as superscript.
 run = new Run(doc, "Superscript.");
 run.getFont().setSuperscript(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.PositionSubscript.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setSuperscript(boolean value) {#setSuperscript-boolean}
```
public void setSuperscript(boolean value)
```


Verdadero si la fuente está formateada como superíndice.

 **Examples:** 

Muestra cómo formatear el texto para desplazar su posición.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // Raise this run of text 5 points above the baseline.
 Run run = new Run(doc, "Raised text. ");
 run.getFont().setPosition(5.0);
 para.appendChild(run);

 // Lower this run of text 10 points below the baseline.
 run = new Run(doc, "Lowered text. ");
 run.getFont().setPosition(-10);
 para.appendChild(run);

 // Add a run of normal text.
 run = new Run(doc, "Text in its default position. ");
 para.appendChild(run);

 // Add a run of text that appears as subscript.
 run = new Run(doc, "Subscript. ");
 run.getFont().setSubscript(true);
 para.appendChild(run);

 // Add a run of text that appears as superscript.
 run = new Run(doc, "Superscript.");
 run.getFont().setSuperscript(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.PositionSubscript.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setTextEffect(int value) {#setTextEffect-int}
```
public void setTextEffect(int value)
```


Establece el efecto de animación de la fuente.

 **Examples:** 

Muestra cómo aplicar un efecto visual a una ejecución.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(36.0);
 builder.getFont().setTextEffect(TextEffect.SPARKLE_TEXT);

 builder.writeln("Text with a sparkle effect.");

 // Older versions of Microsoft Word only support font animation effects.
 doc.save(getArtifactsDir() + "Font.SparklingText.doc");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El efecto de animación de fuente. El valor debe ser uno de los constantes [TextEffect](../../com.aspose.words/texteffect/). |

### setTextureAlignment(int value) {#setTextureAlignment-int}
```
public void setTextureAlignment(int value)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int |  |

### setThemeColor(int value) {#setThemeColor-int}
```
public void setThemeColor(int value)
```


Establece el color del tema en el esquema de colores aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/).

 **Examples:** 

Muestra cómo trabajar con fuentes de tema y colores.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

Muestra cómo crear y usar estilos temáticos.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln();

 // Create some style with theme font properties.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "ThemedStyle");
 style.getFont().setThemeFont(ThemeFont.MAJOR);
 style.getFont().setThemeColor(ThemeColor.ACCENT_5);
 style.getFont().setTintAndShade(0.3);

 builder.getParagraphFormat().setStyleName("ThemedStyle");
 builder.writeln("Text with themed style");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El color de tema en el esquema de colores aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/). El valor debe ser uno de los constantes [ThemeColor](../../com.aspose.words/themecolor/). |

### setThemeFont(int value) {#setThemeFont-int}
```
public void setThemeFont(int value)
```


Establece la fuente del tema en el esquema de fuentes aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/).

 **Examples:** 

Muestra cómo trabajar con fuentes de tema y colores.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

Muestra cómo crear y usar estilos temáticos.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln();

 // Create some style with theme font properties.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "ThemedStyle");
 style.getFont().setThemeFont(ThemeFont.MAJOR);
 style.getFont().setThemeColor(ThemeColor.ACCENT_5);
 style.getFont().setTintAndShade(0.3);

 builder.getParagraphFormat().setStyleName("ThemedStyle");
 builder.writeln("Text with themed style");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | La fuente de tema en el esquema de fuentes aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/). El valor debe ser uno de los constantes [ThemeFont](../../com.aspose.words/themefont/). |

### setThemeFontAscii(int value) {#setThemeFontAscii-int}
```
public void setThemeFontAscii(int value)
```


Establece la fuente del tema utilizada para texto latino (caracteres con códigos de carácter de 0 (cero) a 127) en el esquema de fuentes aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/).

 **Examples:** 

Muestra cómo trabajar con fuentes de tema y colores.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | La fuente de tema utilizada para texto latino (caracteres con códigos de carácter de 0 (cero) a 127) en el esquema de fuentes aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/). El valor debe ser uno de los constantes [ThemeFont](../../com.aspose.words/themefont/). |

### setThemeFontBi(int value) {#setThemeFontBi-int}
```
public void setThemeFontBi(int value)
```


Establece la fuente del tema en el esquema de fuentes aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/) en un documento de idioma de derecha a izquierda.

 **Examples:** 

Muestra cómo trabajar con fuentes de tema y colores.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | La fuente de tema en el esquema de fuentes aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/) en un documento de idioma de derecha a izquierda. El valor debe ser uno de los constantes [ThemeFont](../../com.aspose.words/themefont/). |

### setThemeFontFarEast(int value) {#setThemeFontFarEast-int}
```
public void setThemeFontFarEast(int value)
```


Establece la fuente del tema de Asia Oriental en el esquema de fuentes aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/).

 **Examples:** 

Muestra cómo trabajar con fuentes de tema y colores.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | La fuente de tema de Asia Oriental en el esquema de fuentes aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/). El valor debe ser uno de los constantes [ThemeFont](../../com.aspose.words/themefont/). |

### setThemeFontOther(int value) {#setThemeFontOther-int}
```
public void setThemeFontOther(int value)
```


Establece la fuente del tema utilizada para caracteres con códigos de carácter de 128 a 255 en el esquema de fuentes aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/).

 **Examples:** 

Muestra cómo trabajar con fuentes de tema y colores.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | La fuente de tema utilizada para caracteres con códigos de carácter de 128 a 255 en el esquema de fuentes aplicado que está asociado con este objeto [Font](../../com.aspose.words/font/). El valor debe ser uno de los constantes [ThemeFont](../../com.aspose.words/themefont/). |

### setTintAndShade(double value) {#setTintAndShade-double}
```
public void setTintAndShade(double value)
```


Establece un valor double que aclara o oscurece un color.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | Un valor double que aclara o oscurece un color. |

### setUnderline(int value) {#setUnderline-int}
```
public void setUnderline(int value)
```


Establece el tipo de subrayado aplicado a la fuente.

 **Examples:** 

Muestra cómo insertar texto con formato usando DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

Muestra cómo insertar un campo de hipervínculo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("For more information, please visit the ");

 // Insert a hyperlink and emphasize it with custom formatting.
 // The hyperlink will be a clickable piece of text which will take us to the location specified in the URL.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 builder.insertHyperlink("Google website", "https://www.google.com", false);
 builder.getFont().clearFormatting();
 builder.writeln(".");

 // Ctrl + left clicking the link in the text in Microsoft Word will take us to the URL via a new web browser window.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlink.docx");
 
```

Muestra cómo configurar el estilo y el color de un subrayado de texto.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setUnderline(Underline.DOTTED);
 builder.getFont().setUnderlineColor(Color.RED);

 builder.writeln("Underlined text.");

 doc.save(getArtifactsDir() + "Font.Underlines.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El tipo de subrayado aplicado a la fuente. El valor debe ser uno de los constantes [Underline](../../com.aspose.words/underline/). |

### setUnderlineColor(Color value) {#setUnderlineColor-java.awt.Color}
```
public void setUnderlineColor(Color value)
```


Establece el color del subrayado aplicado a la fuente.

 **Examples:** 

Muestra cómo configurar el estilo y el color de un subrayado de texto.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setUnderline(Underline.DOTTED);
 builder.getFont().setUnderlineColor(Color.RED);

 builder.writeln("Underlined text.");

 doc.save(getArtifactsDir() + "Font.Underlines.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.awt.Color | El color del subrayado aplicado a la fuente. |

### solid() {#solid}
```
public void solid()
```




### twoColorGradient(int style, int variant) {#twoColorGradient-int-int}
```
public void twoColorGradient(int style, int variant)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| estilo | int |  |
| variant | int |  |

