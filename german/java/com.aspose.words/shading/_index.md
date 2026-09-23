---
title: "Schattierung"
linktitle: "Schattierung"
second_title: "Aspose.Words für Java"
description: "Enthält Schattierungsattribute für ein Objekt in Java."
type: docs
weight: 609
url: /de/java/com.aspose.words/shading/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.InternableComplexAttr](../../com.aspose.words/internablecomplexattr/)

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class Shading extends InternableComplexAttr implements Cloneable
```

Enthält Schattierungsattribute für ein Objekt.

Weitere Informationen finden Sie im Dokumentationsartikel [ Programming with Documents ][Programming with Documents].

 **Examples:** 

Zeigt, wie man Rahmen- und Schattierungsfarbe beim Erstellen einer Tabelle anwendet.

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

Zeigt, wie man Text mit Rahmen und Schattierung dekoriert.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Entfernt die Schattierung vom Objekt. |
| [equals(Shading rhs)](#equals-com.aspose.words.Shading) | Bestimmt, ob das angegebene [Shading](../../com.aspose.words/shading/) im Wert dem aktuellen [Shading](../../com.aspose.words/shading/) entspricht. |
| [equals(Object obj)](#equals-java.lang.Object) | Bestimmt, ob das angegebene Objekt im Wert dem aktuellen Objekt entspricht. |
| [getBackgroundPatternColor()](#getBackgroundPatternColor) | Ermittelt die Farbe, die auf den Hintergrund des [Shading](../../com.aspose.words/shading/) Objekts angewendet wird. |
| [getBackgroundPatternThemeColor()](#getBackgroundPatternThemeColor) | Ermittelt die Hintergrundmuster-Themenfarbe im angewendeten Farbschema, die mit diesem [Shading](../../com.aspose.words/shading/) Objekt verknüpft ist. |
| [getBackgroundTintAndShade()](#getBackgroundTintAndShade) | Ermittelt einen double-Wert, der eine Hintergrund-Themenfarbe aufhellt oder abdunkelt. |
| [getForegroundPatternColor()](#getForegroundPatternColor) | Ermittelt die Farbe, die auf den Vordergrund des [Shading](../../com.aspose.words/shading/) Objekts angewendet wird. |
| [getForegroundPatternThemeColor()](#getForegroundPatternThemeColor) | Ermittelt die Vordergrundmuster-Themenfarbe im angewendeten Farbschema, die mit diesem [Shading](../../com.aspose.words/shading/) Objekt verknüpft ist. |
| [getForegroundTintAndShade()](#getForegroundTintAndShade) | Ermittelt einen double-Wert, der eine Vordergrund-Themenfarbe aufhellt oder abdunkelt. |
| [getTexture()](#getTexture) | Ermittelt die Schattierungstextur. |
| [hashCode()](#hashCode) |  |
| [isInheritedComplexAttr()](#isInheritedComplexAttr) |  |
| [setBackgroundPatternColor(Color value)](#setBackgroundPatternColor-java.awt.Color) | Legt die Farbe fest, die auf den Hintergrund des [Shading](../../com.aspose.words/shading/) Objekts angewendet wird. |
| [setBackgroundPatternThemeColor(int value)](#setBackgroundPatternThemeColor-int) | Legt die Hintergrundmuster-Themenfarbe im angewendeten Farbschema fest, die mit diesem [Shading](../../com.aspose.words/shading/) Objekt verknüpft ist. |
| [setBackgroundTintAndShade(double value)](#setBackgroundTintAndShade-double) | Legt einen double-Wert fest, der eine Hintergrund-Themenfarbe aufhellt oder abdunkelt. |
| [setForegroundPatternColor(Color value)](#setForegroundPatternColor-java.awt.Color) | Legt die Farbe fest, die auf den Vordergrund des [Shading](../../com.aspose.words/shading/) Objekts angewendet wird. |
| [setForegroundPatternThemeColor(int value)](#setForegroundPatternThemeColor-int) | Legt die Vordergrundmuster-Themenfarbe im angewendeten Farbschema fest, die mit diesem [Shading](../../com.aspose.words/shading/) Objekt verknüpft ist. |
| [setForegroundTintAndShade(double value)](#setForegroundTintAndShade-double) | Legt einen double-Wert fest, der eine Vordergrund-Themenfarbe aufhellt oder abdunkelt. |
| [setTexture(int value)](#setTexture-int) | Legt die Schattierungstextur fest. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Entfernt die Schattierung vom Objekt.

 **Examples:** 

Zeigt, wie man eine Tabelle mit benutzerdefinierten Rahmen erstellt.

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


Bestimmt, ob das angegebene [Shading](../../com.aspose.words/shading/) im Wert dem aktuellen [Shading](../../com.aspose.words/shading/) entspricht.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| rhs | [Shading](../../com.aspose.words/shading/) |  |

**Returns:**
boolean
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Bestimmt, ob das angegebene Objekt im Wert dem aktuellen Objekt entspricht.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getBackgroundPatternColor() {#getBackgroundPatternColor}
```
public Color getBackgroundPatternColor()
```


Ermittelt die Farbe, die auf den Hintergrund des [Shading](../../com.aspose.words/shading/) Objekts angewendet wird.

 **Examples:** 

Zeigt, wie man Text mit Rahmen und Schattierung dekoriert.

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
java.awt.Color - Die Farbe, die auf den Hintergrund des [Shading](../../com.aspose.words/shading/) Objekts angewendet wird.
### getBackgroundPatternThemeColor() {#getBackgroundPatternThemeColor}
```
public int getBackgroundPatternThemeColor()
```


Ermittelt die Hintergrundmuster-Themenfarbe im angewendeten Farbschema, die mit diesem [Shading](../../com.aspose.words/shading/) Objekt verknüpft ist.

 **Examples:** 

Zeigt, wie man Vorder- und Hintergrundfarben für die Schattierungstextur festlegt.

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
int - Die Hintergrundmuster-Themenfarbe im angewendeten Farbschema, die mit diesem [Shading](../../com.aspose.words/shading/) Objekt verknüpft ist. Der zurückgegebene Wert ist einer der Konstanten von [ThemeColor](../../com.aspose.words/themecolor/).
### getBackgroundTintAndShade() {#getBackgroundTintAndShade}
```
public double getBackgroundTintAndShade()
```


Ermittelt einen double-Wert, der eine Hintergrund-Themenfarbe aufhellt oder abdunkelt.

**Returns:**
double - Ein double-Wert, der eine Hintergrund-Themenfarbe aufhellt oder abdunkelt.
### getForegroundPatternColor() {#getForegroundPatternColor}
```
public Color getForegroundPatternColor()
```


Ermittelt die Farbe, die auf den Vordergrund des [Shading](../../com.aspose.words/shading/) Objekts angewendet wird.

 **Examples:** 

Zeigt, wie man Text mit Rahmen und Schattierung dekoriert.

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
java.awt.Color - Die Farbe, die auf den Vordergrund des [Shading](../../com.aspose.words/shading/) Objekts angewendet wird.
### getForegroundPatternThemeColor() {#getForegroundPatternThemeColor}
```
public int getForegroundPatternThemeColor()
```


Ermittelt die Vordergrundmuster-Themenfarbe im angewendeten Farbschema, die mit diesem [Shading](../../com.aspose.words/shading/) Objekt verknüpft ist.

 **Examples:** 

Zeigt, wie man Vorder- und Hintergrundfarben für die Schattierungstextur festlegt.

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
int - Die Vordergrundmuster-Themenfarbe im angewendeten Farbschema, die mit diesem [Shading](../../com.aspose.words/shading/) Objekt verknüpft ist. Der zurückgegebene Wert ist einer der Konstanten von [ThemeColor](../../com.aspose.words/themecolor/).
### getForegroundTintAndShade() {#getForegroundTintAndShade}
```
public double getForegroundTintAndShade()
```


Ermittelt einen double-Wert, der eine Vordergrund-Themenfarbe aufhellt oder abdunkelt.

**Returns:**
double - Ein double-Wert, der eine Vordergrund-Themenfarbe aufhellt oder abdunkelt.
### getTexture() {#getTexture}
```
public int getTexture()
```


Ermittelt die Schattierungstextur.

 **Examples:** 

Zeigt, wie man Text mit Rahmen und Schattierung dekoriert.

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
int - Die Schattierungstextur. Der zurückgegebene Wert ist einer der [TextureIndex](../../com.aspose.words/textureindex/) Konstanten.
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


Legt die Farbe fest, die auf den Hintergrund des [Shading](../../com.aspose.words/shading/) Objekts angewendet wird.

 **Examples:** 

Zeigt, wie man Text mit Rahmen und Schattierung dekoriert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | java.awt.Color | Die Farbe, die auf den Hintergrund des [Shading](../../com.aspose.words/shading/) Objekts angewendet wird. |

### setBackgroundPatternThemeColor(int value) {#setBackgroundPatternThemeColor-int}
```
public void setBackgroundPatternThemeColor(int value)
```


Legt die Hintergrundmuster-Themenfarbe im angewendeten Farbschema fest, die mit diesem [Shading](../../com.aspose.words/shading/) Objekt verknüpft ist.

 **Examples:** 

Zeigt, wie man Vorder- und Hintergrundfarben für die Schattierungstextur festlegt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Die Hintergrundmuster-Themefarbe im angewendeten Farbschema, die mit diesem [Shading](../../com.aspose.words/shading/) Objekt verknüpft ist. Der Wert muss einer der [ThemeColor](../../com.aspose.words/themecolor/) Konstanten sein. |

### setBackgroundTintAndShade(double value) {#setBackgroundTintAndShade-double}
```
public void setBackgroundTintAndShade(double value)
```


Legt einen double-Wert fest, der eine Hintergrund-Themenfarbe aufhellt oder abdunkelt.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Ein double-Wert, der eine Hintergrund-Themefarbe aufhellt oder abdunkelt. |

### setForegroundPatternColor(Color value) {#setForegroundPatternColor-java.awt.Color}
```
public void setForegroundPatternColor(Color value)
```


Legt die Farbe fest, die auf den Vordergrund des [Shading](../../com.aspose.words/shading/) Objekts angewendet wird.

 **Examples:** 

Zeigt, wie man Text mit Rahmen und Schattierung dekoriert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | java.awt.Color | Die Farbe, die auf den Vordergrund des [Shading](../../com.aspose.words/shading/) Objekts angewendet wird. |

### setForegroundPatternThemeColor(int value) {#setForegroundPatternThemeColor-int}
```
public void setForegroundPatternThemeColor(int value)
```


Legt die Vordergrundmuster-Themenfarbe im angewendeten Farbschema fest, die mit diesem [Shading](../../com.aspose.words/shading/) Objekt verknüpft ist.

 **Examples:** 

Zeigt, wie man Vorder- und Hintergrundfarben für die Schattierungstextur festlegt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Die Vordergrundmuster-Themefarbe im angewendeten Farbschema, die mit diesem [Shading](../../com.aspose.words/shading/) Objekt verknüpft ist. Der Wert muss einer der [ThemeColor](../../com.aspose.words/themecolor/) Konstanten sein. |

### setForegroundTintAndShade(double value) {#setForegroundTintAndShade-double}
```
public void setForegroundTintAndShade(double value)
```


Legt einen double-Wert fest, der eine Vordergrund-Themenfarbe aufhellt oder abdunkelt.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Ein double-Wert, der eine Vordergrund-Themefarbe aufhellt oder abdunkelt. |

### setTexture(int value) {#setTexture-int}
```
public void setTexture(int value)
```


Legt die Schattierungstextur fest.

 **Examples:** 

Zeigt, wie man Text mit Rahmen und Schattierung dekoriert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Die Schattierungstextur. Der Wert muss einer der [TextureIndex](../../com.aspose.words/textureindex/) Konstanten sein. |

