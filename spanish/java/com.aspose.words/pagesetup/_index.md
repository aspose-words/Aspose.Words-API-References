---
title: "PageSetup"
linktitle: "PageSetup"
second_title: "Aspose.Words para Java"
description: "Representa las propiedades de configuración de página de una sección en Java."
type: docs
weight: 519
url: /es/java/com.aspose.words/pagesetup/
---

**Inheritance:**
java.lang.Object
```
public class PageSetup
```

Representa las propiedades de configuración de página de una sección.

Para obtener más información, visite el artículo de documentación [ Working with Sections ][Working with Sections].

 **Remarks:** 

[PageSetup](../../com.aspose.words/pagesetup/) object contains all the page setup attributes of a section (left margin, bottom margin, paper size, and so on) as properties.

 **Examples:** 

Muestra cómo aplicar y revertir la configuración de página a secciones en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```


[Working with Sections]: https://docs.aspose.com/words/java/working-with-sections/
## Métodos

| Método | Descripción |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Restablece la configuración de página al tamaño de papel, márgenes y orientación predeterminados. |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int) |  |
| [getBidi()](#getBidi) | Especifica que esta sección contiene texto bidireccional (scripts complejos). |
| [getBorderAlwaysInFront()](#getBorderAlwaysInFront) | Especifica dónde se posiciona el borde de la página en relación con los textos y objetos intersectados. |
| [getBorderAppliesTo()](#getBorderAppliesTo) | Especifica en qué páginas se imprime el borde de la página. |
| [getBorderDistanceFrom()](#getBorderDistanceFrom) | Obtiene un valor que indica si el borde de página especificado se mide desde el borde de la página o desde el texto que lo rodea. |
| [getBorderSurroundsFooter()](#getBorderSurroundsFooter) | Especifica si el borde de página incluye o excluye el pie de página. |
| [getBorderSurroundsHeader()](#getBorderSurroundsHeader) | Especifica si el borde de página incluye o excluye el encabezado. |
| [getBorders()](#getBorders) | Obtiene una colección de los bordes de página. |
| [getBottomMargin()](#getBottomMargin) | Obtiene la distancia (en puntos) entre el borde inferior de la página y el límite inferior del texto del cuerpo. |
| [getChapterPageSeparator()](#getChapterPageSeparator) | Obtiene el carácter separador que aparece entre el número del capítulo y el número de página. |
| [getCharactersPerLine()](#getCharactersPerLine) | Obtiene el número de caracteres por línea en la cuadrícula del documento. |
| [getDifferentFirstPageHeaderFooter()](#getDifferentFirstPageHeaderFooter) | Verdadero si se utiliza un encabezado o pie de página diferente en la primera página. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int) |  |
| [getEndnoteOptions()](#getEndnoteOptions) | Proporciona opciones que controlan la numeración y la posición de las notas finales en esta sección. |
| [getFirstPageTray()](#getFirstPageTray) | Obtiene la bandeja de papel (cajón) que se usará para la primera página de una sección. |
| [getFooterDistance()](#getFooterDistance) | Obtiene la distancia (en puntos) entre el pie de página y la parte inferior de la página. |
| [getFootnoteOptions()](#getFootnoteOptions) | Proporciona opciones que controlan la numeración y la posición de las notas al pie en esta sección. |
| [getGutter()](#getGutter) | Obtiene la cantidad de espacio adicional añadido al margen para la encuadernación del documento. |
| [getHeaderDistance()](#getHeaderDistance) | Obtiene la distancia (en puntos) entre el encabezado y la parte superior de la página. |
| [getHeadingLevelForChapter()](#getHeadingLevelForChapter) | Obtiene el estilo de nivel de encabezado que se aplica a los títulos de los capítulos en el documento. |
| [getLayoutMode()](#getLayoutMode) | Obtiene el modo de diseño de esta sección. |
| [getLeftMargin()](#getLeftMargin) | Obtiene la distancia (en puntos) entre el borde izquierdo de la página y el límite izquierdo del texto del cuerpo. |
| [getLineNumberCountBy()](#getLineNumberCountBy) | Obtiene el incremento numérico para los números de línea. |
| [getLineNumberDistanceFromText()](#getLineNumberDistanceFromText) | Obtiene la distancia entre el borde derecho de los números de línea y el borde izquierdo del documento. |
| [getLineNumberRestartMode()](#getLineNumberRestartMode) | Obtiene la forma en que se ejecuta la numeración de líneas, es decir, si comienza de nuevo al inicio de una página o sección nueva o se ejecuta de forma continua. |
| [getLineStartingNumber()](#getLineStartingNumber) | Obtiene el número de línea inicial. |
| [getLinesPerPage()](#getLinesPerPage) | Obtiene el número de líneas por página en la cuadrícula del documento. |
| [getMargins()](#getMargins) | Obtiene los [Márgenes](../../com.aspose.words/margins/) predefinidos de la página. |
| [getMultiplePages()](#getMultiplePages) | Para documentos de varias páginas, obtiene o establece cómo se imprime o renderiza un documento para que pueda encuadernarse como folleto. |
| [getOddAndEvenPagesHeaderFooter()](#getOddAndEvenPagesHeaderFooter) | True si el documento tiene encabezados y pies de página diferentes para páginas impares y pares. |
| [getOrientation()](#getOrientation) | Obtiene la orientación de la página. |
| [getOtherPagesTray()](#getOtherPagesTray) | Obtiene la bandeja de papel (cajón) que se usará para todas las páginas excepto la primera de una sección. |
| [getPageHeight()](#getPageHeight) | Obtiene la altura de la página en puntos. |
| [getPageNumberStyle()](#getPageNumberStyle) | Obtiene el formato del número de página. |
| [getPageStartingNumber()](#getPageStartingNumber) | Obtiene el número de página inicial de la sección. |
| [getPageWidth()](#getPageWidth) | Obtiene el ancho de la página en puntos. |
| [getPaperSize()](#getPaperSize) | Obtiene el tamaño del papel. |
| [getRestartPageNumbering()](#getRestartPageNumbering) | True si la numeración de páginas se reinicia al comienzo de la sección. |
| [getRightMargin()](#getRightMargin) | Obtiene la distancia (en puntos) entre el borde derecho de la página y el límite derecho del texto del cuerpo. |
| [getRtlGutter()](#getRtlGutter) | Obtiene si Microsoft Word usa canaletas para la sección según un idioma de derecha a izquierda o de izquierda a derecha. |
| [getSectionStart()](#getSectionStart) | Obtiene el tipo de salto de sección para el objeto especificado. |
| [getSheetsPerBooklet()](#getSheetsPerBooklet) | Obtiene el número de páginas que se incluirán en cada folleto. |
| [getSuppressEndnotes()](#getSuppressEndnotes) | True si las notas finales se imprimen al final de la siguiente sección que no suprime notas finales. |
| [getTextColumns()](#getTextColumns) | Devuelve una colección que representa el conjunto de columnas de texto. |
| [getTextOrientation()](#getTextOrientation) | Permite especificar [getTextOrientation()](../../com.aspose.words/pagesetup/#getTextOrientation) / [setTextOrientation(int)](../../com.aspose.words/pagesetup/#setTextOrientation-int) para toda la página. |
| [getTopMargin()](#getTopMargin) | Obtiene la distancia (en puntos) entre el borde superior de la página y el límite superior del texto del cuerpo. |
| [getVerticalAlignment()](#getVerticalAlignment) | Obtiene la alineación vertical del texto en cada página de un documento o sección. |
| [setBidi(boolean value)](#setBidi-boolean) | Especifica que esta sección contiene texto bidireccional (scripts complejos). |
| [setBorderAlwaysInFront(boolean value)](#setBorderAlwaysInFront-boolean) | Especifica dónde se posiciona el borde de la página en relación con los textos y objetos intersectados. |
| [setBorderAppliesTo(int value)](#setBorderAppliesTo-int) | Especifica en qué páginas se imprime el borde de la página. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object) |  |
| [setBorderDistanceFrom(int value)](#setBorderDistanceFrom-int) | Establece un valor que indica si el borde de página especificado se mide desde el borde de la página o desde el texto que lo rodea. |
| [setBorderSurroundsFooter(boolean value)](#setBorderSurroundsFooter-boolean) | Especifica si el borde de página incluye o excluye el pie de página. |
| [setBorderSurroundsHeader(boolean value)](#setBorderSurroundsHeader-boolean) | Especifica si el borde de página incluye o excluye el encabezado. |
| [setBottomMargin(double value)](#setBottomMargin-double) | Establece la distancia (en puntos) entre el borde inferior de la página y el límite inferior del texto del cuerpo. |
| [setChapterPageSeparator(int value)](#setChapterPageSeparator-int) | Establece el carácter separador que aparece entre el número del capítulo y el número de página. |
| [setCharactersPerLine(int value)](#setCharactersPerLine-int) | Establece el número de caracteres por línea en la cuadrícula del documento. |
| [setDifferentFirstPageHeaderFooter(boolean value)](#setDifferentFirstPageHeaderFooter-boolean) | Verdadero si se utiliza un encabezado o pie de página diferente en la primera página. |
| [setFirstPageTray(int value)](#setFirstPageTray-int) | Establece la bandeja de papel (cajón) que se usará para la primera página de una sección. |
| [setFooterDistance(double value)](#setFooterDistance-double) | Establece la distancia (en puntos) entre el pie de página y la parte inferior de la página. |
| [setGutter(double value)](#setGutter-double) | Establece la cantidad de espacio adicional añadido al margen para la encuadernación del documento. |
| [setHeaderDistance(double value)](#setHeaderDistance-double) | Establece la distancia (en puntos) entre el encabezado y la parte superior de la página. |
| [setHeadingLevelForChapter(int value)](#setHeadingLevelForChapter-int) | Establece el estilo de nivel de encabezado que se aplica a los títulos de capítulo en el documento. |
| [setLayoutMode(int value)](#setLayoutMode-int) | Establece el modo de diseño de esta sección. |
| [setLeftMargin(double value)](#setLeftMargin-double) | Establece la distancia (en puntos) entre el borde izquierdo de la página y el límite izquierdo del texto del cuerpo. |
| [setLineNumberCountBy(int value)](#setLineNumberCountBy-int) | Establece el incremento numérico para los números de línea. |
| [setLineNumberDistanceFromText(double value)](#setLineNumberDistanceFromText-double) | Establece la distancia entre el borde derecho de los números de línea y el borde izquierdo del documento. |
| [setLineNumberRestartMode(int value)](#setLineNumberRestartMode-int) | Establece la forma en que se numeran las líneas, es decir, si se reinician al comienzo de una nueva página o sección o continúan de forma continua. |
| [setLineStartingNumber(int value)](#setLineStartingNumber-int) | Establece el número de línea inicial. |
| [setLinesPerPage(int value)](#setLinesPerPage-int) | Establece el número de líneas por página en la cuadrícula del documento. |
| [setMargins(int value)](#setMargins-int) | Establece los [Márgenes](../../com.aspose.words/margins/) predefinidos de la página. |
| [setMultiplePages(int value)](#setMultiplePages-int) | Para documentos de varias páginas, obtiene o establece cómo se imprime o renderiza un documento para que pueda encuadernarse como folleto. |
| [setOddAndEvenPagesHeaderFooter(boolean value)](#setOddAndEvenPagesHeaderFooter-boolean) | True si el documento tiene encabezados y pies de página diferentes para páginas impares y pares. |
| [setOrientation(int value)](#setOrientation-int) | Establece la orientación de la página. |
| [setOtherPagesTray(int value)](#setOtherPagesTray-int) | Establece la bandeja de papel (cajón) que se usará para todas las páginas excepto la primera de una sección. |
| [setPageHeight(double value)](#setPageHeight-double) | Establece la altura de la página en puntos. |
| [setPageNumberStyle(int value)](#setPageNumberStyle-int) | Establece el formato del número de página. |
| [setPageStartingNumber(int value)](#setPageStartingNumber-int) | Establece el número de página inicial de la sección. |
| [setPageWidth(double value)](#setPageWidth-double) | Establece el ancho de la página en puntos. |
| [setPaperSize(int value)](#setPaperSize-int) | Establece el tamaño del papel. |
| [setRestartPageNumbering(boolean value)](#setRestartPageNumbering-boolean) | True si la numeración de páginas se reinicia al comienzo de la sección. |
| [setRightMargin(double value)](#setRightMargin-double) | Establece la distancia (en puntos) entre el borde derecho de la página y el límite derecho del texto del cuerpo. |
| [setRtlGutter(boolean value)](#setRtlGutter-boolean) | Establece si Microsoft Word usa canaletas para la sección según un idioma de derecha a izquierda o de izquierda a derecha. |
| [setSectionStart(int value)](#setSectionStart-int) | Establece el tipo de salto de sección para el objeto especificado. |
| [setSheetsPerBooklet(int value)](#setSheetsPerBooklet-int) | Establece el número de páginas que se incluirán en cada folleto. |
| [setSuppressEndnotes(boolean value)](#setSuppressEndnotes-boolean) | True si las notas finales se imprimen al final de la siguiente sección que no suprime notas finales. |
| [setTextOrientation(int value)](#setTextOrientation-int) | Permite especificar [getTextOrientation()](../../com.aspose.words/pagesetup/#getTextOrientation) / [setTextOrientation(int)](../../com.aspose.words/pagesetup/#setTextOrientation-int) para toda la página. |
| [setTopMargin(double value)](#setTopMargin-double) | Establece la distancia (en puntos) entre el borde superior de la página y el límite superior del texto del cuerpo. |
| [setVerticalAlignment(int value)](#setVerticalAlignment-int) | Establece la alineación vertical del texto en cada página de un documento o sección. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Restablece la configuración de página al tamaño de papel, márgenes y orientación predeterminados.

 **Examples:** 

Muestra cómo aplicar y revertir la configuración de página a secciones en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
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
### getBidi() {#getBidi}
```
public boolean getBidi()
```


Especifica que esta sección contiene texto bidireccional (scripts complejos).

 **Remarks:** 

Cuando  true , las columnas en esta sección se disponen de derecha a izquierda.

 **Examples:** 

Muestra cómo establecer el orden de las columnas de texto en una sección.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.getTextColumns().setCount(3);

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.write("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.write("Column 2.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.write("Column 3.");

 // Set the "Bidi" property to "true" to arrange the columns starting from the page's right side.
 // The order of the columns will match the direction of the right-to-left text.
 // Set the "Bidi" property to "false" to arrange the columns starting from the page's left side.
 // The order of the columns will match the direction of the left-to-right text.
 pageSetup.setBidi(reverseColumns);

 doc.save(getArtifactsDir() + "PageSetup.Bidi.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getBorderAlwaysInFront() {#getBorderAlwaysInFront}
```
public boolean getBorderAlwaysInFront()
```


Especifica dónde se posiciona el borde de la página en relación con los textos y objetos intersectados.

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
boolean - El valor  boolean  correspondiente.
### getBorderAppliesTo() {#getBorderAppliesTo}
```
public int getBorderAppliesTo()
```


Especifica en qué páginas se imprime el borde de la página.

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
int - El valor int correspondiente. El valor devuelto es uno de los constantes [PageBorderAppliesTo](../../com.aspose.words/pageborderappliesto/).
### getBorderDistanceFrom() {#getBorderDistanceFrom}
```
public int getBorderDistanceFrom()
```


Obtiene un valor que indica si el borde de página especificado se mide desde el borde de la página o desde el texto que lo rodea.

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
int - Un valor que indica si el borde de página especificado se mide desde el borde de la página o desde el texto que lo rodea. El valor devuelto es uno de los constantes [PageBorderDistanceFrom](../../com.aspose.words/pageborderdistancefrom/).
### getBorderSurroundsFooter() {#getBorderSurroundsFooter}
```
public boolean getBorderSurroundsFooter()
```


Especifica si el borde de página incluye o excluye el pie de página.

 **Remarks:** 

Nota, cambiar esta propiedad afecta a todas las secciones del documento.

 **Examples:** 

Muestra cómo aplicar un borde a la página y al encabezado/pie de página.

```

 Document doc = new Document();

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This is the main body text.");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("This is the header.");
 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.write("This is the footer.");
 builder.moveToDocumentEnd();

 // Insert a blue double-line border.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.getBorders().setLineStyle(LineStyle.DOUBLE);
 pageSetup.getBorders().setColor(Color.BLUE);

 // A section's PageSetup object has "BorderSurroundsHeader" and "BorderSurroundsFooter" flags that determine
 // whether a page border surrounds the main body text, also includes the header or footer, respectively.
 // Set the "BorderSurroundsHeader" flag to "true" to surround the header with our border,
 // and then set the "BorderSurroundsFooter" flag to leave the footer outside of the border.
 pageSetup.setBorderSurroundsHeader(true);
 pageSetup.setBorderSurroundsFooter(false);

 doc.save(getArtifactsDir() + "PageSetup.PageBorder.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getBorderSurroundsHeader() {#getBorderSurroundsHeader}
```
public boolean getBorderSurroundsHeader()
```


Especifica si el borde de página incluye o excluye el encabezado.

 **Remarks:** 

Nota, cambiar esta propiedad afecta a todas las secciones del documento.

 **Examples:** 

Muestra cómo aplicar un borde a la página y al encabezado/pie de página.

```

 Document doc = new Document();

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This is the main body text.");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("This is the header.");
 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.write("This is the footer.");
 builder.moveToDocumentEnd();

 // Insert a blue double-line border.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.getBorders().setLineStyle(LineStyle.DOUBLE);
 pageSetup.getBorders().setColor(Color.BLUE);

 // A section's PageSetup object has "BorderSurroundsHeader" and "BorderSurroundsFooter" flags that determine
 // whether a page border surrounds the main body text, also includes the header or footer, respectively.
 // Set the "BorderSurroundsHeader" flag to "true" to surround the header with our border,
 // and then set the "BorderSurroundsFooter" flag to leave the footer outside of the border.
 pageSetup.setBorderSurroundsHeader(true);
 pageSetup.setBorderSurroundsFooter(false);

 doc.save(getArtifactsDir() + "PageSetup.PageBorder.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getBorders() {#getBorders}
```
public BorderCollection getBorders()
```


Obtiene una colección de los bordes de página.

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
[BorderCollection](../../com.aspose.words/bordercollection/) - A collection of the page borders.
### getBottomMargin() {#getBottomMargin}
```
public double getBottomMargin()
```


Obtiene la distancia (en puntos) entre el borde inferior de la página y el límite inferior del texto del cuerpo.

 **Examples:** 

Muestra cómo ajustar el tamaño del papel, la orientación, los márgenes, junto con otras configuraciones para una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Returns:**
double - La distancia (en puntos) entre el borde inferior de la página y el límite inferior del texto del cuerpo.
### getChapterPageSeparator() {#getChapterPageSeparator}
```
public int getChapterPageSeparator()
```


Obtiene el carácter separador que aparece entre el número del capítulo y el número de página.

 **Remarks:** 

Antes de poder crear números de página que incluyan números de capítulo, los encabezados del documento deben tener aplicado un formato de esquema numerado.

 **Examples:** 

Muestra cómo trabajar con capítulos de página.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();

 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 pageSetup.setChapterPageSeparator(com.aspose.words.ChapterPageSeparator.COLON);
 pageSetup.setHeadingLevelForChapter(1);
 
```

**Returns:**
int - El carácter separador que aparece entre el número de capítulo y el número de página. El valor devuelto es uno de los constantes [ChapterPageSeparator](../../com.aspose.words/chapterpageseparator/).
### getCharactersPerLine() {#getCharactersPerLine}
```
public int getCharactersPerLine()
```


Obtiene el número de caracteres por línea en la cuadrícula del documento.

 **Remarks:** 

El valor mínimo de la propiedad es 1. El valor máximo depende del ancho de la página y del tamaño de fuente del estilo Normal. La distancia mínima entre caracteres es el 90 por ciento del tamaño de fuente. Por ejemplo, el número máximo de caracteres por línea de una página Letter con márgenes de una pulgada es 43.

Por defecto, la propiedad tiene un valor en el que la distancia entre caracteres es igual al tamaño de fuente del estilo Normal.

 **Examples:** 

Muestra cómo especificar un para el número de caracteres que cada línea puede tener.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of characters per line in this section.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.GRID);
 builder.getPageSetup().setCharactersPerLine(10);

 // The number of characters also depends on the size of the font.
 doc.getStyles().get("Normal").getFont().setSize(20.0);

 Assert.assertEquals(8, doc.getFirstSection().getPageSetup().getCharactersPerLine());

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "PageSetup.CharactersPerLine.docx");
 
