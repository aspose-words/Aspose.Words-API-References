---
title: "Border"
linktitle: "Border"
second_title: "Aspose.Words für Java"
description: "Stellt einen Rand eines Objekts in Java dar."
type: docs
weight: 46
url: /de/java/com.aspose.words/border/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.InternableComplexAttr](../../com.aspose.words/internablecomplexattr/)

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class Border extends InternableComplexAttr implements Cloneable
```

Stellt einen Rahmen eines Objekts dar.

Weitere Informationen finden Sie im Dokumentationsartikel [ Programming with Documents ][Programming with Documents].

 **Remarks:** 

Ränder können auf verschiedene Dokumentelemente angewendet werden, einschließlich Absatz, Textlauf innerhalb eines Absatzes oder einer Tabellenzelle.

 **Examples:** 

Zeigt, wie man eine von einem Rand umgebene Zeichenkette in ein Dokument einfügt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

Zeigt, wie ein Absatz mit einem oberen Rahmen eingefügt wird.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Setzt die Rand-Eigenschaften auf Standardwerte zurück. |
| [equals(Border rhs)](#equals-com.aspose.words.Border) | Bestimmt, ob der angegebene Rand im Wert dem aktuellen Rand entspricht. |
| [equals(Object obj)](#equals-java.lang.Object) | Bestimmt, ob das angegebene Objekt im Wert dem aktuellen Objekt entspricht. |
| [getColor()](#getColor) | Liefert die Rahmenfarbe. |
| [getDistanceFromText()](#getDistanceFromText) | Ermittelt den Abstand des Randes vom Text oder vom Seitenrand in Punkten. |
| [getLineStyle()](#getLineStyle) | Liefert den Rahmenstil. |
| [getLineWidth()](#getLineWidth) | Liefert die Rahmenbreite in Punkten. |
| [getShadow()](#getShadow) | Liefert einen Wert, der angibt, ob der Rahmen einen Schatten hat. |
| [getThemeColor()](#getThemeColor) | Ermittelt die Themenfarbe im angewendeten Farbschema, die mit diesem Border-Objekt verknüpft ist. |
| [getTintAndShade()](#getTintAndShade) | Gibt einen double-Wert zurück, der eine Farbe aufhellt oder abdunkelt. |
| [hashCode()](#hashCode) |  |
| [isInheritedComplexAttr()](#isInheritedComplexAttr) |  |
| [isVisible()](#isVisible) | Gibt  true  zurück, wenn die [getLineStyle()](../../com.aspose.words/border/\#getLineStyle) / [setLineStyle(int)](../../com.aspose.words/border/\#setLineStyle-int) nicht [LineStyle.NONE](../../com.aspose.words/linestyle/\#NONE) ist. |
| [setColor(Color value)](#setColor-java.awt.Color) | Setzt die Rahmenfarbe. |
| [setDistanceFromText(double value)](#setDistanceFromText-double) | Legt den Abstand des Rahmens vom Text oder vom Seitenrand in Punkten fest. |
| [setLineStyle(int value)](#setLineStyle-int) | Setzt den Rahmenstil. |
| [setLineWidth(double value)](#setLineWidth-double) | Setzt die Rahmenbreite in Punkten. |
| [setShadow(boolean value)](#setShadow-boolean) | Setzt einen Wert, der angibt, ob der Rahmen einen Schatten hat. |
| [setThemeColor(int value)](#setThemeColor-int) | Legt die Themenfarbe im angewendeten Farbschema fest, die mit diesem Border-Objekt verknüpft ist. |
| [setTintAndShade(double value)](#setTintAndShade-double) | Legt einen double-Wert fest, der eine Farbe aufhellt oder abdunkelt. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Setzt die Rand-Eigenschaften auf Standardwerte zurück.

 **Remarks:** 

Wenn die Rahmen-Eigenschaften auf Standardwerte zurückgesetzt werden, ist der Rahmen unsichtbar.

 **Examples:** 

Zeigt, wie man Rahmen aus einem Absatz entfernt.

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


Bestimmt, ob der angegebene Rand im Wert dem aktuellen Rand entspricht.

 **Examples:** 

Zeigt, wie Rahmenkollektionen Elemente teilen können.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| rhs | [Border](../../com.aspose.words/border/) |  |

**Returns:**
boolean
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Bestimmt, ob das angegebene Objekt im Wert dem aktuellen Objekt entspricht.

 **Examples:** 

Zeigt, wie Rahmenkollektionen Elemente teilen können.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getColor() {#getColor}
```
public Color getColor()
```


Liefert die Rahmenfarbe.

 **Examples:** 

Zeigt, wie man eine von einem Rand umgebene Zeichenkette in ein Dokument einfügt.

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
java.awt.Color - Die Randfarbe.
### getDistanceFromText() {#getDistanceFromText}
```
public double getDistanceFromText()
```


Ermittelt den Abstand des Randes vom Text oder vom Seitenrand in Punkten.

 **Remarks:** 

Hat keine Wirkung und wird für Tabellenzellenränder automatisch auf Null zurückgesetzt.

 **Examples:** 

Zeigt, wie man einen breiten blauen Bandrahmen oben auf der ersten Seite erstellt.

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
double - Abstand des Rahmens vom Text oder vom Seitenrand in Punkten.
### getLineStyle() {#getLineStyle}
```
public int getLineStyle()
```


Liefert den Rahmenstil.

 **Remarks:** 

Wenn Sie den Linienstil auf none setzen, wird die Linienbreite automatisch auf null gesetzt.

 **Examples:** 

Zeigt, wie man eine von einem Rand umgebene Zeichenkette in ein Dokument einfügt.

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
int - Der Randstil. Der zurückgegebene Wert ist einer der Konstanten von [LineStyle](../../com.aspose.words/linestyle/).
### getLineWidth() {#getLineWidth}
```
public double getLineWidth()
```


Liefert die Rahmenbreite in Punkten.

 **Remarks:** 

Wenn Sie die Linienbreite größer als null setzen, während der Linienstil none ist, wird der Linienstil automatisch auf einfache Linie geändert.

 **Examples:** 

Zeigt, wie man eine von einem Rand umgebene Zeichenkette in ein Dokument einfügt.

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
double - Die Randbreite in Punkten.
### getShadow() {#getShadow}
```
public boolean getShadow()
```


Liefert einen Wert, der angibt, ob der Rahmen einen Schatten hat.

 **Remarks:** 

In Microsoft Word muss ein Rahmen einen Schatten haben, wenn die Rahmen auf allen vier Seiten (links, oben, rechts und unten) vom selben Typ, derselben Breite, derselben Farbe sind und alle die Shadow property auf  true  gesetzt haben.

 **Examples:** 

Zeigt, wie man einen grünen welligen Seitenrand mit Schatten erstellt.

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
boolean - Ein Wert, der angibt, ob der Rand einen Schatten hat.
### getThemeColor() {#getThemeColor}
```
public int getThemeColor()
```


Ermittelt die Themenfarbe im angewendeten Farbschema, die mit diesem Border-Objekt verknüpft ist.

 **Examples:** 

Zeigt, wie ein Absatz mit einem oberen Rahmen eingefügt wird.

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
int - Die Themenfarbe im angewendeten Farbschema, die mit diesem Border-Objekt verknüpft ist. Der zurückgegebene Wert ist einer der [ThemeColor](../../com.aspose.words/themecolor/) Konstanten.
### getTintAndShade() {#getTintAndShade}
```
public double getTintAndShade()
```


Gibt einen double-Wert zurück, der eine Farbe aufhellt oder abdunkelt.

**Returns:**
double - Ein double-Wert, der eine Farbe aufhellt oder abdunkelt.
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


Gibt  true  zurück, wenn die [getLineStyle()](../../com.aspose.words/border/\#getLineStyle) / [setLineStyle(int)](../../com.aspose.words/border/\#setLineStyle-int) nicht [LineStyle.NONE](../../com.aspose.words/linestyle/\#NONE) ist.

 **Examples:** 

Zeigt, wie man Rahmen aus einem Absatz entfernt.

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
boolean -  true  wenn die [getLineStyle()](../../com.aspose.words/border/\#getLineStyle) / [setLineStyle(int)](../../com.aspose.words/border/\#setLineStyle-int) nicht [LineStyle.NONE](../../com.aspose.words/linestyle/\#NONE) ist.
### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Setzt die Rahmenfarbe.

 **Examples:** 

Zeigt, wie man eine von einem Rand umgebene Zeichenkette in ein Dokument einfügt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.awt.Color | Die Randfarbe. |

### setDistanceFromText(double value) {#setDistanceFromText-double}
```
public void setDistanceFromText(double value)
```


Legt den Abstand des Rahmens vom Text oder vom Seitenrand in Punkten fest.

 **Remarks:** 

Hat keine Wirkung und wird für Tabellenzellenränder automatisch auf Null zurückgesetzt.

 **Examples:** 

Zeigt, wie man einen breiten blauen Bandrahmen oben auf der ersten Seite erstellt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Abstand des Rahmens vom Text oder vom Seitenrand in Punkten. |

### setLineStyle(int value) {#setLineStyle-int}
```
public void setLineStyle(int value)
```


Setzt den Rahmenstil.

 **Remarks:** 

Wenn Sie den Linienstil auf none setzen, wird die Linienbreite automatisch auf null gesetzt.

 **Examples:** 

Zeigt, wie man eine von einem Rand umgebene Zeichenkette in ein Dokument einfügt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der Randstil. Der Wert muss einer der Konstanten von [LineStyle](../../com.aspose.words/linestyle/) sein. |

### setLineWidth(double value) {#setLineWidth-double}
```
public void setLineWidth(double value)
```


Setzt die Rahmenbreite in Punkten.

 **Remarks:** 

Wenn Sie die Linienbreite größer als null setzen, während der Linienstil none ist, wird der Linienstil automatisch auf einfache Linie geändert.

 **Examples:** 

Zeigt, wie man eine von einem Rand umgebene Zeichenkette in ein Dokument einfügt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Die Randbreite in Punkten. |

### setShadow(boolean value) {#setShadow-boolean}
```
public void setShadow(boolean value)
```


Setzt einen Wert, der angibt, ob der Rahmen einen Schatten hat.

 **Remarks:** 

In Microsoft Word muss ein Rahmen einen Schatten haben, wenn die Rahmen auf allen vier Seiten (links, oben, rechts und unten) vom selben Typ, derselben Breite, derselben Farbe sind und alle die Shadow property auf  true  gesetzt haben.

 **Examples:** 

Zeigt, wie man einen grünen welligen Seitenrand mit Schatten erstellt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein Wert, der angibt, ob der Rand einen Schatten hat. |

### setThemeColor(int value) {#setThemeColor-int}
```
public void setThemeColor(int value)
```


Legt die Themenfarbe im angewendeten Farbschema fest, die mit diesem Border-Objekt verknüpft ist.

 **Examples:** 

Zeigt, wie ein Absatz mit einem oberen Rahmen eingefügt wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Die Themenfarbe im angewendeten Farbschema, die mit diesem Border-Objekt verknüpft ist. Der Wert muss einer der [ThemeColor](../../com.aspose.words/themecolor/) Konstanten sein. |

### setTintAndShade(double value) {#setTintAndShade-double}
```
public void setTintAndShade(double value)
```


Legt einen double-Wert fest, der eine Farbe aufhellt oder abdunkelt.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Ein double-Wert, der eine Farbe aufhellt oder abdunkelt. |

