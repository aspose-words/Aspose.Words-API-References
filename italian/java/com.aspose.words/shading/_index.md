---
title: "Ombreggiatura"
linktitle: "Ombreggiatura"
second_title: "Aspose.Words per Java"
description: "Contiene attributi di ombreggiatura per un oggetto in Java."
type: docs
weight: 609
url: /it/java/com.aspose.words/shading/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.InternableComplexAttr](../../com.aspose.words/internablecomplexattr/)

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class Shading extends InternableComplexAttr implements Cloneable
```

Contiene attributi di ombreggiatura per un oggetto.

Per saperne di più, visita l'articolo di documentazione [ Programmare con i Documenti ][Programming with Documents].

 **Examples:** 

Mostra come applicare il colore del bordo e dell'ombreggiatura durante la creazione di una tabella.

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

Mostra come decorare il testo con bordi e ombreggiatura.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Rimuove l'ombreggiatura dall'oggetto. |
| [equals(Shading rhs)](#equals-com.aspose.words.Shading) | Determina se il [Shading](../../com.aspose.words/shading/) specificato è uguale in valore al [Shading](../../com.aspose.words/shading/) corrente. |
| [equals(Object obj)](#equals-java.lang.Object) | Determina se l'oggetto specificato è uguale in valore all'oggetto corrente. |
| [getBackgroundPatternColor()](#getBackgroundPatternColor) | Ottiene il colore applicato allo sfondo dell'oggetto [Shading](../../com.aspose.words/shading/). |
| [getBackgroundPatternThemeColor()](#getBackgroundPatternThemeColor) | Ottiene il colore tematico del motivo di sfondo nello schema colore applicato associato a questo oggetto [Shading](../../com.aspose.words/shading/). |
| [getBackgroundTintAndShade()](#getBackgroundTintAndShade) | Ottiene un valore double che schiarisce o scurisce un colore tematico di sfondo. |
| [getForegroundPatternColor()](#getForegroundPatternColor) | Ottiene il colore applicato al primo piano dell'oggetto [Shading](../../com.aspose.words/shading/). |
| [getForegroundPatternThemeColor()](#getForegroundPatternThemeColor) | Ottiene il colore tematico del motivo di primo piano nello schema colore applicato associato a questo oggetto [Shading](../../com.aspose.words/shading/). |
| [getForegroundTintAndShade()](#getForegroundTintAndShade) | Ottiene un valore double che schiarisce o scurisce un colore tematico di primo piano. |
| [getTexture()](#getTexture) | Ottiene la texture di ombreggiatura. |
| [hashCode()](#hashCode) |  |
| [isInheritedComplexAttr()](#isInheritedComplexAttr) |  |
| [setBackgroundPatternColor(Color value)](#setBackgroundPatternColor-java.awt.Color) | Imposta il colore applicato allo sfondo dell'oggetto [Shading](../../com.aspose.words/shading/). |
| [setBackgroundPatternThemeColor(int value)](#setBackgroundPatternThemeColor-int) | Imposta il colore tematico del motivo di sfondo nello schema colore applicato associato a questo oggetto [Shading](../../com.aspose.words/shading/). |
| [setBackgroundTintAndShade(double value)](#setBackgroundTintAndShade-double) | Imposta un valore double che schiarisce o scurisce un colore tematico di sfondo. |
| [setForegroundPatternColor(Color value)](#setForegroundPatternColor-java.awt.Color) | Imposta il colore applicato al primo piano dell'oggetto [Shading](../../com.aspose.words/shading/). |
| [setForegroundPatternThemeColor(int value)](#setForegroundPatternThemeColor-int) | Imposta il colore tematico del motivo di primo piano nello schema colore applicato associato a questo oggetto [Shading](../../com.aspose.words/shading/). |
| [setForegroundTintAndShade(double value)](#setForegroundTintAndShade-double) | Imposta un valore double che schiarisce o scurisce un colore tematico di primo piano. |
| [setTexture(int value)](#setTexture-int) | Imposta la texture di ombreggiatura. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Rimuove l'ombreggiatura dall'oggetto.

 **Examples:** 

Mostra come creare una tabella con bordi personalizzati.

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


Determina se il [Shading](../../com.aspose.words/shading/) specificato è uguale in valore al [Shading](../../com.aspose.words/shading/) corrente.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| rhs | [Shading](../../com.aspose.words/shading/) |  |

**Returns:**
boolean
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Determina se l'oggetto specificato è uguale in valore all'oggetto corrente.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getBackgroundPatternColor() {#getBackgroundPatternColor}
```
public Color getBackgroundPatternColor()
```


Ottiene il colore applicato allo sfondo dell'oggetto [Shading](../../com.aspose.words/shading/).

 **Examples:** 

Mostra come decorare il testo con bordi e ombreggiatura.

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
java.awt.Color - Il colore applicato allo sfondo dell'oggetto [Shading](../../com.aspose.words/shading/).
### getBackgroundPatternThemeColor() {#getBackgroundPatternThemeColor}
```
public int getBackgroundPatternThemeColor()
```


Ottiene il colore tematico del motivo di sfondo nello schema colore applicato associato a questo oggetto [Shading](../../com.aspose.words/shading/).

 **Examples:** 

Mostra come impostare i colori di primo piano e di sfondo per la texture di ombreggiatura.

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
int - Il colore tematico del motivo di sfondo nello schema colore applicato associato a questo oggetto [Shading](../../com.aspose.words/shading/). Il valore restituito è una delle costanti [ThemeColor](../../com.aspose.words/themecolor/).
### getBackgroundTintAndShade() {#getBackgroundTintAndShade}
```
public double getBackgroundTintAndShade()
```


Ottiene un valore double che schiarisce o scurisce un colore tematico di sfondo.

**Returns:**
double - Un valore double che schiarisce o scurisce un colore tematico di sfondo.
### getForegroundPatternColor() {#getForegroundPatternColor}
```
public Color getForegroundPatternColor()
```


Ottiene il colore applicato al primo piano dell'oggetto [Shading](../../com.aspose.words/shading/).

 **Examples:** 

Mostra come decorare il testo con bordi e ombreggiatura.

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
java.awt.Color - Il colore applicato al primo piano dell'oggetto [Shading](../../com.aspose.words/shading/).
### getForegroundPatternThemeColor() {#getForegroundPatternThemeColor}
```
public int getForegroundPatternThemeColor()
```


Ottiene il colore tematico del motivo di primo piano nello schema colore applicato associato a questo oggetto [Shading](../../com.aspose.words/shading/).

 **Examples:** 

Mostra come impostare i colori di primo piano e di sfondo per la texture di ombreggiatura.

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
int - Il colore tematico del motivo di primo piano nello schema colore applicato associato a questo oggetto [Shading](../../com.aspose.words/shading/). Il valore restituito è una delle costanti [ThemeColor](../../com.aspose.words/themecolor/).
### getForegroundTintAndShade() {#getForegroundTintAndShade}
```
public double getForegroundTintAndShade()
```


Ottiene un valore double che schiarisce o scurisce un colore tematico di primo piano.

**Returns:**
double - Un valore double che schiarisce o scurisce un colore di tema in primo piano.
### getTexture() {#getTexture}
```
public int getTexture()
```


Ottiene la texture di ombreggiatura.

 **Examples:** 

Mostra come decorare il testo con bordi e ombreggiatura.

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
int - La texture di ombreggiatura. Il valore restituito è uno dei costanti [TextureIndex](../../com.aspose.words/textureindex/).
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


Imposta il colore applicato allo sfondo dell'oggetto [Shading](../../com.aspose.words/shading/).

 **Examples:** 

Mostra come decorare il testo con bordi e ombreggiatura.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | java.awt.Color | Il colore applicato allo sfondo dell'oggetto [Shading](../../com.aspose.words/shading/). |

### setBackgroundPatternThemeColor(int value) {#setBackgroundPatternThemeColor-int}
```
public void setBackgroundPatternThemeColor(int value)
```


Imposta il colore tematico del motivo di sfondo nello schema colore applicato associato a questo oggetto [Shading](../../com.aspose.words/shading/).

 **Examples:** 

Mostra come impostare i colori di primo piano e di sfondo per la texture di ombreggiatura.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il colore di tema del motivo di sfondo nello schema colori applicato associato a questo oggetto [Shading](../../com.aspose.words/shading/). Il valore deve essere uno dei costanti [ThemeColor](../../com.aspose.words/themecolor/). |

### setBackgroundTintAndShade(double value) {#setBackgroundTintAndShade-double}
```
public void setBackgroundTintAndShade(double value)
```


Imposta un valore double che schiarisce o scurisce un colore tematico di sfondo.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | Un valore double che schiarisce o scurisce un colore di tema di sfondo. |

### setForegroundPatternColor(Color value) {#setForegroundPatternColor-java.awt.Color}
```
public void setForegroundPatternColor(Color value)
```


Imposta il colore applicato al primo piano dell'oggetto [Shading](../../com.aspose.words/shading/).

 **Examples:** 

Mostra come decorare il testo con bordi e ombreggiatura.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | java.awt.Color | Il colore applicato al primo piano dell'oggetto [Shading](../../com.aspose.words/shading/). |

### setForegroundPatternThemeColor(int value) {#setForegroundPatternThemeColor-int}
```
public void setForegroundPatternThemeColor(int value)
```


Imposta il colore tematico del motivo di primo piano nello schema colore applicato associato a questo oggetto [Shading](../../com.aspose.words/shading/).

 **Examples:** 

Mostra come impostare i colori di primo piano e di sfondo per la texture di ombreggiatura.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il colore di tema del motivo di primo piano nello schema colori applicato associato a questo oggetto [Shading](../../com.aspose.words/shading/). Il valore deve essere uno dei costanti [ThemeColor](../../com.aspose.words/themecolor/). |

### setForegroundTintAndShade(double value) {#setForegroundTintAndShade-double}
```
public void setForegroundTintAndShade(double value)
```


Imposta un valore double che schiarisce o scurisce un colore tematico di primo piano.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | Un valore double che schiarisce o scurisce un colore di tema in primo piano. |

### setTexture(int value) {#setTexture-int}
```
public void setTexture(int value)
```


Imposta la texture di ombreggiatura.

 **Examples:** 

Mostra come decorare il testo con bordi e ombreggiatura.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | La texture di ombreggiatura. Il valore deve essere uno dei costanti [TextureIndex](../../com.aspose.words/textureindex/). |