```

**Returns:**
int - El número de caracteres por línea en la cuadrícula del documento.
### getDifferentFirstPageHeaderFooter() {#getDifferentFirstPageHeaderFooter}
```
public boolean getDifferentFirstPageHeaderFooter()
```


Verdadero si se utiliza un encabezado o pie de página diferente en la primera página.

 **Examples:** 

Muestra cómo crear encabezados y pies de página en un documento usando DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

Muestra cómo rastrear el orden en que una operación de reemplazo de texto recorre los nodos.

```

 public void order(boolean differentFirstPageHeaderFooter) throws Exception {
     Document doc = new Document(getMyDir() + "Header and footer types.docx");

     Section firstPageSection = doc.getFirstSection();

     ReplaceLog logger = new ReplaceLog();
     FindReplaceOptions options = new FindReplaceOptions();
     {
         options.setReplacingCallback(logger);
     }

     // Using a different header/footer for the first page will affect the search order.
     firstPageSection.getPageSetup().setDifferentFirstPageHeaderFooter(differentFirstPageHeaderFooter);
     doc.getRange().replace(Pattern.compile("(header|footer)"), "", options);

     if (differentFirstPageHeaderFooter)
         Assert.assertEquals("First headerFirst footerSecond headerSecond footerThird headerThird footer",
                 logger.Text().replace("\r", ""));
     else
         Assert.assertEquals("Third headerFirst headerThird footerFirst footerSecond headerSecond footer",
                 logger.Text().replace("\r", ""));
 }

 public static Object[][] orderDataProvider() throws Exception {
     return new Object[][]
             {
                     {false},
                     {true},
             };
 }

 /// 
 /// During a find-and-replace operation, records the contents of every node that has text that the operation 'finds',
 /// in the state it is in before the replacement takes place.
 /// This will display the order in which the text replacement operation traverses nodes.
 /// 
 private static class ReplaceLog implements IReplacingCallback {
     public int replacing(ReplacingArgs args) {
         mTextBuilder.append(args.getMatchNode().getText());
         return ReplaceAction.SKIP;
     }

     public String Text() {
         return mTextBuilder.toString();
     }

     private final StringBuilder mTextBuilder = new StringBuilder();
 }
 
```

Muestra cómo habilitar o deshabilitar los encabezados/pies de página principales.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two types of header/footers.
 // 1 -  The "First" header/footer, which appears on the first page of the section.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.writeln("First page header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_FIRST);
 builder.writeln("First page footer.");

 // 2 -  The "Primary" header/footer, which appears on every page in the section.
 // We can override the primary header/footer by a first and an even page header/footer.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Primary header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.writeln("Primary footer.");

 builder.moveToSection(0);
 builder.writeln("Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 3.");

 // Each section has a "PageSetup" object that specifies page appearance-related properties
 // such as orientation, size, and borders.
 // Set the "DifferentFirstPageHeaderFooter" property to "true" to apply the first header/footer to the first page.
 // Set the "DifferentFirstPageHeaderFooter" property to "false"
 // to make the first page display the primary header/footer.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(differentFirstPageHeaderFooter);

 doc.save(getArtifactsDir() + "PageSetup.DifferentFirstPageHeaderFooter.docx");
 
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
### getEndnoteOptions() {#getEndnoteOptions}
```
public EndnoteOptions getEndnoteOptions()
```


Proporciona opciones que controlan la numeración y la posición de las notas finales en esta sección.

 **Examples:** 

Muestra cómo configurar opciones que afectan a las notas al pie/finales en una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Hello world!");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote reference text.");

 // Configure all footnotes in the first section to restart the numbering from 1
 // at each new page and display themselves directly beneath the text on every page.
 FootnoteOptions footnoteOptions = doc.getSections().get(0).getPageSetup().getFootnoteOptions();
 footnoteOptions.setPosition(FootnotePosition.BENEATH_TEXT);
 footnoteOptions.setRestartRule(FootnoteNumberingRule.RESTART_PAGE);
 footnoteOptions.setStartNumber(1);

 builder.write(" Hello again.");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Endnote reference text.");

 // Configure all endnotes in the first section to maintain a continuous count throughout the section,
 // starting from 1. Also, set them all to appear collected at the end of the document.
 EndnoteOptions endnoteOptions = doc.getSections().get(0).getPageSetup().getEndnoteOptions();
 endnoteOptions.setPosition(EndnotePosition.END_OF_DOCUMENT);
 endnoteOptions.setRestartRule(FootnoteNumberingRule.CONTINUOUS);
 endnoteOptions.setStartNumber(1);

 doc.save(getArtifactsDir() + "PageSetup.FootnoteOptions.docx");
 
```

**Returns:**
[EndnoteOptions](../../com.aspose.words/endnoteoptions/) - The corresponding [EndnoteOptions](../../com.aspose.words/endnoteoptions/) value.
### getFirstPageTray() {#getFirstPageTray}
```
public int getFirstPageTray()
```


Obtiene la bandeja de papel (cajón) que se usará para la primera página de una sección. El valor es específico de la implementación (impresora).

 **Examples:** 

Muestra cómo configurar la impresión usando diferentes bandejas de impresora para distintos tamaños de papel.

```

 Document doc = new Document();

 /// Choose the default printer to be used for printing this document.
 PrintService printService = PrintServiceLookup.lookupDefaultPrintService();
 Media[] trays = (Media[]) printService.getSupportedAttributeValues(Media.class, null, null);

 // This is the tray we will use for pages in the "A4" paper size.
 int printerTrayForA4 = trays[0].getValue();
 // This is the tray we will use for pages in the "Letter" paper size.
 int printerTrayForLetter = trays[1].getValue();

 // Modify the PageSettings object of this section to get Microsoft Word to instruct the printer
 // to use one of the trays we identified above, depending on this section's paper size.
 for (Section section : doc.getSections()) {
     if (section.getPageSetup().getPaperSize() == PaperSize.LETTER) {
         section.getPageSetup().setFirstPageTray(printerTrayForLetter);
         section.getPageSetup().setOtherPagesTray(printerTrayForLetter);
     } else if (section.getPageSetup().getPaperSize() == PaperSize.A4) {
         section.getPageSetup().setFirstPageTray(printerTrayForA4);
         section.getPageSetup().setOtherPagesTray(printerTrayForA4);
     }
 }
 
```

**Returns:**
int - La bandeja de papel (cajón) que se usará para la primera página de una sección.
### getFooterDistance() {#getFooterDistance}
```
public double getFooterDistance()
```


Obtiene la distancia (en puntos) entre el pie de página y la parte inferior de la página.

 **Examples:** 

Muestra cómo ajustar el tamaño del papel, la orientación, los márgenes, junto con otras configuraciones para una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Returns:**
double - La distancia (en puntos) entre el pie de página y la parte inferior de la página.
### getFootnoteOptions() {#getFootnoteOptions}
```
public FootnoteOptions getFootnoteOptions()
```


