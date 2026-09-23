---
title: "Ombrage"
linktitle: "Ombrage"
second_title: "Aspose.Words pour Java"
description: "Contient des attributs d’ombrage pour un objet en Java."
type: docs
weight: 609
url: /fr/java/com.aspose.words/shading/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.InternableComplexAttr](../../com.aspose.words/internablecomplexattr/)

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class Shading extends InternableComplexAttr implements Cloneable
```

Contient les attributs d'ombrage pour un objet.

Pour en savoir plus, consultez l'article de documentation [ Programming with Documents ][Programming with Documents].

 **Examples:** 

Montre comment appliquer la couleur de bordure et d’ombrage lors de la création d'un tableau.

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

Montre comment décorer le texte avec des bordures et de l’ombrage.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Supprime l’ombrage de l’objet. |
| [equals(Shading rhs)](#equals-com.aspose.words.Shading) | Détermine si le [Shading](../../com.aspose.words/shading/) spécifié est égal en valeur au [Shading](../../com.aspose.words/shading/) actuel. |
| [equals(Object obj)](#equals-java.lang.Object) | Détermine si l'objet spécifié est égal en valeur à l'objet actuel. |
| [getBackgroundPatternColor()](#getBackgroundPatternColor) | Obtient la couleur appliquée à l’arrière-plan de l’objet [Shading](../../com.aspose.words/shading/). |
| [getBackgroundPatternThemeColor()](#getBackgroundPatternThemeColor) | Obtient la couleur du thème du motif d’arrière-plan dans le schéma de couleurs appliqué associé à cet objet [Shading](../../com.aspose.words/shading/). |
| [getBackgroundTintAndShade()](#getBackgroundTintAndShade) | Obtient une valeur double qui éclaircit ou assombrit une couleur de thème d’arrière-plan. |
| [getForegroundPatternColor()](#getForegroundPatternColor) | Obtient la couleur appliquée au premier plan de l’objet [Shading](../../com.aspose.words/shading/). |
| [getForegroundPatternThemeColor()](#getForegroundPatternThemeColor) | Obtient la couleur du thème du motif de premier plan dans le schéma de couleurs appliqué associé à cet objet [Shading](../../com.aspose.words/shading/). |
| [getForegroundTintAndShade()](#getForegroundTintAndShade) | Obtient une valeur double qui éclaircit ou assombrit une couleur de thème de premier plan. |
| [getTexture()](#getTexture) | Obtient la texture d’ombrage. |
| [hashCode()](#hashCode) |  |
| [isInheritedComplexAttr()](#isInheritedComplexAttr) |  |
| [setBackgroundPatternColor(Color value)](#setBackgroundPatternColor-java.awt.Color) | Définit la couleur appliquée à l’arrière-plan de l’objet [Shading](../../com.aspose.words/shading/). |
| [setBackgroundPatternThemeColor(int value)](#setBackgroundPatternThemeColor-int) | Définit la couleur du thème du motif d’arrière-plan dans le schéma de couleurs appliqué associé à cet objet [Shading](../../com.aspose.words/shading/). |
| [setBackgroundTintAndShade(double value)](#setBackgroundTintAndShade-double) | Définit une valeur double qui éclaircit ou assombrit une couleur de thème d’arrière-plan. |
| [setForegroundPatternColor(Color value)](#setForegroundPatternColor-java.awt.Color) | Définit la couleur appliquée au premier plan de l’objet [Shading](../../com.aspose.words/shading/). |
| [setForegroundPatternThemeColor(int value)](#setForegroundPatternThemeColor-int) | Définit la couleur du thème du motif de premier plan dans le schéma de couleurs appliqué associé à cet objet [Shading](../../com.aspose.words/shading/). |
| [setForegroundTintAndShade(double value)](#setForegroundTintAndShade-double) | Définit une valeur double qui éclaircit ou assombrit une couleur de thème de premier plan. |
| [setTexture(int value)](#setTexture-int) | Définit la texture d’ombrage. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Supprime l’ombrage de l’objet.

 **Examples:** 

Montre comment créer un tableau avec des bordures personnalisées.

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


Détermine si le [Shading](../../com.aspose.words/shading/) spécifié est égal en valeur au [Shading](../../com.aspose.words/shading/) actuel.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| rhs | [Shading](../../com.aspose.words/shading/) |  |

**Returns:**
boolean
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Détermine si l'objet spécifié est égal en valeur à l'objet actuel.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getBackgroundPatternColor() {#getBackgroundPatternColor}
```
public Color getBackgroundPatternColor()
```


Obtient la couleur appliquée à l’arrière-plan de l’objet [Shading](../../com.aspose.words/shading/).

 **Examples:** 

Montre comment décorer le texte avec des bordures et de l’ombrage.

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
java.awt.Color - La couleur appliquée à l’arrière-plan de l’objet [Shading](../../com.aspose.words/shading/).
### getBackgroundPatternThemeColor() {#getBackgroundPatternThemeColor}
```
public int getBackgroundPatternThemeColor()
```


Obtient la couleur du thème du motif d’arrière-plan dans le schéma de couleurs appliqué associé à cet objet [Shading](../../com.aspose.words/shading/).

 **Examples:** 

Montre comment définir les couleurs de premier plan et d’arrière-plan pour la texture d’ombrage.

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
int - La couleur du thème du motif d’arrière-plan dans le schéma de couleurs appliqué associé à cet objet [Shading](../../com.aspose.words/shading/). La valeur retournée est l’une des constantes [ThemeColor](../../com.aspose.words/themecolor/).
### getBackgroundTintAndShade() {#getBackgroundTintAndShade}
```
public double getBackgroundTintAndShade()
```


Obtient une valeur double qui éclaircit ou assombrit une couleur de thème d’arrière-plan.

**Returns:**
double - Une valeur double qui éclaircit ou assombrit une couleur de thème d’arrière-plan.
### getForegroundPatternColor() {#getForegroundPatternColor}
```
public Color getForegroundPatternColor()
```


Obtient la couleur appliquée au premier plan de l’objet [Shading](../../com.aspose.words/shading/).

 **Examples:** 

Montre comment décorer le texte avec des bordures et de l’ombrage.

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
java.awt.Color - La couleur appliquée au premier plan de l’objet [Shading](../../com.aspose.words/shading/).
### getForegroundPatternThemeColor() {#getForegroundPatternThemeColor}
```
public int getForegroundPatternThemeColor()
```


Obtient la couleur du thème du motif de premier plan dans le schéma de couleurs appliqué associé à cet objet [Shading](../../com.aspose.words/shading/).

 **Examples:** 

Montre comment définir les couleurs de premier plan et d’arrière-plan pour la texture d’ombrage.

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
int - La couleur du thème du motif de premier plan dans le schéma de couleurs appliqué associé à cet objet [Shading](../../com.aspose.words/shading/). La valeur retournée est l’une des constantes [ThemeColor](../../com.aspose.words/themecolor/).
### getForegroundTintAndShade() {#getForegroundTintAndShade}
```
public double getForegroundTintAndShade()
```


Obtient une valeur double qui éclaircit ou assombrit une couleur de thème de premier plan.

**Returns:**
double - Une valeur double qui éclaircit ou assombrit une couleur de thème d'avant-plan.
### getTexture() {#getTexture}
```
public int getTexture()
```


Obtient la texture d’ombrage.

 **Examples:** 

Montre comment décorer le texte avec des bordures et de l’ombrage.

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
int - La texture de l'ombrage. La valeur retournée est l'une des constantes [TextureIndex](../../com.aspose.words/textureindex/).
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


Définit la couleur appliquée à l’arrière-plan de l’objet [Shading](../../com.aspose.words/shading/).

 **Examples:** 

Montre comment décorer le texte avec des bordures et de l’ombrage.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | La couleur appliquée à l'arrière-plan de l'objet [Shading](../../com.aspose.words/shading/). |

### setBackgroundPatternThemeColor(int value) {#setBackgroundPatternThemeColor-int}
```
public void setBackgroundPatternThemeColor(int value)
```


Définit la couleur du thème du motif d’arrière-plan dans le schéma de couleurs appliqué associé à cet objet [Shading](../../com.aspose.words/shading/).

 **Examples:** 

Montre comment définir les couleurs de premier plan et d’arrière-plan pour la texture d’ombrage.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La couleur de thème du motif d'arrière-plan dans le schéma de couleurs appliqué qui est associée à cet objet [Shading](../../com.aspose.words/shading/). La valeur doit être l'une des constantes [ThemeColor](../../com.aspose.words/themecolor/). |

### setBackgroundTintAndShade(double value) {#setBackgroundTintAndShade-double}
```
public void setBackgroundTintAndShade(double value)
```


Définit une valeur double qui éclaircit ou assombrit une couleur de thème d’arrière-plan.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | Une valeur double qui éclaircit ou assombrit une couleur de thème d'arrière-plan. |

### setForegroundPatternColor(Color value) {#setForegroundPatternColor-java.awt.Color}
```
public void setForegroundPatternColor(Color value)
```


Définit la couleur appliquée au premier plan de l’objet [Shading](../../com.aspose.words/shading/).

 **Examples:** 

Montre comment décorer le texte avec des bordures et de l’ombrage.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | La couleur appliquée au premier plan de l'objet [Shading](../../com.aspose.words/shading/). |

### setForegroundPatternThemeColor(int value) {#setForegroundPatternThemeColor-int}
```
public void setForegroundPatternThemeColor(int value)
```


Définit la couleur du thème du motif de premier plan dans le schéma de couleurs appliqué associé à cet objet [Shading](../../com.aspose.words/shading/).

 **Examples:** 

Montre comment définir les couleurs de premier plan et d’arrière-plan pour la texture d’ombrage.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La couleur de thème du motif de premier plan dans le schéma de couleurs appliqué qui est associée à cet objet [Shading](../../com.aspose.words/shading/). La valeur doit être l'une des constantes [ThemeColor](../../com.aspose.words/themecolor/). |

### setForegroundTintAndShade(double value) {#setForegroundTintAndShade-double}
```
public void setForegroundTintAndShade(double value)
```


Définit une valeur double qui éclaircit ou assombrit une couleur de thème de premier plan.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | Une valeur double qui éclaircit ou assombrit une couleur de thème d'avant-plan. |

### setTexture(int value) {#setTexture-int}
```
public void setTexture(int value)
```


Définit la texture d’ombrage.

 **Examples:** 

Montre comment décorer le texte avec des bordures et de l’ombrage.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La texture de l'ombrage. La valeur doit être l'une des constantes [TextureIndex](../../com.aspose.words/textureindex/). |

