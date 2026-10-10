---
title: "Border"
linktitle: "Border"
second_title: "Aspose.Words per Java"
description: "Rappresenta un bordo di un oggetto in Java."
type: docs
weight: 46
url: /it/java/com.aspose.words/border/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.InternableComplexAttr](../../com.aspose.words/internablecomplexattr/)

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class Border extends InternableComplexAttr implements Cloneable
```

Rappresenta un bordo di un oggetto.

Per saperne di più, visita l'articolo di documentazione [ Programmare con i Documenti ][Programming with Documents].

 **Remarks:** 

I bordi possono essere applicati a vari elementi del documento, inclusi paragrafi, sequenze di testo all'interno di un paragrafo o celle di una tabella.

 **Examples:** 

Mostra come inserire una stringa circondata da un bordo in un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

Mostra come inserire un paragrafo con un bordo superiore.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Ripristina le proprietà del bordo ai valori predefiniti. |
| [equals(Border rhs)](#equals-com.aspose.words.Border) | Determina se il bordo specificato è uguale in valore al bordo corrente. |
| [equals(Object obj)](#equals-java.lang.Object) | Determina se l'oggetto specificato è uguale in valore all'oggetto corrente. |
| [getColor()](#getColor) | Ottiene il colore del bordo. |
| [getDistanceFromText()](#getDistanceFromText) | Ottiene la distanza del bordo dal testo o dal margine della pagina in punti. |
| [getLineStyle()](#getLineStyle) | Ottiene lo stile del bordo. |
| [getLineWidth()](#getLineWidth) | Ottiene la larghezza del bordo in punti. |
| [getShadow()](#getShadow) | Ottiene un valore che indica se il bordo ha un'ombra. |
| [getThemeColor()](#getThemeColor) | Ottiene il colore del tema nello schema colori applicato associato a questo oggetto Border. |
| [getTintAndShade()](#getTintAndShade) | Ottiene un valore double che schiarisce o scurisce un colore. |
| [hashCode()](#hashCode) |  |
| [isInheritedComplexAttr()](#isInheritedComplexAttr) |  |
| [isVisible()](#isVisible) | Restituisce  true  se il [getLineStyle()](../../com.aspose.words/border/\#getLineStyle) / [setLineStyle(int)](../../com.aspose.words/border/\#setLineStyle-int) non è [LineStyle.NONE](../../com.aspose.words/linestyle/\#NONE). |
| [setColor(Color value)](#setColor-java.awt.Color) | Imposta il colore del bordo. |
| [setDistanceFromText(double value)](#setDistanceFromText-double) | Imposta la distanza del bordo dal testo o dal margine della pagina in punti. |
| [setLineStyle(int value)](#setLineStyle-int) | Imposta lo stile del bordo. |
| [setLineWidth(double value)](#setLineWidth-double) | Imposta la larghezza del bordo in punti. |
| [setShadow(boolean value)](#setShadow-boolean) | Imposta un valore che indica se il bordo ha un'ombra. |
| [setThemeColor(int value)](#setThemeColor-int) | Imposta il colore del tema nello schema colori applicato associato a questo oggetto Border. |
| [setTintAndShade(double value)](#setTintAndShade-double) | Imposta un valore double che schiarisce o scurisce un colore. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Ripristina le proprietà del bordo ai valori predefiniti.

 **Remarks:** 

Quando le proprietà del bordo vengono ripristinate ai valori predefiniti, il bordo è invisibile.

 **Examples:** 

Mostra come rimuovere i bordi da un paragrafo.

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


Determina se il bordo specificato è uguale in valore al bordo corrente.

 **Examples:** 

Mostra come le collezioni di bordi possono condividere elementi.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| rhs | [Border](../../com.aspose.words/border/) |  |

**Returns:**
boolean
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Determina se l'oggetto specificato è uguale in valore all'oggetto corrente.

 **Examples:** 

Mostra come le collezioni di bordi possono condividere elementi.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getColor() {#getColor}
```
public Color getColor()
```


Ottiene il colore del bordo.

 **Examples:** 

Mostra come inserire una stringa circondata da un bordo in un documento.

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
java.awt.Color - Il colore del bordo.
### getDistanceFromText() {#getDistanceFromText}
```
public double getDistanceFromText()
```


Ottiene la distanza del bordo dal testo o dal margine della pagina in punti.

 **Remarks:** 

Non ha effetto e verrà automaticamente reimpostato a zero per i bordi delle celle della tabella.

 **Examples:** 

Mostra come creare un bordo a banda blu larga nella parte superiore della prima pagina.

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
double - Distanza del bordo dal testo o dal margine della pagina in punti.
### getLineStyle() {#getLineStyle}
```
public int getLineStyle()
```


Ottiene lo stile del bordo.

 **Remarks:** 

Se imposti lo stile della linea su none, la larghezza della linea viene automaticamente impostata a zero.

 **Examples:** 

Mostra come inserire una stringa circondata da un bordo in un documento.

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
int - Lo stile del bordo. Il valore restituito è una delle costanti [LineStyle](../../com.aspose.words/linestyle/).
### getLineWidth() {#getLineWidth}
```
public double getLineWidth()
```


Ottiene la larghezza del bordo in punti.

 **Remarks:** 

Se imposti la larghezza della linea maggiore di zero quando lo stile della linea è none, lo stile della linea viene automaticamente cambiato in linea singola.

 **Examples:** 

Mostra come inserire una stringa circondata da un bordo in un documento.

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
double - La larghezza del bordo in punti.
### getShadow() {#getShadow}
```
public boolean getShadow()
```


Ottiene un valore che indica se il bordo ha un'ombra.

 **Remarks:** 

In Microsoft Word, perché un bordo abbia un'ombra, i bordi su tutti e quattro i lati (sinistro, superiore, destro e inferiore) devono essere dello stesso tipo, larghezza, colore e tutti devono avere la proprietà Shadow impostata su  true .

 **Examples:** 

Mostra come creare un bordo di pagina verde ondulato con un'ombra.

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
boolean - Un valore che indica se il bordo ha un'ombra.
### getThemeColor() {#getThemeColor}
```
public int getThemeColor()
```


Ottiene il colore del tema nello schema colori applicato associato a questo oggetto Border.

 **Examples:** 

Mostra come inserire un paragrafo con un bordo superiore.

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
int - Il colore del tema nello schema colori applicato associato a questo oggetto Border. Il valore restituito è una delle costanti [ThemeColor](../../com.aspose.words/themecolor/).
### getTintAndShade() {#getTintAndShade}
```
public double getTintAndShade()
```


Ottiene un valore double che schiarisce o scurisce un colore.

**Returns:**
double - Un valore double che schiarisce o scurisce un colore.
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


Restituisce  true  se il [getLineStyle()](../../com.aspose.words/border/\#getLineStyle) / [setLineStyle(int)](../../com.aspose.words/border/\#setLineStyle-int) non è [LineStyle.NONE](../../com.aspose.words/linestyle/\#NONE).

 **Examples:** 

Mostra come rimuovere i bordi da un paragrafo.

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
boolean -  true  se il [getLineStyle()](../../com.aspose.words/border/\#getLineStyle) / [setLineStyle(int)](../../com.aspose.words/border/\#setLineStyle-int) non è [LineStyle.NONE](../../com.aspose.words/linestyle/\#NONE).
### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Imposta il colore del bordo.

 **Examples:** 

Mostra come inserire una stringa circondata da un bordo in un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.awt.Color | Il colore del bordo. |

### setDistanceFromText(double value) {#setDistanceFromText-double}
```
public void setDistanceFromText(double value)
```


Imposta la distanza del bordo dal testo o dal margine della pagina in punti.

 **Remarks:** 

Non ha effetto e verrà automaticamente reimpostato a zero per i bordi delle celle della tabella.

 **Examples:** 

Mostra come creare un bordo a banda blu larga nella parte superiore della prima pagina.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | Distanza del bordo dal testo o dal margine della pagina in punti. |

### setLineStyle(int value) {#setLineStyle-int}
```
public void setLineStyle(int value)
```


Imposta lo stile del bordo.

 **Remarks:** 

Se imposti lo stile della linea su none, la larghezza della linea viene automaticamente impostata a zero.

 **Examples:** 

Mostra come inserire una stringa circondata da un bordo in un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Lo stile del bordo. Il valore deve essere una delle costanti [LineStyle](../../com.aspose.words/linestyle/). |

### setLineWidth(double value) {#setLineWidth-double}
```
public void setLineWidth(double value)
```


Imposta la larghezza del bordo in punti.

 **Remarks:** 

Se imposti la larghezza della linea maggiore di zero quando lo stile della linea è none, lo stile della linea viene automaticamente cambiato in linea singola.

 **Examples:** 

Mostra come inserire una stringa circondata da un bordo in un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | La larghezza del bordo in punti. |

### setShadow(boolean value) {#setShadow-boolean}
```
public void setShadow(boolean value)
```


Imposta un valore che indica se il bordo ha un'ombra.

 **Remarks:** 

In Microsoft Word, perché un bordo abbia un'ombra, i bordi su tutti e quattro i lati (sinistro, superiore, destro e inferiore) devono essere dello stesso tipo, larghezza, colore e tutti devono avere la proprietà Shadow impostata su  true .

 **Examples:** 

Mostra come creare un bordo di pagina verde ondulato con un'ombra.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Un valore che indica se il bordo ha un'ombra. |

### setThemeColor(int value) {#setThemeColor-int}
```
public void setThemeColor(int value)
```


Imposta il colore del tema nello schema colori applicato associato a questo oggetto Border.

 **Examples:** 

Mostra come inserire un paragrafo con un bordo superiore.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il colore del tema nello schema colori applicato associato a questo oggetto Border. Il valore deve essere una delle costanti [ThemeColor](../../com.aspose.words/themecolor/). |

### setTintAndShade(double value) {#setTintAndShade-double}
```
public void setTintAndShade(double value)
```


Imposta un valore double che schiarisce o scurisce un colore.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | Un valore double che schiarisce o scurisce un colore. |