Proporciona opciones que controlan la numeración y la posición de las notas al pie en esta sección.

 **Examples:** 

Muestra cómo configurar opciones que afectan a las notas al pie/finales en una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Hello world!");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote reference text.");

 // Configure all footnotes in the first section to restart the numbering from 1
 // at each new page and display themselves directly beneath the text on every page.
 FootnoteOptions footnoteOptions = doc.getSections().get(0).getPageSetup().getFootnoteOptions();
 footnoteOptions.setPosition(FootnotePosition.BENEATH_TEXT);
 footnoteOptions.setRestartRule(FootnoteNumberingRule.RESTART_PAGE);
 footnoteOptions.setStartNumber(1);

 builder.write(" Hello again.");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Endnote reference text.");

 // Configure all endnotes in the first section to maintain a continuous count throughout the section,
 // starting from 1. Also, set them all to appear collected at the end of the document.
 EndnoteOptions endnoteOptions = doc.getSections().get(0).getPageSetup().getEndnoteOptions();
 endnoteOptions.setPosition(EndnotePosition.END_OF_DOCUMENT);
 endnoteOptions.setRestartRule(FootnoteNumberingRule.CONTINUOUS);
 endnoteOptions.setStartNumber(1);

 doc.save(getArtifactsDir() + "PageSetup.FootnoteOptions.docx");
 
```

**Returns:**
[FootnoteOptions](../../com.aspose.words/footnoteoptions/) - The corresponding [FootnoteOptions](../../com.aspose.words/footnoteoptions/) value.
### getGutter() {#getGutter}
```
public double getGutter()
```


Obtiene la cantidad de espacio adicional añadido al margen para la encuadernación del documento.

 **Examples:** 

Muestra cómo establecer márgenes de canal.

```

 Document doc = new Document();

 // Insert text that spans several pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 for (int i = 0; i < 6; i++) {
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
             "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
     builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // A gutter adds whitespaces to either the left or right page margin,
 // which makes up for the center folding of pages in a book encroaching on the page's layout.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 // Determine how much space our pages have for text within the margins and then add an amount to pad a margin.
 Assert.assertEquals(468.00d, pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin(), 0.01d);

 pageSetup.setGutter(100.0d);

 // Set the "RtlGutter" property to "true" to place the gutter in a more suitable position for right-to-left text.
 pageSetup.setRtlGutter(true);

 // Set the "MultiplePages" property to "MultiplePagesType.MirrorMargins" to alternate
 // the left/right page side position of margins every page.
 pageSetup.setMultiplePages(MultiplePagesType.MIRROR_MARGINS);

 doc.save(getArtifactsDir() + "PageSetup.Gutter.docx");
 
```

Muestra cómo configurar un documento que puede imprimirse como un pliegue de libro.

```

 Document doc = new Document();

 // Insert text that spans 16 pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("My Booklet:");

 for (int i = 0; i < 15; i++) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.write(MessageFormat.format("Booklet face #{0}", i));
 }

 // Configure the first section's "PageSetup" property to print the document in the form of a book fold.
 // When we print this document on both sides, we can take the pages to stack them
 // and fold them all down the middle at once. The contents of the document will line up into a book fold.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setMultiplePages(MultiplePagesType.BOOK_FOLD_PRINTING);

 // We can only specify the number of sheets in multiples of 4.
 pageSetup.setSheetsPerBooklet(4);

 doc.save(getArtifactsDir() + "PageSetup.Booklet.docx");
 
```

**Returns:**
double - La cantidad de espacio adicional añadido al margen para la encuadernación del documento.
### getHeaderDistance() {#getHeaderDistance}
```
public double getHeaderDistance()
```


Obtiene la distancia (en puntos) entre el encabezado y la parte superior de la página.

 **Examples:** 

Muestra cómo ajustar el tamaño del papel, la orientación, los márgenes, junto con otras configuraciones para una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Returns:**
double - La distancia (en puntos) entre el encabezado y la parte superior de la página.
### getHeadingLevelForChapter() {#getHeadingLevelForChapter}
```
public int getHeadingLevelForChapter()
```


Obtiene el estilo de nivel de encabezado que se aplica a los títulos de los capítulos en el documento.

 **Remarks:** 

Puede ser un número del 0 al 9. 0 significa que no hay número de capítulo si se aplica al número de página.

Antes de poder crear números de página que incluyan números de capítulo, los encabezados del documento deben tener aplicado un formato de esquema numerado.

 **Examples:** 

Muestra cómo trabajar con capítulos de página.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();

 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 pageSetup.setChapterPageSeparator(com.aspose.words.ChapterPageSeparator.COLON);
 pageSetup.setHeadingLevelForChapter(1);
 
```

**Returns:**
int - El estilo de nivel de encabezado que se aplica a los títulos de capítulo en el documento.
### getLayoutMode() {#getLayoutMode}
```
public int getLayoutMode()
```


Obtiene el modo de diseño de esta sección.

 **Examples:** 

Muestra cómo especificar un para el número de caracteres que cada línea puede tener.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of characters per line in this section.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.GRID);
 builder.getPageSetup().setCharactersPerLine(10);

 // The number of characters also depends on the size of the font.
 doc.getStyles().get("Normal").getFont().setSize(20.0);

 Assert.assertEquals(8, doc.getFirstSection().getPageSetup().getCharactersPerLine());

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "PageSetup.CharactersPerLine.docx");
 
```

Muestra cómo especificar un límite para la cantidad de líneas que puede tener cada página.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of lines per page in this section.
 // A large enough font size will push some lines down onto the next page to avoid overlapping characters.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.LINE_GRID);
 builder.getPageSetup().setLinesPerPage(15);

 builder.getParagraphFormat().setSnapToGrid(true);

 for (int i = 0; i < 30; i++)
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

 doc.save(getArtifactsDir() + "PageSetup.LinesPerPage.docx");
 
```

**Returns:**
int - El modo de diseño de esta sección. El valor devuelto es una de las constantes de [SectionLayoutMode](../../com.aspose.words/sectionlayoutmode/).
### getLeftMargin() {#getLeftMargin}
```
public double getLeftMargin()
```


Obtiene la distancia (en puntos) entre el borde izquierdo de la página y el límite izquierdo del texto del cuerpo.

 **Examples:** 

Muestra cómo ajustar el tamaño del papel, la orientación, los márgenes, junto con otras configuraciones para una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Returns:**
double - La distancia (en puntos) entre el borde izquierdo de la página y el límite izquierdo del texto del cuerpo.
### getLineNumberCountBy() {#getLineNumberCountBy}
```
public int getLineNumberCountBy()
```


Obtiene el incremento numérico para los números de línea.

 **Examples:** 

Muestra cómo habilitar la numeración de líneas para una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Returns:**
int - El incremento numérico para los números de línea.
### getLineNumberDistanceFromText() {#getLineNumberDistanceFromText}
```
public double getLineNumberDistanceFromText()
```


Obtiene la distancia entre el borde derecho de los números de línea y el borde izquierdo del documento.

 **Remarks:** 

Establezca esta propiedad en cero para la distancia automática entre los números de línea y el texto del documento.

 **Examples:** 

Muestra cómo habilitar la numeración de líneas para una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Returns:**
double - Distancia entre el borde derecho de los números de línea y el borde izquierdo del documento.
### getLineNumberRestartMode() {#getLineNumberRestartMode}
```
public int getLineNumberRestartMode()
```


Obtiene la forma en que se ejecuta la numeración de líneas, es decir, si comienza de nuevo al inicio de una página o sección nueva o se ejecuta de forma continua.

 **Examples:** 

Muestra cómo habilitar la numeración de líneas para una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Returns:**
int - La forma en que se ejecuta la numeración de líneas, es decir, si se reinicia al comienzo de una nueva página o sección o se ejecuta de forma continua. El valor devuelto es una de las constantes de [LineNumberRestartMode](../../com.aspose.words/linenumberrestartmode/).
### getLineStartingNumber() {#getLineStartingNumber}
```
public int getLineStartingNumber()
```


Obtiene el número de línea inicial.

 **Examples:** 

Muestra cómo habilitar la numeración de líneas para una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Returns:**
int - El número de línea inicial.
### getLinesPerPage() {#getLinesPerPage}
```
public int getLinesPerPage()
```


Obtiene el número de líneas por página en la cuadrícula del documento.

 **Remarks:** 

El valor mínimo de la propiedad es 1. El valor máximo depende de la altura de la página y del tamaño de fuente del estilo Normal. El paso mínimo de línea es el 136 % del tamaño de fuente. Por ejemplo, el número máximo de líneas por página de una hoja Letter con márgenes de una pulgada es 39.

Por defecto, la propiedad tiene un valor en el que el paso de línea es 1,5 veces mayor que el tamaño de fuente del estilo Normal.

 **Examples:** 

Muestra cómo especificar un límite para la cantidad de líneas que puede tener cada página.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of lines per page in this section.
 // A large enough font size will push some lines down onto the next page to avoid overlapping characters.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.LINE_GRID);
 builder.getPageSetup().setLinesPerPage(15);

 builder.getParagraphFormat().setSnapToGrid(true);

 for (int i = 0; i < 30; i++)
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

 doc.save(getArtifactsDir() + "PageSetup.LinesPerPage.docx");
 
```

**Returns:**
int - La cantidad de líneas por página en la cuadrícula del documento.
### getMargins() {#getMargins}
```
public int getMargins()
```


Obtiene los [Márgenes](../../com.aspose.words/margins/) predefinidos de la página.

 **Examples:** 

Muestra cuándo recalcular el diseño de página del documento.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Saving a document to PDF, to an image, or printing for the first time will automatically
 // cache the layout of the document within its pages.
 doc.save(getArtifactsDir() + "Document.UpdatePageLayout.1.pdf");

 // Modify the document in some way.
 doc.getStyles().get("Normal").getFont().setSize(6.0);
 doc.getSections().get(0).getPageSetup().setOrientation(Orientation.LANDSCAPE);
 doc.getSections().get(0).getPageSetup().setMargins(Margins.MIRRORED);

 // In the current version of Aspose.Words, modifying the document does not automatically rebuild
 // the cached page layout. If we wish for the cached layout
 // to stay up to date, we will need to update it manually.
 doc.updatePageLayout();

 doc.save(getArtifactsDir() + "Document.UpdatePageLayout.2.pdf");
 
```

**Returns:**
int - Preajuste de [Margins](../../com.aspose.words/margins/) de la página. El valor devuelto es una de las constantes de [Margins](../../com.aspose.words/margins/).
### getMultiplePages() {#getMultiplePages}
```
public int getMultiplePages()
```


Para documentos de varias páginas, obtiene o establece cómo se imprime o renderiza un documento para que pueda encuadernarse como folleto.

 **Examples:** 

Muestra cómo establecer márgenes de canal.

```

 Document doc = new Document();

 // Insert text that spans several pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 for (int i = 0; i < 6; i++) {
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
             "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
     builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // A gutter adds whitespaces to either the left or right page margin,
 // which makes up for the center folding of pages in a book encroaching on the page's layout.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 // Determine how much space our pages have for text within the margins and then add an amount to pad a margin.
 Assert.assertEquals(468.00d, pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin(), 0.01d);

 pageSetup.setGutter(100.0d);

 // Set the "RtlGutter" property to "true" to place the gutter in a more suitable position for right-to-left text.
 pageSetup.setRtlGutter(true);

 // Set the "MultiplePages" property to "MultiplePagesType.MirrorMargins" to alternate
 // the left/right page side position of margins every page.
 pageSetup.setMultiplePages(MultiplePagesType.MIRROR_MARGINS);

 doc.save(getArtifactsDir() + "PageSetup.Gutter.docx");
 
```

Muestra cómo configurar un documento que puede imprimirse como un pliegue de libro.

```

 Document doc = new Document();

 // Insert text that spans 16 pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("My Booklet:");

 for (int i = 0; i < 15; i++) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.write(MessageFormat.format("Booklet face #{0}", i));
 }

 // Configure the first section's "PageSetup" property to print the document in the form of a book fold.
 // When we print this document on both sides, we can take the pages to stack them
 // and fold them all down the middle at once. The contents of the document will line up into a book fold.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setMultiplePages(MultiplePagesType.BOOK_FOLD_PRINTING);

 // We can only specify the number of sheets in multiples of 4.
 pageSetup.setSheetsPerBooklet(4);

 doc.save(getArtifactsDir() + "PageSetup.Booklet.docx");
 
```

**Returns:**
int - El valor int correspondiente. El valor devuelto es una de las constantes de [MultiplePagesType](../../com.aspose.words/multiplepagestype/).
### getOddAndEvenPagesHeaderFooter() {#getOddAndEvenPagesHeaderFooter}
```
public boolean getOddAndEvenPagesHeaderFooter()
```


True si el documento tiene encabezados y pies de página diferentes para páginas impares y pares.

 **Remarks:** 

Nota, cambiar esta propiedad afecta a todas las secciones del documento.

 **Examples:** 

Muestra cómo crear encabezados y pies de página en un documento usando DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

