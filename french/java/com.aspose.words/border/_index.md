---
title: "Bordure"
linktitle: "Bordure"
second_title: "Aspose.Words pour Java"
description: "Représente une bordure d'un objet en Java."
type: docs
weight: 46
url: /fr/java/com.aspose.words/border/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.InternableComplexAttr](../../com.aspose.words/internablecomplexattr/)

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class Border extends InternableComplexAttr implements Cloneable
```

Représente une bordure d'un objet.

Pour en savoir plus, consultez l'article de documentation [ Programming with Documents ][Programming with Documents].

 **Remarks:** 

Les bordures peuvent être appliquées à divers éléments de document, y compris le paragraphe, la séquence de texte à l'intérieur d'un paragraphe ou une cellule de tableau.

 **Examples:** 

Montre comment insérer une chaîne entourée d'une bordure dans un document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

Montre comment insérer un paragraphe avec une bordure supérieure.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Réinitialise les propriétés de bordure aux valeurs par défaut. |
| [equals(Border rhs)](#equals-com.aspose.words.Border) | Détermine si la bordure spécifiée est égale en valeur à la bordure actuelle. |
| [equals(Object obj)](#equals-java.lang.Object) | Détermine si l'objet spécifié est égal en valeur à l'objet actuel. |
| [getColor()](#getColor) | Obtient la couleur de la bordure. |
| [getDistanceFromText()](#getDistanceFromText) | Obtient la distance de la bordure par rapport au texte ou au bord de la page en points. |
| [getLineStyle()](#getLineStyle) | Obtient le style de la bordure. |
| [getLineWidth()](#getLineWidth) | Obtient la largeur de la bordure en points. |
| [getShadow()](#getShadow) | Obtient une valeur indiquant si la bordure possède une ombre. |
| [getThemeColor()](#getThemeColor) | Obtient la couleur du thème dans le schéma de couleurs appliqué qui est associé à cet objet Border. |
| [getTintAndShade()](#getTintAndShade) | Obtient une valeur double qui éclaircit ou assombrit une couleur. |
| [hashCode()](#hashCode) |  |
| [isInheritedComplexAttr()](#isInheritedComplexAttr) |  |
| [isVisible()](#isVisible) | Renvoie  true  si le [getLineStyle()](../../com.aspose.words/border/\#getLineStyle) / [setLineStyle(int)](../../com.aspose.words/border/\#setLineStyle-int) n'est pas [LineStyle.NONE](../../com.aspose.words/linestyle/\#NONE). |
| [setColor(Color value)](#setColor-java.awt.Color) | Définit la couleur de la bordure. |
| [setDistanceFromText(double value)](#setDistanceFromText-double) | Définit la distance de la bordure par rapport au texte ou au bord de la page en points. |
| [setLineStyle(int value)](#setLineStyle-int) | Définit le style de la bordure. |
| [setLineWidth(double value)](#setLineWidth-double) | Définit la largeur de la bordure en points. |
| [setShadow(boolean value)](#setShadow-boolean) | Définit une valeur indiquant si la bordure possède une ombre. |
| [setThemeColor(int value)](#setThemeColor-int) | Définit la couleur du thème dans le schéma de couleurs appliqué qui est associé à cet objet Border. |
| [setTintAndShade(double value)](#setTintAndShade-double) | Définit une valeur double qui éclaircit ou assombrit une couleur. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Réinitialise les propriétés de bordure aux valeurs par défaut.

 **Remarks:** 

Lorsque les propriétés de bordure sont réinitialisées aux valeurs par défaut, la bordure est invisible.

 **Examples:** 

Montre comment supprimer les bordures d'un paragraphe.

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


Détermine si la bordure spécifiée est égale en valeur à la bordure actuelle.

 **Examples:** 

Montre comment les collections de bordures peuvent partager des éléments.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| rhs | [Border](../../com.aspose.words/border/) |  |

**Returns:**
boolean
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Détermine si l'objet spécifié est égal en valeur à l'objet actuel.

 **Examples:** 

Montre comment les collections de bordures peuvent partager des éléments.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getColor() {#getColor}
```
public Color getColor()
```


Obtient la couleur de la bordure.

 **Examples:** 

Montre comment insérer une chaîne entourée d'une bordure dans un document.

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
java.awt.Color - La couleur de la bordure.
### getDistanceFromText() {#getDistanceFromText}
```
public double getDistanceFromText()
```


Obtient la distance de la bordure par rapport au texte ou au bord de la page en points.

 **Remarks:** 

N'a aucun effet et sera automatiquement réinitialisé à zéro pour les bordures des cellules de tableau.

 **Examples:** 

Montre comment créer une bordure à bande bleue large en haut de la première page.

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
double - Distance de la bordure par rapport au texte ou au bord de la page en points.
### getLineStyle() {#getLineStyle}
```
public int getLineStyle()
```


Obtient le style de la bordure.

 **Remarks:** 

Si vous définissez le style de ligne sur none, alors la largeur de ligne est automatiquement changée à zéro.

 **Examples:** 

Montre comment insérer une chaîne entourée d'une bordure dans un document.

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
int - Le style de la bordure. La valeur renvoyée est l'une des constantes [LineStyle](../../com.aspose.words/linestyle/).
### getLineWidth() {#getLineWidth}
```
public double getLineWidth()
```


Obtient la largeur de la bordure en points.

 **Remarks:** 

Si vous définissez la largeur de ligne supérieure à zéro lorsque le style de ligne est none, le style de ligne est automatiquement changé en ligne simple.

 **Examples:** 

Montre comment insérer une chaîne entourée d'une bordure dans un document.

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
double - La largeur de la bordure en points.
### getShadow() {#getShadow}
```
public boolean getShadow()
```


Obtient une valeur indiquant si la bordure possède une ombre.

 **Remarks:** 

Dans Microsoft Word, pour qu'une bordure ait une ombre, les bordures sur les quatre côtés (gauche, haut, droite et bas) doivent être du même type, même largeur, même couleur et toutes doivent avoir la propriété Shadow définie sur  true .

 **Examples:** 

Montre comment créer une bordure de page verte ondulée avec une ombre.

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
boolean - Une valeur indiquant si la bordure a une ombre.
### getThemeColor() {#getThemeColor}
```
public int getThemeColor()
```


Obtient la couleur du thème dans le schéma de couleurs appliqué qui est associé à cet objet Border.

 **Examples:** 

Montre comment insérer un paragraphe avec une bordure supérieure.

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
int - La couleur du thème dans le schéma de couleurs appliqué qui est associé à cet objet Border. La valeur retournée est l'une des constantes [ThemeColor](../../com.aspose.words/themecolor/).
### getTintAndShade() {#getTintAndShade}
```
public double getTintAndShade()
```


Obtient une valeur double qui éclaircit ou assombrit une couleur.

**Returns:**
double - Une valeur double qui éclaircit ou assombrit une couleur.
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


Renvoie  true  si le [getLineStyle()](../../com.aspose.words/border/\#getLineStyle) / [setLineStyle(int)](../../com.aspose.words/border/\#setLineStyle-int) n'est pas [LineStyle.NONE](../../com.aspose.words/linestyle/\#NONE).

 **Examples:** 

Montre comment supprimer les bordures d'un paragraphe.

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
boolean -  true  si le [getLineStyle()](../../com.aspose.words/border/\#getLineStyle) / [setLineStyle(int)](../../com.aspose.words/border/\#setLineStyle-int) n'est pas [LineStyle.NONE](../../com.aspose.words/linestyle/\#NONE).
### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Définit la couleur de la bordure.

 **Examples:** 

Montre comment insérer une chaîne entourée d'une bordure dans un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.awt.Color | La couleur de la bordure. |

### setDistanceFromText(double value) {#setDistanceFromText-double}
```
public void setDistanceFromText(double value)
```


Définit la distance de la bordure par rapport au texte ou au bord de la page en points.

 **Remarks:** 

N'a aucun effet et sera automatiquement réinitialisé à zéro pour les bordures des cellules de tableau.

 **Examples:** 

Montre comment créer une bordure à bande bleue large en haut de la première page.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | Distance de la bordure par rapport au texte ou au bord de la page en points. |

### setLineStyle(int value) {#setLineStyle-int}
```
public void setLineStyle(int value)
```


Définit le style de la bordure.

 **Remarks:** 

Si vous définissez le style de ligne sur none, alors la largeur de ligne est automatiquement changée à zéro.

 **Examples:** 

Montre comment insérer une chaîne entourée d'une bordure dans un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | Le style de la bordure. La valeur doit être l'une des constantes [LineStyle](../../com.aspose.words/linestyle/). |

### setLineWidth(double value) {#setLineWidth-double}
```
public void setLineWidth(double value)
```


Définit la largeur de la bordure en points.

 **Remarks:** 

Si vous définissez la largeur de ligne supérieure à zéro lorsque le style de ligne est none, le style de ligne est automatiquement changé en ligne simple.

 **Examples:** 

Montre comment insérer une chaîne entourée d'une bordure dans un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | La largeur de la bordure en points. |

### setShadow(boolean value) {#setShadow-boolean}
```
public void setShadow(boolean value)
```


Définit une valeur indiquant si la bordure possède une ombre.

 **Remarks:** 

Dans Microsoft Word, pour qu'une bordure ait une ombre, les bordures sur les quatre côtés (gauche, haut, droite et bas) doivent être du même type, même largeur, même couleur et toutes doivent avoir la propriété Shadow définie sur  true .

 **Examples:** 

Montre comment créer une bordure de page verte ondulée avec une ombre.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Une valeur indiquant si la bordure a une ombre. |

### setThemeColor(int value) {#setThemeColor-int}
```
public void setThemeColor(int value)
```


Définit la couleur du thème dans le schéma de couleurs appliqué qui est associé à cet objet Border.

 **Examples:** 

Montre comment insérer un paragraphe avec une bordure supérieure.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La couleur du thème dans le schéma de couleurs appliqué qui est associé à cet objet Border. La valeur doit être l'une des constantes [ThemeColor](../../com.aspose.words/themecolor/). |

### setTintAndShade(double value) {#setTintAndShade-double}
```
public void setTintAndShade(double value)
```


Définit une valeur double qui éclaircit ou assombrit une couleur.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | Une valeur double qui éclaircit ou assombrit une couleur. |