Muestra cómo habilitar o deshabilitar los encabezados/pies de página pares.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two types of header/footers.
 // 1 -  The "Primary" header/footer, which appears on every page in the section.
 // We can override the primary header/footer by a first and an even page header/footer.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Primary header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.writeln("Primary footer.");

 // 2 -  The "Even" header/footer, which appears on every even page of this section.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.writeln("Even page header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_EVEN);
 builder.writeln("Even page footer.");

 builder.moveToSection(0);
 builder.writeln("Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 3.");

 // Each section has a "PageSetup" object that specifies page appearance-related properties
 // such as orientation, size, and borders.
 // Set the "OddAndEvenPagesHeaderFooter" property to "true"
 // to display the even page header/footer on even pages.
 // Set the "OddAndEvenPagesHeaderFooter" property to "false"
 // to display the primary header/footer on even pages.
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(oddAndEvenPagesHeaderFooter);

 doc.save(getArtifactsDir() + "PageSetup.OddAndEvenPagesHeaderFooter.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getOrientation() {#getOrientation}
```
public int getOrientation()
```


Obtiene la orientación de la página.

 **Remarks:** 

Cambiar [getOrientation()](../../com.aspose.words/pagesetup/\#getOrientation) / [setOrientation(int)](../../com.aspose.words/pagesetup/\#setOrientation-int) intercambia [getPageWidth()](../../com.aspose.words/pagesetup/\#getPageWidth) / [setPageWidth(double)](../../com.aspose.words/pagesetup/\#setPageWidth-double) y [getPageHeight()](../../com.aspose.words/pagesetup/\#getPageHeight) / [setPageHeight(double)](../../com.aspose.words/pagesetup/\#setPageHeight-double).

 **Examples:** 

Muestra cómo aplicar y revertir la configuración de página a secciones en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

Muestra cómo ajustar el tamaño del papel, la orientación, los márgenes, junto con otras configuraciones para una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Returns:**
int - La orientación de la página. El valor devuelto es una de las constantes de [Orientation](../../com.aspose.words/orientation/).
### getOtherPagesTray() {#getOtherPagesTray}
```
public int getOtherPagesTray()
```


Obtiene la bandeja de papel (compartimento) que se usará para todas las páginas excepto la primera de una sección. El valor es específico de la implementación (impresora).

 **Examples:** 

Muestra cómo configurar la impresión usando diferentes bandejas de impresora para distintos tamaños de papel.

```

 Document doc = new Document();

 /// Choose the default printer to be used for printing this document.
 PrintService printService = PrintServiceLookup.lookupDefaultPrintService();
 Media[] trays = (Media[]) printService.getSupportedAttributeValues(Media.class, null, null);

 // This is the tray we will use for pages in the "A4" paper size.
 int printerTrayForA4 = trays[0].getValue();
 // This is the tray we will use for pages in the "Letter" paper size.
 int printerTrayForLetter = trays[1].getValue();

 // Modify the PageSettings object of this section to get Microsoft Word to instruct the printer
 // to use one of the trays we identified above, depending on this section's paper size.
 for (Section section : doc.getSections()) {
     if (section.getPageSetup().getPaperSize() == PaperSize.LETTER) {
         section.getPageSetup().setFirstPageTray(printerTrayForLetter);
         section.getPageSetup().setOtherPagesTray(printerTrayForLetter);
     } else if (section.getPageSetup().getPaperSize() == PaperSize.A4) {
         section.getPageSetup().setFirstPageTray(printerTrayForA4);
         section.getPageSetup().setOtherPagesTray(printerTrayForA4);
     }
 }
 
```

**Returns:**
int - La bandeja de papel (compartimento) que se usará para todas las páginas excepto la primera de una sección.
### getPageHeight() {#getPageHeight}
```
public double getPageHeight()
```


Obtiene la altura de la página en puntos.

 **Examples:** 

Muestra cómo insertar una imagen y usarla como marca de agua.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert the image into the header so that it will be visible on every page.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 Shape shape = builder.insertImage(getImageDir() + "Transparent background logo.png");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);

 // Place the image at the center of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setLeft((builder.getPageSetup().getPageWidth() - shape.getWidth()) / 2.0);
 shape.setTop((builder.getPageSetup().getPageHeight() - shape.getHeight()) / 2.0);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertWatermark.docx");
 
```

**Returns:**
double - La altura de la página en puntos.
### getPageNumberStyle() {#getPageNumberStyle}
```
public int getPageNumberStyle()
```


Obtiene el formato del número de página.

 **Examples:** 

Muestra cómo configurar la numeración de páginas en una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 3.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("Section 2, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 3.");

 // Move the document builder to the first section's primary header,
 // which every page in that section will display.
 builder.moveToSection(0);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);

 // Insert a PAGE field, which will display the number of the current page.
 builder.write("Page ");
 builder.insertField("PAGE", "");

 // Configure the section to have the page count that PAGE fields display start from 5.
 // Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageStartingNumber(5);
 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);

 // Create another primary header for the second section, with another PAGE field.
 builder.moveToSection(1);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write(" - ");
 builder.insertField("PAGE", "");
 builder.write(" - ");

 // Configure the section to have the page count that PAGE fields display start from 10.
 // Also, configure all PAGE fields to display their page numbers using Arabic numbers.
 pageSetup = doc.getSections().get(1).getPageSetup();
 pageSetup.setPageStartingNumber(10);
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageNumberStyle(NumberStyle.ARABIC);

 doc.save(getArtifactsDir() + "PageSetup.PageNumbering.docx");
 
```

**Returns:**
int - El formato del número de página. El valor devuelto es uno de los constantes de [NumberStyle](../../com.aspose.words/numberstyle/) constantes.
### getPageStartingNumber() {#getPageStartingNumber}
```
public int getPageStartingNumber()
```


Obtiene el número de página inicial de la sección.

 **Remarks:** 

La propiedad [getRestartPageNumbering()](../../com.aspose.words/pagesetup/\#getRestartPageNumbering) / [setRestartPageNumbering(boolean)](../../com.aspose.words/pagesetup/\#setRestartPageNumbering-boolean) , si se establece en false , sobrescribirá la propiedad [getPageStartingNumber()](../../com.aspose.words/pagesetup/\#getPageStartingNumber) / [setPageStartingNumber(int)](../../com.aspose.words/pagesetup/\#setPageStartingNumber-int) para que la numeración de páginas pueda continuar desde la sección anterior.

 **Examples:** 

Muestra cómo configurar la numeración de páginas en una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 3.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("Section 2, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 3.");

 // Move the document builder to the first section's primary header,
 // which every page in that section will display.
 builder.moveToSection(0);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);

 // Insert a PAGE field, which will display the number of the current page.
 builder.write("Page ");
 builder.insertField("PAGE", "");

 // Configure the section to have the page count that PAGE fields display start from 5.
 // Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageStartingNumber(5);
 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);

 // Create another primary header for the second section, with another PAGE field.
 builder.moveToSection(1);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write(" - ");
 builder.insertField("PAGE", "");
 builder.write(" - ");

 // Configure the section to have the page count that PAGE fields display start from 10.
 // Also, configure all PAGE fields to display their page numbers using Arabic numbers.
 pageSetup = doc.getSections().get(1).getPageSetup();
 pageSetup.setPageStartingNumber(10);
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageNumberStyle(NumberStyle.ARABIC);

 doc.save(getArtifactsDir() + "PageSetup.PageNumbering.docx");
 
```

**Returns:**
int - El número de página inicial de la sección.
### getPageWidth() {#getPageWidth}
```
public double getPageWidth()
```


Obtiene el ancho de la página en puntos.

 **Examples:** 

Muestra cómo insertar una imagen y usarla como marca de agua.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert the image into the header so that it will be visible on every page.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 Shape shape = builder.insertImage(getImageDir() + "Transparent background logo.png");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);

 // Place the image at the center of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setLeft((builder.getPageSetup().getPageWidth() - shape.getWidth()) / 2.0);
 shape.setTop((builder.getPageSetup().getPageHeight() - shape.getHeight()) / 2.0);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertWatermark.docx");
 
```

Muestra cómo insertar una imagen flotante y especificar su posición y tamaño.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);

 // Configure the shape's "RelativeHorizontalPosition" property to treat the value of the "Left" property
 // as the shape's horizontal distance, in points, from the left side of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);

 // Set the shape's horizontal distance from the left side of the page to 100.
 shape.setLeft(100.0);

 // Use the "RelativeVerticalPosition" property in a similar way to position the shape 80pt below the top of the page.
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setTop(80.0);

 // Set the shape's height, which will automatically scale the width to preserve dimensions.
 shape.setHeight(125.0);

 Assert.assertEquals(125.0d, shape.getWidth());

 // The "Bottom" and "Right" properties contain the bottom and right edges of the image.
 Assert.assertEquals(shape.getTop() + shape.getHeight(), shape.getBottom());
 Assert.assertEquals(shape.getLeft() + shape.getWidth(), shape.getRight());

 doc.save(getArtifactsDir() + "Image.CreateFloatingPositionSize.docx");
 
```

**Returns:**
double - El ancho de la página en puntos.
### getPaperSize() {#getPaperSize}
```
public int getPaperSize()
```


Obtiene el tamaño del papel.

 **Remarks:** 

Al establecer esta propiedad actualiza los valores de [getPageWidth()](../../com.aspose.words/pagesetup/\#getPageWidth) / [setPageWidth(double)](../../com.aspose.words/pagesetup/\#setPageWidth-double) y [getPageHeight()](../../com.aspose.words/pagesetup/\#getPageHeight) / [setPageHeight(double)](../../com.aspose.words/pagesetup/\#setPageHeight-double). Establecer este valor a [PaperSize.CUSTOM](../../com.aspose.words/papersize/\#CUSTOM) no cambia los valores existentes.

 **Examples:** 

Muestra cómo ajustar el tamaño del papel, la orientación, los márgenes, junto con otras configuraciones para una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

Muestra cómo establecer tamaños de página.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can change the current page's size to a pre-defined size
 // by using the "PaperSize" property of this section's PageSetup object.
 builder.getPageSetup().setPaperSize(PaperSize.TABLOID);

 Assert.assertEquals(792.0d, builder.getPageSetup().getPageWidth());
 Assert.assertEquals(1224.0d, builder.getPageSetup().getPageHeight());

 builder.writeln(MessageFormat.format("This page is {0}x{1}.", builder.getPageSetup().getPageWidth(), builder.getPageSetup().getPageHeight()));

 // Each section has its own PageSetup object. When we use a document builder to make a new section,
 // that section's PageSetup object inherits all the previous section's PageSetup object's values.
 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);

 Assert.assertEquals(PaperSize.TABLOID, builder.getPageSetup().getPaperSize());

 builder.getPageSetup().setPaperSize(PaperSize.A5);
 builder.writeln(MessageFormat.format("This page is {0}x{1}.", builder.getPageSetup().getPageWidth(), builder.getPageSetup().getPageHeight()));

 Assert.assertEquals(419.55d, builder.getPageSetup().getPageWidth());
 Assert.assertEquals(595.30d, builder.getPageSetup().getPageHeight());

 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);

 // Set a custom size for this section's pages.
 builder.getPageSetup().setPageWidth(620.0);
 builder.getPageSetup().setPageHeight(480.0);

 Assert.assertEquals(PaperSize.CUSTOM, builder.getPageSetup().getPaperSize());

 builder.writeln(MessageFormat.format("This page is {0}x{1}.", builder.getPageSetup().getPageWidth(), builder.getPageSetup().getPageHeight()));

 doc.save(getArtifactsDir() + "PageSetup.PaperSizes.docx");
 
```

Muestra cómo establecer el tamaño de papel de JisB4 o JisB5.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();
 // Set the paper size to JisB4 (257x364mm).
 pageSetup.setPaperSize(PaperSize.JIS_B_4);
 // Alternatively, set the paper size to JisB5. (182x257mm).
 pageSetup.setPaperSize(PaperSize.JIS_B_5);
 
```

Muestra cómo construir un documento Aspose.Words manualmente.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Returns:**
int - El tamaño de papel. El valor devuelto es uno de los constantes de [PaperSize](../../com.aspose.words/papersize/) constantes.
### getRestartPageNumbering() {#getRestartPageNumbering}
```
public boolean getRestartPageNumbering()
```


True si la numeración de páginas se reinicia al comienzo de la sección.

 **Remarks:** 

Si se establece en false , la propiedad [getRestartPageNumbering()](../../com.aspose.words/pagesetup/\#getRestartPageNumbering) / [setRestartPageNumbering(boolean)](../../com.aspose.words/pagesetup/\#setRestartPageNumbering-boolean) sobrescribirá la propiedad [getPageStartingNumber()](../../com.aspose.words/pagesetup/\#getPageStartingNumber) / [setPageStartingNumber(int)](../../com.aspose.words/pagesetup/\#setPageStartingNumber-int) para que la numeración de páginas pueda continuar desde la sección anterior.

 **Examples:** 

Muestra cómo configurar la numeración de páginas en una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 3.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("Section 2, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 3.");

 // Move the document builder to the first section's primary header,
 // which every page in that section will display.
 builder.moveToSection(0);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);

 // Insert a PAGE field, which will display the number of the current page.
 builder.write("Page ");
 builder.insertField("PAGE", "");

 // Configure the section to have the page count that PAGE fields display start from 5.
 // Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageStartingNumber(5);
 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);

 // Create another primary header for the second section, with another PAGE field.
 builder.moveToSection(1);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write(" - ");
 builder.insertField("PAGE", "");
 builder.write(" - ");

 // Configure the section to have the page count that PAGE fields display start from 10.
 // Also, configure all PAGE fields to display their page numbers using Arabic numbers.
 pageSetup = doc.getSections().get(1).getPageSetup();
 pageSetup.setPageStartingNumber(10);
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageNumberStyle(NumberStyle.ARABIC);

 doc.save(getArtifactsDir() + "PageSetup.PageNumbering.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getRightMargin() {#getRightMargin}
```
public double getRightMargin()
```


Obtiene la distancia (en puntos) entre el borde derecho de la página y el límite derecho del texto del cuerpo.

 **Examples:** 

Muestra cómo ajustar el tamaño del papel, la orientación, los márgenes, junto con otras configuraciones para una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Returns:**
double - La distancia (en puntos) entre el borde derecho de la página y el límite derecho del texto del cuerpo.
### getRtlGutter() {#getRtlGutter}
```
public boolean getRtlGutter()
```


Obtiene si Microsoft Word usa canaletas para la sección según un idioma de derecha a izquierda o de izquierda a derecha.

 **Examples:** 

Muestra cómo establecer márgenes de canal.

```

 Document doc = new Document();

 // Insert text that spans several pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 for (int i = 0; i < 6; i++) {
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
             "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
     builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // A gutter adds whitespaces to either the left or right page margin,
 // which makes up for the center folding of pages in a book encroaching on the page's layout.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 // Determine how much space our pages have for text within the margins and then add an amount to pad a margin.
 Assert.assertEquals(468.00d, pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin(), 0.01d);

 pageSetup.setGutter(100.0d);

 // Set the "RtlGutter" property to "true" to place the gutter in a more suitable position for right-to-left text.
 pageSetup.setRtlGutter(true);

 // Set the "MultiplePages" property to "MultiplePagesType.MirrorMargins" to alternate
 // the left/right page side position of margins every page.
 pageSetup.setMultiplePages(MultiplePagesType.MIRROR_MARGINS);

 doc.save(getArtifactsDir() + "PageSetup.Gutter.docx");
 
```

**Returns:**
boolean - Indica si Microsoft Word usa márgenes internos (gutters) para la sección según un idioma de derecha a izquierda o de izquierda a derecha.
### getSectionStart() {#getSectionStart}
```
public int getSectionStart()
```


Obtiene el tipo de salto de sección para el objeto especificado.

 **Examples:** 

Muestra cómo especificar cómo una nueva sección se separa de la anterior.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("This text is in section 1.");

 // Section break types determine how a new section separates itself from the previous section.
 // Below are five types of section breaks.
 // 1 -  Starts the next section on a new page:
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("This text is in section 2.");

 Assert.assertEquals(SectionStart.NEW_PAGE, doc.getSections().get(1).getPageSetup().getSectionStart());

 // 2 -  Starts the next section on the current page:
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.writeln("This text is in section 3.");

 Assert.assertEquals(SectionStart.CONTINUOUS, doc.getSections().get(2).getPageSetup().getSectionStart());

 // 3 -  Starts the next section on a new even page:
 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);
 builder.writeln("This text is in section 4.");

 Assert.assertEquals(SectionStart.EVEN_PAGE, doc.getSections().get(3).getPageSetup().getSectionStart());

 // 4 -  Starts the next section on a new odd page:
 builder.insertBreak(BreakType.SECTION_BREAK_ODD_PAGE);
 builder.writeln("This text is in section 5.");

 Assert.assertEquals(SectionStart.ODD_PAGE, doc.getSections().get(4).getPageSetup().getSectionStart());

 // 5 -  Starts the next section on a new column:
 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setCount(2);

 builder.insertBreak(BreakType.SECTION_BREAK_NEW_COLUMN);
 builder.writeln("This text is in section 6.");

 Assert.assertEquals(SectionStart.NEW_COLUMN, doc.getSections().get(5).getPageSetup().getSectionStart());

 doc.save(getArtifactsDir() + "PageSetup.SetSectionStart.docx");
 
```

Muestra cómo construir un documento Aspose.Words manualmente.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Returns:**
int - El tipo de salto de sección para el objeto especificado. El valor devuelto es uno de los constantes de [SectionStart](../../com.aspose.words/sectionstart/) constantes.
### getSheetsPerBooklet() {#getSheetsPerBooklet}
```
public int getSheetsPerBooklet()
```


Obtiene el número de páginas que se incluirán en cada folleto.

 **Examples:** 

Muestra cómo configurar un documento que puede imprimirse como un pliegue de libro.

```

 Document doc = new Document();

 // Insert text that spans 16 pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("My Booklet:");

 for (int i = 0; i < 15; i++) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.write(MessageFormat.format("Booklet face #{0}", i));
 }

 // Configure the first section's "PageSetup" property to print the document in the form of a book fold.
 // When we print this document on both sides, we can take the pages to stack them
 // and fold them all down the middle at once. The contents of the document will line up into a book fold.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setMultiplePages(MultiplePagesType.BOOK_FOLD_PRINTING);

 // We can only specify the number of sheets in multiples of 4.
 pageSetup.setSheetsPerBooklet(4);

 doc.save(getArtifactsDir() + "PageSetup.Booklet.docx");
 
```

**Returns:**
int - El número de páginas que se incluirán en cada folleto.
### getSuppressEndnotes() {#getSuppressEndnotes}
```
public boolean getSuppressEndnotes()
```


True si las notas al final se imprimen al final de la siguiente sección que no suprime notas al final. Las notas al final suprimidas se imprimen antes de las notas al final en esa sección.

 **Examples:** 

Muestra cómo almacenar notas al final al final de cada sección y modificar sus posiciones.

```

 public void suppressEndnotes() throws Exception {
     Document doc = new Document();
     doc.removeAllChildren();

     // By default, a document compiles all endnotes at its end.
     Assert.assertEquals(EndnotePosition.END_OF_DOCUMENT, doc.getEndnoteOptions().getPosition());

     // We use the "Position" property of the document's "EndnoteOptions" object
     // to collect endnotes at the end of each section instead.
     doc.getEndnoteOptions().setPosition(EndnotePosition.END_OF_SECTION);

     insertSectionWithEndnote(doc, "Section 1", "Endnote 1, will stay in section 1");
     insertSectionWithEndnote(doc, "Section 2", "Endnote 2, will be pushed down to section 3");
     insertSectionWithEndnote(doc, "Section 3", "Endnote 3, will stay in section 3");

     // While getting sections to display their respective endnotes, we can set the "SuppressEndnotes" flag
     // of a section's "PageSetup" object to "true" to revert to the default behavior and pass its endnotes
     // onto the next section.
     PageSetup pageSetup = doc.getSections().get(1).getPageSetup();
     pageSetup.setSuppressEndnotes(true);

     doc.save(getArtifactsDir() + "PageSetup.SuppressEndnotes.docx");
 }

 /// 
 /// Append a section with text and an endnote to a document.
 /// 
 private static void insertSectionWithEndnote(Document doc, String sectionBodyText, String endnoteText) {
     Section section = new Section(doc);

     doc.appendChild(section);

     Body body = new Body(doc);
     section.appendChild(body);

     Assert.assertEquals(body.getParentNode(), section);

     Paragraph para = new Paragraph(doc);
     body.appendChild(para);

     Assert.assertEquals(para.getParentNode(), body);

     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.moveTo(para);
     builder.write(sectionBodyText);
     builder.insertFootnote(FootnoteType.ENDNOTE, endnoteText);
 }
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getTextColumns() {#getTextColumns}
```
public TextColumnCollection getTextColumns()
```


Devuelve una colección que representa el conjunto de columnas de texto.

 **Examples:** 

Muestra cómo crear múltiples columnas espaciadas uniformemente en una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```

**Returns:**
[TextColumnCollection](../../com.aspose.words/textcolumncollection/) - A collection that represents the set of text columns.
### getTextOrientation() {#getTextOrientation}
```
public int getTextOrientation()
```


Permite especificar [getTextOrientation()](../../com.aspose.words/pagesetup/\#getTextOrientation) / [setTextOrientation(int)](../../com.aspose.words/pagesetup/\#setTextOrientation-int) para toda la página. El valor predeterminado es [TextOrientation.HORIZONTAL](../../com.aspose.words/textorientation/\#HORIZONTAL)

 **Remarks:** 

Esta propiedad solo es compatible con los formatos nativos de MS Word DOCX, WML, RTF y DOC.

 **Examples:** 

Muestra cómo establecer la orientación del texto.

```

 Document doc = new Document();

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Set the "TextOrientation" property to "TextOrientation.Upward" to rotate all the text 90 degrees
 // to the right so that all left-to-right text now goes top-to-bottom.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setTextOrientation(TextOrientation.UPWARD);

 doc.save(getArtifactsDir() + "PageSetup.SetTextOrientation.docx");
 
```

**Returns:**
int - El valor int correspondiente. El valor devuelto es uno de los constantes de [TextOrientation](../../com.aspose.words/textorientation/) constantes.
### getTopMargin() {#getTopMargin}
```
public double getTopMargin()
```


Obtiene la distancia (en puntos) entre el borde superior de la página y el límite superior del texto del cuerpo.

 **Examples:** 

Muestra cómo ajustar el tamaño del papel, la orientación, los márgenes, junto con otras configuraciones para una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Returns:**
double - La distancia (en puntos) entre el borde superior de la página y el límite superior del texto del cuerpo.
### getVerticalAlignment() {#getVerticalAlignment}
```
public int getVerticalAlignment()
```


Obtiene la alineación vertical del texto en cada página de un documento o sección.

 **Examples:** 

Muestra cómo aplicar y revertir la configuración de página a secciones en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

**Returns:**
int - La alineación vertical del texto en cada página de un documento o sección. El valor devuelto es uno de los constantes de [PageVerticalAlignment](../../com.aspose.words/pageverticalalignment/) constantes.
### setBidi(boolean value) {#setBidi-boolean}
```
public void setBidi(boolean value)
```


Especifica que esta sección contiene texto bidireccional (scripts complejos).

 **Remarks:** 

Cuando  true , las columnas en esta sección se disponen de derecha a izquierda.

 **Examples:** 

Muestra cómo establecer el orden de las columnas de texto en una sección.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.getTextColumns().setCount(3);

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.write("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.write("Column 2.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.write("Column 3.");

 // Set the "Bidi" property to "true" to arrange the columns starting from the page's right side.
 // The order of the columns will match the direction of the right-to-left text.
 // Set the "Bidi" property to "false" to arrange the columns starting from the page's left side.
 // The order of the columns will match the direction of the left-to-right text.
 pageSetup.setBidi(reverseColumns);

 doc.save(getArtifactsDir() + "PageSetup.Bidi.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setBorderAlwaysInFront(boolean value) {#setBorderAlwaysInFront-boolean}
```
public void setBorderAlwaysInFront(boolean value)
```


Especifica dónde se posiciona el borde de la página en relación con los textos y objetos intersectados.

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
| valor | boolean | El valor  boolean  correspondiente. |

### setBorderAppliesTo(int value) {#setBorderAppliesTo-int}
```
public void setBorderAppliesTo(int value)
```


Especifica en qué páginas se imprime el borde de la página.

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
| value | int | El valor entero correspondiente. El valor debe ser uno de los constantes [PageBorderAppliesTo](../../com.aspose.words/pageborderappliesto/). |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |
| valor | java.lang.Object |  |

### setBorderDistanceFrom(int value) {#setBorderDistanceFrom-int}
```
public void setBorderDistanceFrom(int value)
```


Establece un valor que indica si el borde de página especificado se mide desde el borde de la página o desde el texto que lo rodea.

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
| value | int | Un valor que indica si el borde de página especificado se mide desde el borde de la página o desde el texto que lo rodea. El valor debe ser uno de los constantes [PageBorderDistanceFrom](../../com.aspose.words/pageborderdistancefrom/). |

### setBorderSurroundsFooter(boolean value) {#setBorderSurroundsFooter-boolean}
```
public void setBorderSurroundsFooter(boolean value)
```


Especifica si el borde de página incluye o excluye el pie de página.

 **Remarks:** 

Nota, cambiar esta propiedad afecta a todas las secciones del documento.

 **Examples:** 

Muestra cómo aplicar un borde a la página y al encabezado/pie de página.

```

 Document doc = new Document();

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This is the main body text.");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("This is the header.");
 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.write("This is the footer.");
 builder.moveToDocumentEnd();

 // Insert a blue double-line border.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.getBorders().setLineStyle(LineStyle.DOUBLE);
 pageSetup.getBorders().setColor(Color.BLUE);

 // A section's PageSetup object has "BorderSurroundsHeader" and "BorderSurroundsFooter" flags that determine
 // whether a page border surrounds the main body text, also includes the header or footer, respectively.
 // Set the "BorderSurroundsHeader" flag to "true" to surround the header with our border,
 // and then set the "BorderSurroundsFooter" flag to leave the footer outside of the border.
 pageSetup.setBorderSurroundsHeader(true);
 pageSetup.setBorderSurroundsFooter(false);

 doc.save(getArtifactsDir() + "PageSetup.PageBorder.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setBorderSurroundsHeader(boolean value) {#setBorderSurroundsHeader-boolean}
```
public void setBorderSurroundsHeader(boolean value)
```


Especifica si el borde de página incluye o excluye el encabezado.

 **Remarks:** 

Nota, cambiar esta propiedad afecta a todas las secciones del documento.

 **Examples:** 

Muestra cómo aplicar un borde a la página y al encabezado/pie de página.

```

 Document doc = new Document();

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This is the main body text.");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("This is the header.");
 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.write("This is the footer.");
 builder.moveToDocumentEnd();

 // Insert a blue double-line border.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.getBorders().setLineStyle(LineStyle.DOUBLE);
 pageSetup.getBorders().setColor(Color.BLUE);

 // A section's PageSetup object has "BorderSurroundsHeader" and "BorderSurroundsFooter" flags that determine
 // whether a page border surrounds the main body text, also includes the header or footer, respectively.
 // Set the "BorderSurroundsHeader" flag to "true" to surround the header with our border,
 // and then set the "BorderSurroundsFooter" flag to leave the footer outside of the border.
 pageSetup.setBorderSurroundsHeader(true);
 pageSetup.setBorderSurroundsFooter(false);

 doc.save(getArtifactsDir() + "PageSetup.PageBorder.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setBottomMargin(double value) {#setBottomMargin-double}
```
public void setBottomMargin(double value)
```


Establece la distancia (en puntos) entre el borde inferior de la página y el límite inferior del texto del cuerpo.

 **Examples:** 

Muestra cómo ajustar el tamaño del papel, la orientación, los márgenes, junto con otras configuraciones para una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | La distancia (en puntos) entre el borde inferior de la página y el límite inferior del texto del cuerpo. |

### setChapterPageSeparator(int value) {#setChapterPageSeparator-int}
```
public void setChapterPageSeparator(int value)
```


Establece el carácter separador que aparece entre el número del capítulo y el número de página.

 **Remarks:** 

Antes de poder crear números de página que incluyan números de capítulo, los encabezados del documento deben tener aplicado un formato de esquema numerado.

 **Examples:** 

Muestra cómo trabajar con capítulos de página.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();

 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 pageSetup.setChapterPageSeparator(com.aspose.words.ChapterPageSeparator.COLON);
 pageSetup.setHeadingLevelForChapter(1);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El carácter separador que aparece entre el número de capítulo y el número de página. El valor debe ser uno de los constantes [ChapterPageSeparator](../../com.aspose.words/chapterpageseparator/). |

### setCharactersPerLine(int value) {#setCharactersPerLine-int}
```
public void setCharactersPerLine(int value)
```


Establece el número de caracteres por línea en la cuadrícula del documento.

 **Remarks:** 

El valor mínimo de la propiedad es 1. El valor máximo depende del ancho de la página y del tamaño de fuente del estilo Normal. La distancia mínima entre caracteres es el 90 por ciento del tamaño de fuente. Por ejemplo, el número máximo de caracteres por línea de una página Letter con márgenes de una pulgada es 43.

Por defecto, la propiedad tiene un valor en el que la distancia entre caracteres es igual al tamaño de fuente del estilo Normal.

 **Examples:** 

Muestra cómo especificar un para el número de caracteres que cada línea puede tener.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of characters per line in this section.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.GRID);
 builder.getPageSetup().setCharactersPerLine(10);

 // The number of characters also depends on the size of the font.
 doc.getStyles().get("Normal").getFont().setSize(20.0);

 Assert.assertEquals(8, doc.getFirstSection().getPageSetup().getCharactersPerLine());

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "PageSetup.CharactersPerLine.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El número de caracteres por línea en la cuadrícula del documento. |

### setDifferentFirstPageHeaderFooter(boolean value) {#setDifferentFirstPageHeaderFooter-boolean}
```
public void setDifferentFirstPageHeaderFooter(boolean value)
```


Verdadero si se utiliza un encabezado o pie de página diferente en la primera página.

 **Examples:** 

Muestra cómo crear encabezados y pies de página en un documento usando DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

Muestra cómo rastrear el orden en que una operación de reemplazo de texto recorre los nodos.

```

 public void order(boolean differentFirstPageHeaderFooter) throws Exception {
     Document doc = new Document(getMyDir() + "Header and footer types.docx");

     Section firstPageSection = doc.getFirstSection();

     ReplaceLog logger = new ReplaceLog();
     FindReplaceOptions options = new FindReplaceOptions();
     {
         options.setReplacingCallback(logger);
     }

     // Using a different header/footer for the first page will affect the search order.
     firstPageSection.getPageSetup().setDifferentFirstPageHeaderFooter(differentFirstPageHeaderFooter);
     doc.getRange().replace(Pattern.compile("(header|footer)"), "", options);

     if (differentFirstPageHeaderFooter)
         Assert.assertEquals("First headerFirst footerSecond headerSecond footerThird headerThird footer",
                 logger.Text().replace("\r", ""));
     else
         Assert.assertEquals("Third headerFirst headerThird footerFirst footerSecond headerSecond footer",
                 logger.Text().replace("\r", ""));
 }

 public static Object[][] orderDataProvider() throws Exception {
     return new Object[][]
             {
                     {false},
                     {true},
             };
 }

 /// 
 /// During a find-and-replace operation, records the contents of every node that has text that the operation 'finds',
 /// in the state it is in before the replacement takes place.
 /// This will display the order in which the text replacement operation traverses nodes.
 /// 
 private static class ReplaceLog implements IReplacingCallback {
     public int replacing(ReplacingArgs args) {
         mTextBuilder.append(args.getMatchNode().getText());
         return ReplaceAction.SKIP;
     }

     public String Text() {
         return mTextBuilder.toString();
     }

     private final StringBuilder mTextBuilder = new StringBuilder();
 }
 
```

Muestra cómo habilitar o deshabilitar los encabezados/pies de página principales.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two types of header/footers.
 // 1 -  The "First" header/footer, which appears on the first page of the section.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.writeln("First page header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_FIRST);
 builder.writeln("First page footer.");

 // 2 -  The "Primary" header/footer, which appears on every page in the section.
 // We can override the primary header/footer by a first and an even page header/footer.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Primary header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.writeln("Primary footer.");

 builder.moveToSection(0);
 builder.writeln("Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 3.");

 // Each section has a "PageSetup" object that specifies page appearance-related properties
 // such as orientation, size, and borders.
 // Set the "DifferentFirstPageHeaderFooter" property to "true" to apply the first header/footer to the first page.
 // Set the "DifferentFirstPageHeaderFooter" property to "false"
 // to make the first page display the primary header/footer.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(differentFirstPageHeaderFooter);

 doc.save(getArtifactsDir() + "PageSetup.DifferentFirstPageHeaderFooter.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setFirstPageTray(int value) {#setFirstPageTray-int}
```
public void setFirstPageTray(int value)
```


Establece la bandeja de papel (cajón) que se usará para la primera página de una sección. El valor es específico de la implementación (impresora).

 **Examples:** 

Muestra cómo configurar la impresión usando diferentes bandejas de impresora para distintos tamaños de papel.

```

 Document doc = new Document();

 /// Choose the default printer to be used for printing this document.
 PrintService printService = PrintServiceLookup.lookupDefaultPrintService();
 Media[] trays = (Media[]) printService.getSupportedAttributeValues(Media.class, null, null);

 // This is the tray we will use for pages in the "A4" paper size.
 int printerTrayForA4 = trays[0].getValue();
 // This is the tray we will use for pages in the "Letter" paper size.
 int printerTrayForLetter = trays[1].getValue();

 // Modify the PageSettings object of this section to get Microsoft Word to instruct the printer
 // to use one of the trays we identified above, depending on this section's paper size.
 for (Section section : doc.getSections()) {
     if (section.getPageSetup().getPaperSize() == PaperSize.LETTER) {
         section.getPageSetup().setFirstPageTray(printerTrayForLetter);
         section.getPageSetup().setOtherPagesTray(printerTrayForLetter);
     } else if (section.getPageSetup().getPaperSize() == PaperSize.A4) {
         section.getPageSetup().setFirstPageTray(printerTrayForA4);
         section.getPageSetup().setOtherPagesTray(printerTrayForA4);
     }
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | La bandeja de papel (cajón) que se usará para la primera página de una sección. |

### setFooterDistance(double value) {#setFooterDistance-double}
```
public void setFooterDistance(double value)
```


Establece la distancia (en puntos) entre el pie de página y la parte inferior de la página.

 **Examples:** 

Muestra cómo ajustar el tamaño del papel, la orientación, los márgenes, junto con otras configuraciones para una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | La distancia (en puntos) entre el pie de página y el borde inferior de la página. |

### setGutter(double value) {#setGutter-double}
```
public void setGutter(double value)
```


Establece la cantidad de espacio adicional añadido al margen para la encuadernación del documento.

 **Examples:** 

Muestra cómo establecer márgenes de canal.

```

 Document doc = new Document();

 // Insert text that spans several pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 for (int i = 0; i < 6; i++) {
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
             "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
     builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // A gutter adds whitespaces to either the left or right page margin,
 // which makes up for the center folding of pages in a book encroaching on the page's layout.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 // Determine how much space our pages have for text within the margins and then add an amount to pad a margin.
 Assert.assertEquals(468.00d, pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin(), 0.01d);

 pageSetup.setGutter(100.0d);

 // Set the "RtlGutter" property to "true" to place the gutter in a more suitable position for right-to-left text.
 pageSetup.setRtlGutter(true);

 // Set the "MultiplePages" property to "MultiplePagesType.MirrorMargins" to alternate
 // the left/right page side position of margins every page.
 pageSetup.setMultiplePages(MultiplePagesType.MIRROR_MARGINS);

 doc.save(getArtifactsDir() + "PageSetup.Gutter.docx");
 
```

Muestra cómo configurar un documento que puede imprimirse como un pliegue de libro.

```

 Document doc = new Document();

 // Insert text that spans 16 pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("My Booklet:");

 for (int i = 0; i < 15; i++) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.write(MessageFormat.format("Booklet face #{0}", i));
 }

 // Configure the first section's "PageSetup" property to print the document in the form of a book fold.
 // When we print this document on both sides, we can take the pages to stack them
 // and fold them all down the middle at once. The contents of the document will line up into a book fold.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setMultiplePages(MultiplePagesType.BOOK_FOLD_PRINTING);

 // We can only specify the number of sheets in multiples of 4.
 pageSetup.setSheetsPerBooklet(4);

 doc.save(getArtifactsDir() + "PageSetup.Booklet.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | La cantidad de espacio adicional añadido al margen para la encuadernación del documento. |

### setHeaderDistance(double value) {#setHeaderDistance-double}
```
public void setHeaderDistance(double value)
```


Establece la distancia (en puntos) entre el encabezado y la parte superior de la página.

 **Examples:** 

Muestra cómo ajustar el tamaño del papel, la orientación, los márgenes, junto con otras configuraciones para una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | La distancia (en puntos) entre el encabezado y el borde superior de la página. |

### setHeadingLevelForChapter(int value) {#setHeadingLevelForChapter-int}
```
public void setHeadingLevelForChapter(int value)
```


Establece el estilo de nivel de encabezado que se aplica a los títulos de capítulo en el documento.

 **Remarks:** 

Puede ser un número del 0 al 9. 0 significa que no hay número de capítulo si se aplica al número de página.

Antes de poder crear números de página que incluyan números de capítulo, los encabezados del documento deben tener aplicado un formato de esquema numerado.

 **Examples:** 

Muestra cómo trabajar con capítulos de página.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();

 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 pageSetup.setChapterPageSeparator(com.aspose.words.ChapterPageSeparator.COLON);
 pageSetup.setHeadingLevelForChapter(1);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El estilo de nivel de encabezado que se aplica a los títulos de capítulo en el documento. |

### setLayoutMode(int value) {#setLayoutMode-int}
```
public void setLayoutMode(int value)
```


Establece el modo de diseño de esta sección.

 **Examples:** 

Muestra cómo especificar un para el número de caracteres que cada línea puede tener.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of characters per line in this section.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.GRID);
 builder.getPageSetup().setCharactersPerLine(10);

 // The number of characters also depends on the size of the font.
 doc.getStyles().get("Normal").getFont().setSize(20.0);

 Assert.assertEquals(8, doc.getFirstSection().getPageSetup().getCharactersPerLine());

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "PageSetup.CharactersPerLine.docx");
 
```

Muestra cómo especificar un límite para la cantidad de líneas que puede tener cada página.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of lines per page in this section.
 // A large enough font size will push some lines down onto the next page to avoid overlapping characters.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.LINE_GRID);
 builder.getPageSetup().setLinesPerPage(15);

 builder.getParagraphFormat().setSnapToGrid(true);

 for (int i = 0; i < 30; i++)
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

 doc.save(getArtifactsDir() + "PageSetup.LinesPerPage.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El modo de diseño de esta sección. El valor debe ser uno de los constantes [SectionLayoutMode](../../com.aspose.words/sectionlayoutmode/). |

### setLeftMargin(double value) {#setLeftMargin-double}
```
public void setLeftMargin(double value)
```


Establece la distancia (en puntos) entre el borde izquierdo de la página y el límite izquierdo del texto del cuerpo.

 **Examples:** 

Muestra cómo ajustar el tamaño del papel, la orientación, los márgenes, junto con otras configuraciones para una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | La distancia (en puntos) entre el borde izquierdo de la página y el límite izquierdo del texto del cuerpo. |

### setLineNumberCountBy(int value) {#setLineNumberCountBy-int}
```
public void setLineNumberCountBy(int value)
```


Establece el incremento numérico para los números de línea.

 **Examples:** 

Muestra cómo habilitar la numeración de líneas para una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El incremento numérico para los números de línea. |

### setLineNumberDistanceFromText(double value) {#setLineNumberDistanceFromText-double}
```
public void setLineNumberDistanceFromText(double value)
```


Establece la distancia entre el borde derecho de los números de línea y el borde izquierdo del documento.

 **Remarks:** 

Establezca esta propiedad en cero para la distancia automática entre los números de línea y el texto del documento.

 **Examples:** 

Muestra cómo habilitar la numeración de líneas para una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | Distancia entre el borde derecho de los números de línea y el borde izquierdo del documento. |

### setLineNumberRestartMode(int value) {#setLineNumberRestartMode-int}
```
public void setLineNumberRestartMode(int value)
```


Establece la forma en que se numeran las líneas, es decir, si se reinician al comienzo de una nueva página o sección o continúan de forma continua.

 **Examples:** 

Muestra cómo habilitar la numeración de líneas para una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | La forma en que se ejecuta la numeración de líneas, es decir, si se reinicia al comienzo de una nueva página o sección o se ejecuta de forma continua. El valor debe ser uno de los constantes [LineNumberRestartMode](../../com.aspose.words/linenumberrestartmode/). |

### setLineStartingNumber(int value) {#setLineStartingNumber-int}
```
public void setLineStartingNumber(int value)
```


Establece el número de línea inicial.

 **Examples:** 

Muestra cómo habilitar la numeración de líneas para una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El número de línea inicial. |

### setLinesPerPage(int value) {#setLinesPerPage-int}
```
public void setLinesPerPage(int value)
```


Establece el número de líneas por página en la cuadrícula del documento.

 **Remarks:** 

El valor mínimo de la propiedad es 1. El valor máximo depende de la altura de la página y del tamaño de fuente del estilo Normal. El paso mínimo de línea es el 136 % del tamaño de fuente. Por ejemplo, el número máximo de líneas por página de una hoja Letter con márgenes de una pulgada es 39.

Por defecto, la propiedad tiene un valor en el que el paso de línea es 1,5 veces mayor que el tamaño de fuente del estilo Normal.

 **Examples:** 

Muestra cómo especificar un límite para la cantidad de líneas que puede tener cada página.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of lines per page in this section.
 // A large enough font size will push some lines down onto the next page to avoid overlapping characters.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.LINE_GRID);
 builder.getPageSetup().setLinesPerPage(15);

 builder.getParagraphFormat().setSnapToGrid(true);

 for (int i = 0; i < 30; i++)
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

 doc.save(getArtifactsDir() + "PageSetup.LinesPerPage.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El número de líneas por página en la cuadrícula del documento. |

### setMargins(int value) {#setMargins-int}
```
public void setMargins(int value)
```


Establece los [Márgenes](../../com.aspose.words/margins/) predefinidos de la página.

 **Examples:** 

Muestra cuándo recalcular el diseño de página del documento.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Saving a document to PDF, to an image, or printing for the first time will automatically
 // cache the layout of the document within its pages.
 doc.save(getArtifactsDir() + "Document.UpdatePageLayout.1.pdf");

 // Modify the document in some way.
 doc.getStyles().get("Normal").getFont().setSize(6.0);
 doc.getSections().get(0).getPageSetup().setOrientation(Orientation.LANDSCAPE);
 doc.getSections().get(0).getPageSetup().setMargins(Margins.MIRRORED);

 // In the current version of Aspose.Words, modifying the document does not automatically rebuild
 // the cached page layout. If we wish for the cached layout
 // to stay up to date, we will need to update it manually.
 doc.updatePageLayout();

 doc.save(getArtifactsDir() + "Document.UpdatePageLayout.2.pdf");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | Preajuste [Margins](../../com.aspose.words/margins/) de la página. El valor debe ser uno de los constantes [Margins](../../com.aspose.words/margins/). |

### setMultiplePages(int value) {#setMultiplePages-int}
```
public void setMultiplePages(int value)
```


Para documentos de varias páginas, obtiene o establece cómo se imprime o renderiza un documento para que pueda encuadernarse como folleto.

 **Examples:** 

Muestra cómo establecer márgenes de canal.

```

 Document doc = new Document();

 // Insert text that spans several pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 for (int i = 0; i < 6; i++) {
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
             "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
     builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // A gutter adds whitespaces to either the left or right page margin,
 // which makes up for the center folding of pages in a book encroaching on the page's layout.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 // Determine how much space our pages have for text within the margins and then add an amount to pad a margin.
 Assert.assertEquals(468.00d, pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin(), 0.01d);

 pageSetup.setGutter(100.0d);

 // Set the "RtlGutter" property to "true" to place the gutter in a more suitable position for right-to-left text.
 pageSetup.setRtlGutter(true);

 // Set the "MultiplePages" property to "MultiplePagesType.MirrorMargins" to alternate
 // the left/right page side position of margins every page.
 pageSetup.setMultiplePages(MultiplePagesType.MIRROR_MARGINS);

 doc.save(getArtifactsDir() + "PageSetup.Gutter.docx");
 
```

Muestra cómo configurar un documento que puede imprimirse como un pliegue de libro.

```

 Document doc = new Document();

 // Insert text that spans 16 pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("My Booklet:");

 for (int i = 0; i < 15; i++) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.write(MessageFormat.format("Booklet face #{0}", i));
 }

 // Configure the first section's "PageSetup" property to print the document in the form of a book fold.
 // When we print this document on both sides, we can take the pages to stack them
 // and fold them all down the middle at once. The contents of the document will line up into a book fold.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setMultiplePages(MultiplePagesType.BOOK_FOLD_PRINTING);

 // We can only specify the number of sheets in multiples of 4.
 pageSetup.setSheetsPerBooklet(4);

 doc.save(getArtifactsDir() + "PageSetup.Booklet.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor entero correspondiente. El valor debe ser uno de los constantes [MultiplePagesType](../../com.aspose.words/multiplepagestype/). |

### setOddAndEvenPagesHeaderFooter(boolean value) {#setOddAndEvenPagesHeaderFooter-boolean}
```
public void setOddAndEvenPagesHeaderFooter(boolean value)
```


True si el documento tiene encabezados y pies de página diferentes para páginas impares y pares.

 **Remarks:** 

Nota, cambiar esta propiedad afecta a todas las secciones del documento.

 **Examples:** 

Muestra cómo crear encabezados y pies de página en un documento usando DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

Muestra cómo habilitar o deshabilitar los encabezados/pies de página pares.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two types of header/footers.
 // 1 -  The "Primary" header/footer, which appears on every page in the section.
 // We can override the primary header/footer by a first and an even page header/footer.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Primary header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.writeln("Primary footer.");

 // 2 -  The "Even" header/footer, which appears on every even page of this section.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.writeln("Even page header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_EVEN);
 builder.writeln("Even page footer.");

 builder.moveToSection(0);
 builder.writeln("Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 3.");

 // Each section has a "PageSetup" object that specifies page appearance-related properties
 // such as orientation, size, and borders.
 // Set the "OddAndEvenPagesHeaderFooter" property to "true"
 // to display the even page header/footer on even pages.
 // Set the "OddAndEvenPagesHeaderFooter" property to "false"
 // to display the primary header/footer on even pages.
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(oddAndEvenPagesHeaderFooter);

 doc.save(getArtifactsDir() + "PageSetup.OddAndEvenPagesHeaderFooter.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setOrientation(int value) {#setOrientation-int}
```
public void setOrientation(int value)
```


Establece la orientación de la página.

 **Remarks:** 

Cambiar [getOrientation()](../../com.aspose.words/pagesetup/\#getOrientation) / [setOrientation(int)](../../com.aspose.words/pagesetup/\#setOrientation-int) intercambia [getPageWidth()](../../com.aspose.words/pagesetup/\#getPageWidth) / [setPageWidth(double)](../../com.aspose.words/pagesetup/\#setPageWidth-double) y [getPageHeight()](../../com.aspose.words/pagesetup/\#getPageHeight) / [setPageHeight(double)](../../com.aspose.words/pagesetup/\#setPageHeight-double).

 **Examples:** 

Muestra cómo aplicar y revertir la configuración de página a secciones en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

Muestra cómo ajustar el tamaño del papel, la orientación, los márgenes, junto con otras configuraciones para una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | La orientación de la página. El valor debe ser uno de los constantes [Orientation](../../com.aspose.words/orientation/). |

### setOtherPagesTray(int value) {#setOtherPagesTray-int}
```
public void setOtherPagesTray(int value)
```


Establece la bandeja de papel (cajón) que se usará para todas las páginas excepto la primera de una sección. El valor es específico de la implementación (impresora).

 **Examples:** 

Muestra cómo configurar la impresión usando diferentes bandejas de impresora para distintos tamaños de papel.

```

 Document doc = new Document();

 /// Choose the default printer to be used for printing this document.
 PrintService printService = PrintServiceLookup.lookupDefaultPrintService();
 Media[] trays = (Media[]) printService.getSupportedAttributeValues(Media.class, null, null);

 // This is the tray we will use for pages in the "A4" paper size.
 int printerTrayForA4 = trays[0].getValue();
 // This is the tray we will use for pages in the "Letter" paper size.
 int printerTrayForLetter = trays[1].getValue();

 // Modify the PageSettings object of this section to get Microsoft Word to instruct the printer
 // to use one of the trays we identified above, depending on this section's paper size.
 for (Section section : doc.getSections()) {
     if (section.getPageSetup().getPaperSize() == PaperSize.LETTER) {
         section.getPageSetup().setFirstPageTray(printerTrayForLetter);
         section.getPageSetup().setOtherPagesTray(printerTrayForLetter);
     } else if (section.getPageSetup().getPaperSize() == PaperSize.A4) {
         section.getPageSetup().setFirstPageTray(printerTrayForA4);
         section.getPageSetup().setOtherPagesTray(printerTrayForA4);
     }
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | La bandeja de papel (cajón) que se usará para todas las páginas excepto la primera de una sección. |

### setPageHeight(double value) {#setPageHeight-double}
```
public void setPageHeight(double value)
```


Establece la altura de la página en puntos.

 **Examples:** 

Muestra cómo insertar una imagen y usarla como marca de agua.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert the image into the header so that it will be visible on every page.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 Shape shape = builder.insertImage(getImageDir() + "Transparent background logo.png");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);

 // Place the image at the center of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setLeft((builder.getPageSetup().getPageWidth() - shape.getWidth()) / 2.0);
 shape.setTop((builder.getPageSetup().getPageHeight() - shape.getHeight()) / 2.0);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertWatermark.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | La altura de la página en puntos. |

### setPageNumberStyle(int value) {#setPageNumberStyle-int}
```
public void setPageNumberStyle(int value)
```


Establece el formato del número de página.

 **Examples:** 

Muestra cómo configurar la numeración de páginas en una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 3.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("Section 2, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 3.");

 // Move the document builder to the first section's primary header,
 // which every page in that section will display.
 builder.moveToSection(0);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);

 // Insert a PAGE field, which will display the number of the current page.
 builder.write("Page ");
 builder.insertField("PAGE", "");

 // Configure the section to have the page count that PAGE fields display start from 5.
 // Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageStartingNumber(5);
 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);

 // Create another primary header for the second section, with another PAGE field.
 builder.moveToSection(1);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write(" - ");
 builder.insertField("PAGE", "");
 builder.write(" - ");

 // Configure the section to have the page count that PAGE fields display start from 10.
 // Also, configure all PAGE fields to display their page numbers using Arabic numbers.
 pageSetup = doc.getSections().get(1).getPageSetup();
 pageSetup.setPageStartingNumber(10);
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageNumberStyle(NumberStyle.ARABIC);

 doc.save(getArtifactsDir() + "PageSetup.PageNumbering.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El formato del número de página. El valor debe ser uno de los constantes [NumberStyle](../../com.aspose.words/numberstyle/). |

### setPageStartingNumber(int value) {#setPageStartingNumber-int}
```
public void setPageStartingNumber(int value)
```


Establece el número de página inicial de la sección.

 **Remarks:** 

La propiedad [getRestartPageNumbering()](../../com.aspose.words/pagesetup/\#getRestartPageNumbering) / [setRestartPageNumbering(boolean)](../../com.aspose.words/pagesetup/\#setRestartPageNumbering-boolean) , si se establece en false , sobrescribirá la propiedad [getPageStartingNumber()](../../com.aspose.words/pagesetup/\#getPageStartingNumber) / [setPageStartingNumber(int)](../../com.aspose.words/pagesetup/\#setPageStartingNumber-int) para que la numeración de páginas pueda continuar desde la sección anterior.

 **Examples:** 

Muestra cómo configurar la numeración de páginas en una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 3.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("Section 2, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 3.");

 // Move the document builder to the first section's primary header,
 // which every page in that section will display.
 builder.moveToSection(0);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);

 // Insert a PAGE field, which will display the number of the current page.
 builder.write("Page ");
 builder.insertField("PAGE", "");

 // Configure the section to have the page count that PAGE fields display start from 5.
 // Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageStartingNumber(5);
 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);

 // Create another primary header for the second section, with another PAGE field.
 builder.moveToSection(1);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write(" - ");
 builder.insertField("PAGE", "");
 builder.write(" - ");

 // Configure the section to have the page count that PAGE fields display start from 10.
 // Also, configure all PAGE fields to display their page numbers using Arabic numbers.
 pageSetup = doc.getSections().get(1).getPageSetup();
 pageSetup.setPageStartingNumber(10);
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageNumberStyle(NumberStyle.ARABIC);

 doc.save(getArtifactsDir() + "PageSetup.PageNumbering.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El número de página inicial de la sección. |

### setPageWidth(double value) {#setPageWidth-double}
```
public void setPageWidth(double value)
```


Establece el ancho de la página en puntos.

 **Examples:** 

Muestra cómo insertar una imagen y usarla como marca de agua.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert the image into the header so that it will be visible on every page.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 Shape shape = builder.insertImage(getImageDir() + "Transparent background logo.png");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);

 // Place the image at the center of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setLeft((builder.getPageSetup().getPageWidth() - shape.getWidth()) / 2.0);
 shape.setTop((builder.getPageSetup().getPageHeight() - shape.getHeight()) / 2.0);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertWatermark.docx");
 
```

Muestra cómo insertar una imagen flotante y especificar su posición y tamaño.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);

 // Configure the shape's "RelativeHorizontalPosition" property to treat the value of the "Left" property
 // as the shape's horizontal distance, in points, from the left side of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);

 // Set the shape's horizontal distance from the left side of the page to 100.
 shape.setLeft(100.0);

 // Use the "RelativeVerticalPosition" property in a similar way to position the shape 80pt below the top of the page.
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setTop(80.0);

 // Set the shape's height, which will automatically scale the width to preserve dimensions.
 shape.setHeight(125.0);

 Assert.assertEquals(125.0d, shape.getWidth());

 // The "Bottom" and "Right" properties contain the bottom and right edges of the image.
 Assert.assertEquals(shape.getTop() + shape.getHeight(), shape.getBottom());
 Assert.assertEquals(shape.getLeft() + shape.getWidth(), shape.getRight());

 doc.save(getArtifactsDir() + "Image.CreateFloatingPositionSize.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | El ancho de la página en puntos. |

### setPaperSize(int value) {#setPaperSize-int}
```
public void setPaperSize(int value)
```


Establece el tamaño del papel.

 **Remarks:** 

Al establecer esta propiedad actualiza los valores de [getPageWidth()](../../com.aspose.words/pagesetup/\#getPageWidth) / [setPageWidth(double)](../../com.aspose.words/pagesetup/\#setPageWidth-double) y [getPageHeight()](../../com.aspose.words/pagesetup/\#getPageHeight) / [setPageHeight(double)](../../com.aspose.words/pagesetup/\#setPageHeight-double). Establecer este valor a [PaperSize.CUSTOM](../../com.aspose.words/papersize/\#CUSTOM) no cambia los valores existentes.

 **Examples:** 

Muestra cómo ajustar el tamaño del papel, la orientación, los márgenes, junto con otras configuraciones para una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

Muestra cómo establecer tamaños de página.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can change the current page's size to a pre-defined size
 // by using the "PaperSize" property of this section's PageSetup object.
 builder.getPageSetup().setPaperSize(PaperSize.TABLOID);

 Assert.assertEquals(792.0d, builder.getPageSetup().getPageWidth());
 Assert.assertEquals(1224.0d, builder.getPageSetup().getPageHeight());

 builder.writeln(MessageFormat.format("This page is {0}x{1}.", builder.getPageSetup().getPageWidth(), builder.getPageSetup().getPageHeight()));

 // Each section has its own PageSetup object. When we use a document builder to make a new section,
 // that section's PageSetup object inherits all the previous section's PageSetup object's values.
 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);

 Assert.assertEquals(PaperSize.TABLOID, builder.getPageSetup().getPaperSize());

 builder.getPageSetup().setPaperSize(PaperSize.A5);
 builder.writeln(MessageFormat.format("This page is {0}x{1}.", builder.getPageSetup().getPageWidth(), builder.getPageSetup().getPageHeight()));

 Assert.assertEquals(419.55d, builder.getPageSetup().getPageWidth());
 Assert.assertEquals(595.30d, builder.getPageSetup().getPageHeight());

 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);

 // Set a custom size for this section's pages.
 builder.getPageSetup().setPageWidth(620.0);
 builder.getPageSetup().setPageHeight(480.0);

 Assert.assertEquals(PaperSize.CUSTOM, builder.getPageSetup().getPaperSize());

 builder.writeln(MessageFormat.format("This page is {0}x{1}.", builder.getPageSetup().getPageWidth(), builder.getPageSetup().getPageHeight()));

 doc.save(getArtifactsDir() + "PageSetup.PaperSizes.docx");
 
```

Muestra cómo establecer el tamaño de papel de JisB4 o JisB5.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();
 // Set the paper size to JisB4 (257x364mm).
 pageSetup.setPaperSize(PaperSize.JIS_B_4);
 // Alternatively, set the paper size to JisB5. (182x257mm).
 pageSetup.setPaperSize(PaperSize.JIS_B_5);
 
```

Muestra cómo construir un documento Aspose.Words manualmente.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El tamaño del papel. El valor debe ser uno de los constantes [PaperSize](../../com.aspose.words/papersize/). |

### setRestartPageNumbering(boolean value) {#setRestartPageNumbering-boolean}
```
public void setRestartPageNumbering(boolean value)
```


True si la numeración de páginas se reinicia al comienzo de la sección.

 **Remarks:** 

Si se establece en false , la propiedad [getRestartPageNumbering()](../../com.aspose.words/pagesetup/\#getRestartPageNumbering) / [setRestartPageNumbering(boolean)](../../com.aspose.words/pagesetup/\#setRestartPageNumbering-boolean) sobrescribirá la propiedad [getPageStartingNumber()](../../com.aspose.words/pagesetup/\#getPageStartingNumber) / [setPageStartingNumber(int)](../../com.aspose.words/pagesetup/\#setPageStartingNumber-int) para que la numeración de páginas pueda continuar desde la sección anterior.

 **Examples:** 

Muestra cómo configurar la numeración de páginas en una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 3.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("Section 2, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 3.");

 // Move the document builder to the first section's primary header,
 // which every page in that section will display.
 builder.moveToSection(0);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);

 // Insert a PAGE field, which will display the number of the current page.
 builder.write("Page ");
 builder.insertField("PAGE", "");

 // Configure the section to have the page count that PAGE fields display start from 5.
 // Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageStartingNumber(5);
 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);

 // Create another primary header for the second section, with another PAGE field.
 builder.moveToSection(1);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write(" - ");
 builder.insertField("PAGE", "");
 builder.write(" - ");

 // Configure the section to have the page count that PAGE fields display start from 10.
 // Also, configure all PAGE fields to display their page numbers using Arabic numbers.
 pageSetup = doc.getSections().get(1).getPageSetup();
 pageSetup.setPageStartingNumber(10);
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageNumberStyle(NumberStyle.ARABIC);

 doc.save(getArtifactsDir() + "PageSetup.PageNumbering.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setRightMargin(double value) {#setRightMargin-double}
```
public void setRightMargin(double value)
```


Establece la distancia (en puntos) entre el borde derecho de la página y el límite derecho del texto del cuerpo.

 **Examples:** 

Muestra cómo ajustar el tamaño del papel, la orientación, los márgenes, junto con otras configuraciones para una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | La distancia (en puntos) entre el borde derecho de la página y el límite derecho del texto del cuerpo. |

### setRtlGutter(boolean value) {#setRtlGutter-boolean}
```
public void setRtlGutter(boolean value)
```


Establece si Microsoft Word usa canaletas para la sección según un idioma de derecha a izquierda o de izquierda a derecha.

 **Examples:** 

Muestra cómo establecer márgenes de canal.

```

 Document doc = new Document();

 // Insert text that spans several pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 for (int i = 0; i < 6; i++) {
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
             "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
     builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // A gutter adds whitespaces to either the left or right page margin,
 // which makes up for the center folding of pages in a book encroaching on the page's layout.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 // Determine how much space our pages have for text within the margins and then add an amount to pad a margin.
 Assert.assertEquals(468.00d, pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin(), 0.01d);

 pageSetup.setGutter(100.0d);

 // Set the "RtlGutter" property to "true" to place the gutter in a more suitable position for right-to-left text.
 pageSetup.setRtlGutter(true);

 // Set the "MultiplePages" property to "MultiplePagesType.MirrorMargins" to alternate
 // the left/right page side position of margins every page.
 pageSetup.setMultiplePages(MultiplePagesType.MIRROR_MARGINS);

 doc.save(getArtifactsDir() + "PageSetup.Gutter.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Si Microsoft Word usa canaletas para la sección según un idioma de derecha a izquierda o de izquierda a derecha. |

### setSectionStart(int value) {#setSectionStart-int}
```
public void setSectionStart(int value)
```


Establece el tipo de salto de sección para el objeto especificado.

 **Examples:** 

Muestra cómo especificar cómo una nueva sección se separa de la anterior.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("This text is in section 1.");

 // Section break types determine how a new section separates itself from the previous section.
 // Below are five types of section breaks.
 // 1 -  Starts the next section on a new page:
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("This text is in section 2.");

 Assert.assertEquals(SectionStart.NEW_PAGE, doc.getSections().get(1).getPageSetup().getSectionStart());

 // 2 -  Starts the next section on the current page:
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.writeln("This text is in section 3.");

 Assert.assertEquals(SectionStart.CONTINUOUS, doc.getSections().get(2).getPageSetup().getSectionStart());

 // 3 -  Starts the next section on a new even page:
 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);
 builder.writeln("This text is in section 4.");

 Assert.assertEquals(SectionStart.EVEN_PAGE, doc.getSections().get(3).getPageSetup().getSectionStart());

 // 4 -  Starts the next section on a new odd page:
 builder.insertBreak(BreakType.SECTION_BREAK_ODD_PAGE);
 builder.writeln("This text is in section 5.");

 Assert.assertEquals(SectionStart.ODD_PAGE, doc.getSections().get(4).getPageSetup().getSectionStart());

 // 5 -  Starts the next section on a new column:
 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setCount(2);

 builder.insertBreak(BreakType.SECTION_BREAK_NEW_COLUMN);
 builder.writeln("This text is in section 6.");

 Assert.assertEquals(SectionStart.NEW_COLUMN, doc.getSections().get(5).getPageSetup().getSectionStart());

 doc.save(getArtifactsDir() + "PageSetup.SetSectionStart.docx");
 
```

Muestra cómo construir un documento Aspose.Words manualmente.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El tipo de salto de sección para el objeto especificado. El valor debe ser uno de los constantes [SectionStart](../../com.aspose.words/sectionstart/). |

### setSheetsPerBooklet(int value) {#setSheetsPerBooklet-int}
```
public void setSheetsPerBooklet(int value)
```


Establece el número de páginas que se incluirán en cada folleto.

 **Examples:** 

Muestra cómo configurar un documento que puede imprimirse como un pliegue de libro.

```

 Document doc = new Document();

 // Insert text that spans 16 pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("My Booklet:");

 for (int i = 0; i < 15; i++) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.write(MessageFormat.format("Booklet face #{0}", i));
 }

 // Configure the first section's "PageSetup" property to print the document in the form of a book fold.
 // When we print this document on both sides, we can take the pages to stack them
 // and fold them all down the middle at once. The contents of the document will line up into a book fold.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setMultiplePages(MultiplePagesType.BOOK_FOLD_PRINTING);

 // We can only specify the number of sheets in multiples of 4.
 pageSetup.setSheetsPerBooklet(4);

 doc.save(getArtifactsDir() + "PageSetup.Booklet.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El número de páginas que se incluirán en cada folleto. |

### setSuppressEndnotes(boolean value) {#setSuppressEndnotes-boolean}
```
public void setSuppressEndnotes(boolean value)
```


True si las notas al final se imprimen al final de la siguiente sección que no suprime notas al final. Las notas al final suprimidas se imprimen antes de las notas al final en esa sección.

 **Examples:** 

Muestra cómo almacenar notas al final al final de cada sección y modificar sus posiciones.

```

 public void suppressEndnotes() throws Exception {
     Document doc = new Document();
     doc.removeAllChildren();

     // By default, a document compiles all endnotes at its end.
     Assert.assertEquals(EndnotePosition.END_OF_DOCUMENT, doc.getEndnoteOptions().getPosition());

     // We use the "Position" property of the document's "EndnoteOptions" object
     // to collect endnotes at the end of each section instead.
     doc.getEndnoteOptions().setPosition(EndnotePosition.END_OF_SECTION);

     insertSectionWithEndnote(doc, "Section 1", "Endnote 1, will stay in section 1");
     insertSectionWithEndnote(doc, "Section 2", "Endnote 2, will be pushed down to section 3");
     insertSectionWithEndnote(doc, "Section 3", "Endnote 3, will stay in section 3");

     // While getting sections to display their respective endnotes, we can set the "SuppressEndnotes" flag
     // of a section's "PageSetup" object to "true" to revert to the default behavior and pass its endnotes
     // onto the next section.
     PageSetup pageSetup = doc.getSections().get(1).getPageSetup();
     pageSetup.setSuppressEndnotes(true);

     doc.save(getArtifactsDir() + "PageSetup.SuppressEndnotes.docx");
 }

 /// 
 /// Append a section with text and an endnote to a document.
 /// 
 private static void insertSectionWithEndnote(Document doc, String sectionBodyText, String endnoteText) {
     Section section = new Section(doc);

     doc.appendChild(section);

     Body body = new Body(doc);
     section.appendChild(body);

     Assert.assertEquals(body.getParentNode(), section);

     Paragraph para = new Paragraph(doc);
     body.appendChild(para);

     Assert.assertEquals(para.getParentNode(), body);

     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.moveTo(para);
     builder.write(sectionBodyText);
     builder.insertFootnote(FootnoteType.ENDNOTE, endnoteText);
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setTextOrientation(int value) {#setTextOrientation-int}
```
public void setTextOrientation(int value)
```


Permite especificar [getTextOrientation()](../../com.aspose.words/pagesetup/\#getTextOrientation) / [setTextOrientation(int)](../../com.aspose.words/pagesetup/\#setTextOrientation-int) para toda la página. El valor predeterminado es [TextOrientation.HORIZONTAL](../../com.aspose.words/textorientation/\#HORIZONTAL)

 **Remarks:** 

Esta propiedad solo es compatible con los formatos nativos de MS Word DOCX, WML, RTF y DOC.

 **Examples:** 

Muestra cómo establecer la orientación del texto.

```

 Document doc = new Document();

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Set the "TextOrientation" property to "TextOrientation.Upward" to rotate all the text 90 degrees
 // to the right so that all left-to-right text now goes top-to-bottom.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setTextOrientation(TextOrientation.UPWARD);

 doc.save(getArtifactsDir() + "PageSetup.SetTextOrientation.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor int correspondiente. El valor debe ser uno de los constantes [TextOrientation](../../com.aspose.words/textorientation/). |

### setTopMargin(double value) {#setTopMargin-double}
```
public void setTopMargin(double value)
```


Establece la distancia (en puntos) entre el borde superior de la página y el límite superior del texto del cuerpo.

 **Examples:** 

Muestra cómo ajustar el tamaño del papel, la orientación, los márgenes, junto con otras configuraciones para una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | La distancia (en puntos) entre el borde superior de la página y el límite superior del texto del cuerpo. |

### setVerticalAlignment(int value) {#setVerticalAlignment-int}
```
public void setVerticalAlignment(int value)
```


Establece la alineación vertical del texto en cada página de un documento o sección.

 **Examples:** 

Muestra cómo aplicar y revertir la configuración de página a secciones en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | La alineación vertical del texto en cada página de un documento o sección. El valor debe ser uno de los constantes [PageVerticalAlignment](../../com.aspose.words/pageverticalalignment/). |

