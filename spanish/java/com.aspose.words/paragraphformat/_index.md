---
title: "ParagraphFormat"
linktitle: "ParagraphFormat"
second_title: "Aspose.Words para Java"
description: "Representa todo el formato de un párrafo en Java."
type: docs
weight: 525
url: /es/java/com.aspose.words/paragraphformat/
---

**Inheritance:**
java.lang.Object
```
public class ParagraphFormat
```

Representa todo el formato de un párrafo.

Para obtener más información, visite el artículo de documentación [ Working with Paragraphs ][Working with Paragraphs].

 **Examples:** 

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


[Working with Paragraphs]: https://docs.aspose.com/words/java/working-with-paragraphs/
## Métodos

| Método | Descripción |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Restablece el formato de párrafo predeterminado. |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int) |  |
| [fetchInheritedShadingAttr(int key)](#fetchInheritedShadingAttr-int) |  |
| [getAddSpaceBetweenFarEastAndAlpha()](#getAddSpaceBetweenFarEastAndAlpha) | Obtiene una bandera que indica si el espaciado entre caracteres se ajusta automáticamente entre regiones de texto latino y regiones de texto de Asia Oriental en el párrafo actual. |
| [getAddSpaceBetweenFarEastAndDigit()](#getAddSpaceBetweenFarEastAndDigit) | Obtiene una bandera que indica si el espaciado entre caracteres se ajusta automáticamente entre regiones de números y regiones de texto de Asia Oriental en el párrafo actual. |
| [getAlignment()](#getAlignment) | Obtiene la alineación del texto para el párrafo. |
| [getBaselineAlignment()](#getBaselineAlignment) | Obtiene la posición vertical de las fuentes en una línea. |
| [getBidi()](#getBidi) | Obtiene si este es un párrafo de derecha a izquierda. |
| [getBorders()](#getBorders) | Obtiene la colección de bordes del párrafo. |
| [getCharacterUnitFirstLineIndent()](#getCharacterUnitFirstLineIndent) | Obtiene el valor (en caracteres) para la sangría de primera línea o colgante. |
| [getCharacterUnitLeftIndent()](#getCharacterUnitLeftIndent) | Obtiene el valor de sangría izquierda (en caracteres) para los párrafos especificados. |
| [getCharacterUnitRightIndent()](#getCharacterUnitRightIndent) | Obtiene el valor de sangría derecha (en caracteres) para los párrafos especificados. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int) |  |
| [getDropCapPosition()](#getDropCapPosition) | Obtiene la posición para un texto de letra capitular. |
| [getFarEastLineBreakControl()](#getFarEastLineBreakControl) | Obtiene una bandera que indica si se aplican las reglas de salto de línea de Asia Oriental al párrafo actual. |
| [getFirstLineIndent()](#getFirstLineIndent) | Obtiene el valor (en puntos) para una sangría de primera línea o colgante. |
| [getHangingPunctuation()](#getHangingPunctuation) | Obtiene una bandera que indica si la puntuación colgante está habilitada para el párrafo actual. |
| [getKeepTogether()](#getKeepTogether) | Verdadero si todas las líneas del párrafo deben permanecer en la misma página. |
| [getKeepWithNext()](#getKeepWithNext) | Verdadero si el párrafo debe permanecer en la misma página que el párrafo que lo sigue. |
| [getLeftIndent()](#getLeftIndent) | Obtiene el valor (en puntos) que representa la sangría izquierda del párrafo. |
| [getLineSpacing()](#getLineSpacing) | Obtiene el interlineado (en puntos) del párrafo. |
| [getLineSpacingRule()](#getLineSpacingRule) | Obtiene el interlineado del párrafo. |
| [getLineUnitAfter()](#getLineUnitAfter) | Obtiene la cantidad de espacio (en líneas de cuadrícula) después de los párrafos. |
| [getLineUnitBefore()](#getLineUnitBefore) | Obtiene la cantidad de espacio (en líneas de cuadrícula) antes de los párrafos. |
| [getLinesToDrop()](#getLinesToDrop) | Obtiene el número de líneas del texto del párrafo usadas para calcular la altura de la letra capitular. |
| [getMirrorIndents()](#getMirrorIndents) | Obtiene una bandera que indica si las sangrías izquierda y derecha tienen la misma anchura. |
| [getNoSpaceBetweenParagraphsOfSameStyle()](#getNoSpaceBetweenParagraphsOfSameStyle) | Cuando verdadero, [getSpaceBefore()](../../com.aspose.words/paragraphformat/\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat/\#setSpaceBefore-double) y [getSpaceAfter()](../../com.aspose.words/paragraphformat/\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat/\#setSpaceAfter-double) serán ignorados entre los párrafos del mismo estilo. |
| [getOutlineLevel()](#getOutlineLevel) | Especifica el nivel de esquema del párrafo en el documento. |
| [getPageBreakBefore()](#getPageBreakBefore) | Verdadero si se fuerza un salto de página antes del párrafo. |
| [getRightIndent()](#getRightIndent) | Obtiene el valor (en puntos) que representa la sangría derecha del párrafo. |
| [getShading()](#getShading) | Devuelve un objeto [Shading](../../com.aspose.words/shading/) que se refiere al formato de sombreado del párrafo. |
| [getSnapToGrid()](#getSnapToGrid) | Especifica si el párrafo actual debe usar la configuración de líneas de cuadrícula del documento por página al organizar el contenido en el párrafo. |
| [getSpaceAfter()](#getSpaceAfter) | Obtiene la cantidad de espacio (en puntos) después del párrafo. |
| [getSpaceAfterAuto()](#getSpaceAfterAuto) | Verdadero si la cantidad de espacio después del párrafo se establece automáticamente. |
| [getSpaceBefore()](#getSpaceBefore) | Obtiene la cantidad de espacio (en puntos) antes del párrafo. |
| [getSpaceBeforeAuto()](#getSpaceBeforeAuto) | Verdadero si la cantidad de espacio antes del párrafo se establece automáticamente. |
| [getStyle()](#getStyle) | Obtiene el estilo de párrafo aplicado a este formato. |
| [getStyleIdentifier()](#getStyleIdentifier) | Obtiene el identificador de estilo independiente de la configuración regional del estilo de párrafo aplicado a este formato. |
| [getStyleName()](#getStyleName) | Obtiene el nombre del estilo de párrafo aplicado a este formato. |
| [getSuppressAutoHyphens()](#getSuppressAutoHyphens) | Especifica si el párrafo actual debe estar exento de cualquier guionado que se aplique en la configuración del documento. |
| [getSuppressLineNumbers()](#getSuppressLineNumbers) | Especifica si las líneas del párrafo actual deben estar exentas de la numeración de líneas que se aplica en la sección principal. |
| [getTabStops()](#getTabStops) | Obtiene la colección de tabuladores personalizados definidos para este objeto. |
| [getWidowControl()](#getWidowControl) | Verdadero si la primera y la última línea del párrafo deben permanecer en la misma página que el resto del párrafo. |
| [getWordWrap()](#getWordWrap) | Si esta propiedad es false, el texto latino en medio de una palabra puede ajustarse para el párrafo actual. |
| [isHeading()](#isHeading) | Verdadero cuando el estilo de párrafo es uno de los estilos de encabezado incorporados. |
| [isListItem()](#isListItem) | Verdadero cuando el párrafo es un elemento de una lista con viñetas o numerada. |
| [setAddSpaceBetweenFarEastAndAlpha(boolean value)](#setAddSpaceBetweenFarEastAndAlpha-boolean) | Establece una bandera que indica si el espaciado entre caracteres se ajusta automáticamente entre regiones de texto latino y regiones de texto de Asia Oriental en el párrafo actual. |
| [setAddSpaceBetweenFarEastAndDigit(boolean value)](#setAddSpaceBetweenFarEastAndDigit-boolean) | Establece una bandera que indica si el espaciado entre caracteres se ajusta automáticamente entre regiones de números y regiones de texto de Asia Oriental en el párrafo actual. |
| [setAlignment(int value)](#setAlignment-int) | Establece la alineación del texto para el párrafo. |
| [setBaselineAlignment(int value)](#setBaselineAlignment-int) | Establece la posición vertical de las fuentes en una línea. |
| [setBidi(boolean value)](#setBidi-boolean) | Establece si este es un párrafo de derecha a izquierda. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object) |  |
| [setCharacterUnitFirstLineIndent(double value)](#setCharacterUnitFirstLineIndent-double) | Establece el valor (en caracteres) para la sangría de primera línea o colgante. |
| [setCharacterUnitLeftIndent(double value)](#setCharacterUnitLeftIndent-double) | Establece el valor de sangría izquierda (en caracteres) para los párrafos especificados. |
| [setCharacterUnitRightIndent(double value)](#setCharacterUnitRightIndent-double) | Establece el valor de sangría derecha (en caracteres) para los párrafos especificados. |
| [setDropCapPosition(int value)](#setDropCapPosition-int) | Establece la posición para un texto de letra capitular. |
| [setFarEastLineBreakControl(boolean value)](#setFarEastLineBreakControl-boolean) | Establece una bandera que indica si se aplican las reglas de salto de línea de Asia Oriental al párrafo actual. |
| [setFirstLineIndent(double value)](#setFirstLineIndent-double) | Establece el valor (en puntos) para una primera línea o sangría colgante. |
| [setHangingPunctuation(boolean value)](#setHangingPunctuation-boolean) | Establece una bandera que indica si la puntuación colgante está habilitada para el párrafo actual. |
| [setKeepTogether(boolean value)](#setKeepTogether-boolean) | Verdadero si todas las líneas del párrafo deben permanecer en la misma página. |
| [setKeepWithNext(boolean value)](#setKeepWithNext-boolean) | Verdadero si el párrafo debe permanecer en la misma página que el párrafo que lo sigue. |
| [setLeftIndent(double value)](#setLeftIndent-double) | Establece el valor (en puntos) que representa la sangría izquierda para el párrafo. |
| [setLineSpacing(double value)](#setLineSpacing-double) | Establece el interlineado (en puntos) para el párrafo. |
| [setLineSpacingRule(int value)](#setLineSpacingRule-int) | Establece el interlineado para el párrafo. |
| [setLineUnitAfter(double value)](#setLineUnitAfter-double) | Establece la cantidad de espacio (en líneas de cuadrícula) después de los párrafos. |
| [setLineUnitBefore(double value)](#setLineUnitBefore-double) | Establece la cantidad de espacio (en líneas de cuadrícula) antes de los párrafos. |
| [setLinesToDrop(int value)](#setLinesToDrop-int) | Establece el número de líneas del texto del párrafo usadas para calcular la altura de la letra capitular. |
| [setMirrorIndents(boolean value)](#setMirrorIndents-boolean) | Establece una bandera que indica si las sangrías izquierda y derecha tienen la misma anchura. |
| [setNoSpaceBetweenParagraphsOfSameStyle(boolean value)](#setNoSpaceBetweenParagraphsOfSameStyle-boolean) | Cuando verdadero, [getSpaceBefore()](../../com.aspose.words/paragraphformat/\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat/\#setSpaceBefore-double) y [getSpaceAfter()](../../com.aspose.words/paragraphformat/\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat/\#setSpaceAfter-double) serán ignorados entre los párrafos del mismo estilo. |
| [setOutlineLevel(int value)](#setOutlineLevel-int) | Especifica el nivel de esquema del párrafo en el documento. |
| [setPageBreakBefore(boolean value)](#setPageBreakBefore-boolean) | Verdadero si se fuerza un salto de página antes del párrafo. |
| [setRightIndent(double value)](#setRightIndent-double) | Establece el valor (en puntos) que representa la sangría derecha para el párrafo. |
| [setSnapToGrid(boolean value)](#setSnapToGrid-boolean) | Especifica si el párrafo actual debe usar la configuración de líneas de cuadrícula del documento por página al organizar el contenido en el párrafo. |
| [setSpaceAfter(double value)](#setSpaceAfter-double) | Establece la cantidad de espacio (en puntos) después del párrafo. |
| [setSpaceAfterAuto(boolean value)](#setSpaceAfterAuto-boolean) | Verdadero si la cantidad de espacio después del párrafo se establece automáticamente. |
| [setSpaceBefore(double value)](#setSpaceBefore-double) | Establece la cantidad de espacio (en puntos) antes del párrafo. |
| [setSpaceBeforeAuto(boolean value)](#setSpaceBeforeAuto-boolean) | Verdadero si la cantidad de espacio antes del párrafo se establece automáticamente. |
| [setStyle(Style value)](#setStyle-com.aspose.words.Style) | Establece el estilo de párrafo aplicado a este formato. |
| [setStyleIdentifier(int value)](#setStyleIdentifier-int) | Establece el identificador de estilo independiente de la configuración regional del estilo de párrafo aplicado a este formato. |
| [setStyleName(String value)](#setStyleName-java.lang.String) | Establece el nombre del estilo de párrafo aplicado a este formato. |
| [setSuppressAutoHyphens(boolean value)](#setSuppressAutoHyphens-boolean) | Especifica si el párrafo actual debe estar exento de cualquier guionado que se aplique en la configuración del documento. |
| [setSuppressLineNumbers(boolean value)](#setSuppressLineNumbers-boolean) | Especifica si las líneas del párrafo actual deben estar exentas de la numeración de líneas que se aplica en la sección principal. |
| [setWidowControl(boolean value)](#setWidowControl-boolean) | Verdadero si la primera y la última línea del párrafo deben permanecer en la misma página que el resto del párrafo. |
| [setWordWrap(boolean value)](#setWordWrap-boolean) | Si esta propiedad es false, el texto latino en medio de una palabra puede ajustarse para el párrafo actual. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Restablece el formato de párrafo predeterminado.

 **Remarks:** 

El formato de párrafo predeterminado es el estilo Normal, alineado a la izquierda, sin sangría, sin espaciado, sin bordes y sin sombreado.

 **Examples:** 

Muestra cómo anidar una lista dentro de otra lista.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Create an outline list for the headings.
 List outlineList = doc.getLists().add(ListTemplate.OUTLINE_NUMBERS);
 builder.getListFormat().setList(outlineList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("This is my Chapter 1");

 // Create a numbered list.
 List numberedList = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);
 builder.getListFormat().setList(numberedList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.NORMAL);
 builder.writeln("Numbered list item 1.");

 // Every paragraph that comprises a list will have this flag.
 Assert.assertTrue(builder.getCurrentParagraph().isListItem());
 Assert.assertTrue(builder.getParagraphFormat().isListItem());

 // Create a bulleted list.
 List bulletedList = doc.getLists().add(ListTemplate.BULLET_DEFAULT);
 builder.getListFormat().setList(bulletedList);
 builder.getParagraphFormat().setLeftIndent(72.0);
 builder.writeln("Bulleted list item 1.");
 builder.writeln("Bulleted list item 2.");
 builder.getParagraphFormat().clearFormatting();

 // Revert to the numbered list.
 builder.getListFormat().setList(numberedList);
 builder.writeln("Numbered list item 2.");
 builder.writeln("Numbered list item 3.");

 // Revert to the outline list.
 builder.getListFormat().setList(outlineList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("This is my Chapter 2");

 builder.getParagraphFormat().clearFormatting();

 builder.getDocument().save(getArtifactsDir() + "Lists.NestedLists.docx");
 
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
### getAddSpaceBetweenFarEastAndAlpha() {#getAddSpaceBetweenFarEastAndAlpha}
```
public boolean getAddSpaceBetweenFarEastAndAlpha()
```


Obtiene una bandera que indica si el espaciado entre caracteres se ajusta automáticamente entre regiones de texto latino y regiones de texto de Asia Oriental en el párrafo actual.

 **Examples:** 

Muestra cómo insertar un párrafo en el documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Arial");
 font.setUnderline(Underline.DASH);

 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setFirstLineIndent(8.0);
 paragraphFormat.setAlignment(ParagraphAlignment.JUSTIFY);
 paragraphFormat.setAddSpaceBetweenFarEastAndAlpha(true);
 paragraphFormat.setAddSpaceBetweenFarEastAndDigit(true);
 paragraphFormat.setKeepTogether(true);

 // The "Writeln" method ends the paragraph after appending text
 // and then starts a new line, adding a new paragraph.
 builder.writeln("Hello world!");

 Assert.assertTrue(builder.getCurrentParagraph().isEndOfDocument());
 
```

**Returns:**
boolean - Un indicador que muestra si el espaciado entre caracteres se ajusta automáticamente entre regiones de texto latino y regiones de texto de Asia Oriental en el párrafo actual.
### getAddSpaceBetweenFarEastAndDigit() {#getAddSpaceBetweenFarEastAndDigit}
```
public boolean getAddSpaceBetweenFarEastAndDigit()
```


Obtiene una bandera que indica si el espaciado entre caracteres se ajusta automáticamente entre regiones de números y regiones de texto de Asia Oriental en el párrafo actual.

 **Examples:** 

Muestra cómo insertar un párrafo en el documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Arial");
 font.setUnderline(Underline.DASH);

 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setFirstLineIndent(8.0);
 paragraphFormat.setAlignment(ParagraphAlignment.JUSTIFY);
 paragraphFormat.setAddSpaceBetweenFarEastAndAlpha(true);
 paragraphFormat.setAddSpaceBetweenFarEastAndDigit(true);
 paragraphFormat.setKeepTogether(true);

 // The "Writeln" method ends the paragraph after appending text
 // and then starts a new line, adding a new paragraph.
 builder.writeln("Hello world!");

 Assert.assertTrue(builder.getCurrentParagraph().isEndOfDocument());
 
```

**Returns:**
boolean - Un indicador que muestra si el espaciado entre caracteres se ajusta automáticamente entre regiones de números y regiones de texto de Asia Oriental en el párrafo actual.
### getAlignment() {#getAlignment}
```
public int getAlignment()
```


Obtiene la alineación del texto para el párrafo.

 **Examples:** 

Muestra cómo insertar un párrafo en el documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Arial");
 font.setUnderline(Underline.DASH);

 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setFirstLineIndent(8.0);
 paragraphFormat.setAlignment(ParagraphAlignment.JUSTIFY);
 paragraphFormat.setAddSpaceBetweenFarEastAndAlpha(true);
 paragraphFormat.setAddSpaceBetweenFarEastAndDigit(true);
 paragraphFormat.setKeepTogether(true);

 // The "Writeln" method ends the paragraph after appending text
 // and then starts a new line, adding a new paragraph.
 builder.writeln("Hello world!");

 Assert.assertTrue(builder.getCurrentParagraph().isEndOfDocument());
 
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
int - Alineación del texto para el párrafo. El valor devuelto es una de las constantes de [ParagraphAlignment](../../com.aspose.words/paragraphalignment/).
### getBaselineAlignment() {#getBaselineAlignment}
```
public int getBaselineAlignment()
```


Obtiene la posición vertical de las fuentes en una línea.

 **Examples:** 

Muestra cómo establecer la posición vertical de las fuentes en una línea.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat();
 if (format.getBaselineAlignment() == BaselineAlignment.AUTO)
 {
     format.setBaselineAlignment(BaselineAlignment.TOP);
 }

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphBaselineAlignment.docx");
 
```

**Returns:**
int - Posición vertical de las fuentes en una línea. El valor devuelto es una de las constantes de [BaselineAlignment](../../com.aspose.words/baselinealignment/).
### getBidi() {#getBidi}
```
public boolean getBidi()
```


Obtiene si este es un párrafo de derecha a izquierda.

 **Remarks:** 

Cuando  true , las ejecuciones y otros objetos en línea en este párrafo se disponen de derecha a izquierda.

 **Examples:** 

Muestra cómo crear listas compatibles con idiomas de derecha a izquierda usando campos BIDIOUTLINE.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // The BIDIOUTLINE field numbers paragraphs like the AUTONUM/LISTNUM fields,
 // but is only visible when a right-to-left editing language is enabled, such as Hebrew or Arabic.
 // The following field will display ".1", the RTL equivalent of list number "1.".
 FieldBidiOutline field = (FieldBidiOutline) builder.insertField(FieldType.FIELD_BIDI_OUTLINE, true);
 builder.writeln("\u05e9\u05dc\u05d5\u05dd");

 Assert.assertEquals(" BIDIOUTLINE ", field.getFieldCode());

 // Add two more BIDIOUTLINE fields, which will display ".2" and ".3".
 builder.insertField(FieldType.FIELD_BIDI_OUTLINE, true);
 builder.writeln("\u05e9\u05dc\u05d5\u05dd");
 builder.insertField(FieldType.FIELD_BIDI_OUTLINE, true);
 builder.writeln("\u05e9\u05dc\u05d5\u05dd");

 // Set the horizontal text alignment for every paragraph in the document to RTL.
 for (Paragraph para : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     para.getParagraphFormat().setBidi(true);
 }

 // If we enable a right-to-left editing language in Microsoft Word, our fields will display numbers.
 // Otherwise, they will display "###".
 doc.save(getArtifactsDir() + "Field.BIDIOUTLINE.docx");
 
```

Muestra cómo detectar la dirección del texto en un documento de texto plano.

```

 // Create a "TxtLoadOptions" object, which we can pass to a document's constructor
 // to modify how we load a plaintext document.
 TxtLoadOptions loadOptions = new TxtLoadOptions();

 // Set the "DocumentDirection" property to "DocumentDirection.Auto" automatically detects
 // the direction of every paragraph of text that Aspose.Words loads from plaintext.
 // Each paragraph's "Bidi" property will store its direction.
 loadOptions.setDocumentDirection(DocumentDirection.AUTO);

 // Detect Hebrew text as right-to-left.
 Document doc = new Document(getMyDir() + "Hebrew text.txt", loadOptions);

 Assert.assertTrue(doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBidi());

 // Detect English text as right-to-left.
 doc = new Document(getMyDir() + "English text.txt", loadOptions);

 Assert.assertFalse(doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBidi());
 
```

**Returns:**
boolean - Indica si este es un párrafo de derecha a izquierda.
### getBorders() {#getBorders}
```
public BorderCollection getBorders()
```


Obtiene la colección de bordes del párrafo.

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
[BorderCollection](../../com.aspose.words/bordercollection/) - Collection of borders of the paragraph.
### getCharacterUnitFirstLineIndent() {#getCharacterUnitFirstLineIndent}
```
public double getCharacterUnitFirstLineIndent()
```


Obtiene el valor (en caracteres) para la sangría de primera línea o colgante.

Use valores positivos para establecer la sangría de la primera línea y valores negativos para establecer la sangría colgante.

 **Examples:** 

Muestra cómo cambiar el espaciado y las sangrías del párrafo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();

 // Below are five different spacing options, along with the properties that their configuration indirectly affects.
 // 1 -  Left indent:
 Assert.assertEquals(format.getLeftIndent(), 0.0d);

 format.setCharacterUnitLeftIndent(10.0);

 Assert.assertEquals(format.getLeftIndent(), 120.0d);

 // 2 -  Right indent:
 Assert.assertEquals(format.getRightIndent(), 0.0d);

 format.setCharacterUnitRightIndent(-5.5);

 Assert.assertEquals(format.getRightIndent(), -66.0d);

 // 3 -  Hanging indent:
 Assert.assertEquals(format.getFirstLineIndent(), 0.0d);

 format.setCharacterUnitFirstLineIndent(20.3);

 Assert.assertEquals(format.getFirstLineIndent(), 243.59d, 0.1d);

 // 4 -  Line spacing before paragraphs:
 Assert.assertEquals(format.getSpaceBefore(), 0.0d);

 format.setLineUnitBefore(5.1);

 Assert.assertEquals(format.getSpaceBefore(), 61.1d, 0.1d);

 // 5 -  Line spacing after paragraphs:
 Assert.assertEquals(format.getSpaceAfter(), 0.0d);

 format.setLineUnitAfter(10.9);

 Assert.assertEquals(format.getSpaceAfter(), 130.8d, 0.1d);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5" +
         "\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863");
 
```

**Returns:**
double - El valor (en caracteres) para la sangría de la primera línea o colgante.
### getCharacterUnitLeftIndent() {#getCharacterUnitLeftIndent}
```
public double getCharacterUnitLeftIndent()
```


Obtiene el valor de sangría izquierda (en caracteres) para los párrafos especificados.

 **Examples:** 

Muestra cómo cambiar el espaciado y las sangrías del párrafo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();

 // Below are five different spacing options, along with the properties that their configuration indirectly affects.
 // 1 -  Left indent:
 Assert.assertEquals(format.getLeftIndent(), 0.0d);

 format.setCharacterUnitLeftIndent(10.0);

 Assert.assertEquals(format.getLeftIndent(), 120.0d);

 // 2 -  Right indent:
 Assert.assertEquals(format.getRightIndent(), 0.0d);

 format.setCharacterUnitRightIndent(-5.5);

 Assert.assertEquals(format.getRightIndent(), -66.0d);

 // 3 -  Hanging indent:
 Assert.assertEquals(format.getFirstLineIndent(), 0.0d);

 format.setCharacterUnitFirstLineIndent(20.3);

 Assert.assertEquals(format.getFirstLineIndent(), 243.59d, 0.1d);

 // 4 -  Line spacing before paragraphs:
 Assert.assertEquals(format.getSpaceBefore(), 0.0d);

 format.setLineUnitBefore(5.1);

 Assert.assertEquals(format.getSpaceBefore(), 61.1d, 0.1d);

 // 5 -  Line spacing after paragraphs:
 Assert.assertEquals(format.getSpaceAfter(), 0.0d);

 format.setLineUnitAfter(10.9);

 Assert.assertEquals(format.getSpaceAfter(), 130.8d, 0.1d);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5" +
         "\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863");
 
```

**Returns:**
double - El valor de la sangría izquierda (en caracteres) para los párrafos especificados.
### getCharacterUnitRightIndent() {#getCharacterUnitRightIndent}
```
public double getCharacterUnitRightIndent()
```


Obtiene el valor de sangría derecha (en caracteres) para los párrafos especificados.

 **Examples:** 

Muestra cómo cambiar el espaciado y las sangrías del párrafo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();

 // Below are five different spacing options, along with the properties that their configuration indirectly affects.
 // 1 -  Left indent:
 Assert.assertEquals(format.getLeftIndent(), 0.0d);

 format.setCharacterUnitLeftIndent(10.0);

 Assert.assertEquals(format.getLeftIndent(), 120.0d);

 // 2 -  Right indent:
 Assert.assertEquals(format.getRightIndent(), 0.0d);

 format.setCharacterUnitRightIndent(-5.5);

 Assert.assertEquals(format.getRightIndent(), -66.0d);

 // 3 -  Hanging indent:
 Assert.assertEquals(format.getFirstLineIndent(), 0.0d);

 format.setCharacterUnitFirstLineIndent(20.3);

 Assert.assertEquals(format.getFirstLineIndent(), 243.59d, 0.1d);

 // 4 -  Line spacing before paragraphs:
 Assert.assertEquals(format.getSpaceBefore(), 0.0d);

 format.setLineUnitBefore(5.1);

 Assert.assertEquals(format.getSpaceBefore(), 61.1d, 0.1d);

 // 5 -  Line spacing after paragraphs:
 Assert.assertEquals(format.getSpaceAfter(), 0.0d);

 format.setLineUnitAfter(10.9);

 Assert.assertEquals(format.getSpaceAfter(), 130.8d, 0.1d);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5" +
         "\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863");
 
```

**Returns:**
double - El valor de la sangría derecha (en caracteres) para los párrafos especificados.
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
### getDropCapPosition() {#getDropCapPosition}
```
public int getDropCapPosition()
```


Obtiene la posición para un texto de letra capitular.

 **Examples:** 

Muestra cómo anidar una lista dentro de otra lista.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Create an outline list for the headings.
 List outlineList = doc.getLists().add(ListTemplate.OUTLINE_NUMBERS);
 builder.getListFormat().setList(outlineList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("This is my Chapter 1");

 // Create a numbered list.
 List numberedList = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);
 builder.getListFormat().setList(numberedList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.NORMAL);
 builder.writeln("Numbered list item 1.");

 // Every paragraph that comprises a list will have this flag.
 Assert.assertTrue(builder.getCurrentParagraph().isListItem());
 Assert.assertTrue(builder.getParagraphFormat().isListItem());

 // Create a bulleted list.
 List bulletedList = doc.getLists().add(ListTemplate.BULLET_DEFAULT);
 builder.getListFormat().setList(bulletedList);
 builder.getParagraphFormat().setLeftIndent(72.0);
 builder.writeln("Bulleted list item 1.");
 builder.writeln("Bulleted list item 2.");
 builder.getParagraphFormat().clearFormatting();

 // Revert to the numbered list.
 builder.getListFormat().setList(numberedList);
 builder.writeln("Numbered list item 2.");
 builder.writeln("Numbered list item 3.");

 // Revert to the outline list.
 builder.getListFormat().setList(outlineList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("This is my Chapter 2");

 builder.getParagraphFormat().clearFormatting();

 builder.getDocument().save(getArtifactsDir() + "Lists.NestedLists.docx");
 
```

**Returns:**
int - La posición para un texto de letra capitular. El valor devuelto es una de las constantes de [DropCapPosition](../../com.aspose.words/dropcapposition/).
### getFarEastLineBreakControl() {#getFarEastLineBreakControl}
```
public boolean getFarEastLineBreakControl()
```


Obtiene una bandera que indica si se aplican las reglas de salto de línea de Asia Oriental al párrafo actual.

 **Examples:** 

Muestra cómo establecer propiedades especiales para la tipografía asiática.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setFarEastLineBreakControl(true);
 format.setWordWrap(false);
 format.setHangingPunctuation(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.AsianTypographyProperties.docx");
 
```

**Returns:**
boolean - Un indicador que muestra si se aplican las reglas de salto de línea de Asia Oriental al párrafo actual.
### getFirstLineIndent() {#getFirstLineIndent}
```
public double getFirstLineIndent()
```


Obtiene el valor (en puntos) para una sangría de primera línea o colgante.

Use valores positivos para establecer la sangría de la primera línea y valores negativos para establecer la sangría colgante.

 **Examples:** 

Muestra cómo insertar un párrafo en el documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Arial");
 font.setUnderline(Underline.DASH);

 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setFirstLineIndent(8.0);
 paragraphFormat.setAlignment(ParagraphAlignment.JUSTIFY);
 paragraphFormat.setAddSpaceBetweenFarEastAndAlpha(true);
 paragraphFormat.setAddSpaceBetweenFarEastAndDigit(true);
 paragraphFormat.setKeepTogether(true);

 // The "Writeln" method ends the paragraph after appending text
 // and then starts a new line, adding a new paragraph.
 builder.writeln("Hello world!");

 Assert.assertTrue(builder.getCurrentParagraph().isEndOfDocument());
 
```

**Returns:**
double - El valor (en puntos) para una primera línea o sangría colgante.
### getHangingPunctuation() {#getHangingPunctuation}
```
public boolean getHangingPunctuation()
```


Obtiene una bandera que indica si la puntuación colgante está habilitada para el párrafo actual.

 **Examples:** 

Muestra cómo establecer propiedades especiales para la tipografía asiática.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setFarEastLineBreakControl(true);
 format.setWordWrap(false);
 format.setHangingPunctuation(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.AsianTypographyProperties.docx");
 
```

**Returns:**
boolean - Un indicador que muestra si la puntuación colgante está habilitada para el párrafo actual.
### getKeepTogether() {#getKeepTogether}
```
public boolean getKeepTogether()
```


Verdadero si todas las líneas del párrafo deben permanecer en la misma página.

 **Examples:** 

Muestra cómo insertar un párrafo en el documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Arial");
 font.setUnderline(Underline.DASH);

 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setFirstLineIndent(8.0);
 paragraphFormat.setAlignment(ParagraphAlignment.JUSTIFY);
 paragraphFormat.setAddSpaceBetweenFarEastAndAlpha(true);
 paragraphFormat.setAddSpaceBetweenFarEastAndDigit(true);
 paragraphFormat.setKeepTogether(true);

 // The "Writeln" method ends the paragraph after appending text
 // and then starts a new line, adding a new paragraph.
 builder.writeln("Hello world!");

 Assert.assertTrue(builder.getCurrentParagraph().isEndOfDocument());
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getKeepWithNext() {#getKeepWithNext}
```
public boolean getKeepWithNext()
```


Verdadero si el párrafo debe permanecer en la misma página que el párrafo que lo sigue.

 **Examples:** 

Muestra cómo configurar una tabla para que permanezca junta en la misma página.

```

 Document doc = new Document(getMyDir() + "Table spanning two pages.docx");
 Table table = doc.getFirstSection().getBody().getTables().get(0);

 // Enabling KeepWithNext for every paragraph in the table except for the
 // last ones in the last row will prevent the table from splitting across multiple pages.
 for (Cell cell : (Iterable) table.getChildNodes(NodeType.CELL, true))
     for (Paragraph para : cell.getParagraphs()) {
         Assert.assertTrue(para.isInCell());

         if (!(cell.getParentRow().isLastRow() && para.isEndOfCell()))
             para.getParagraphFormat().setKeepWithNext(true);
     }

 doc.save(getArtifactsDir() + "Table.KeepTableTogether.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getLeftIndent() {#getLeftIndent}
```
public double getLeftIndent()
```


Obtiene el valor (en puntos) que representa la sangría izquierda del párrafo.

 **Examples:** 

Muestra cómo configurar el formato de párrafo para crear texto fuera de centro.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Center all text that the document builder writes, and set up indents.
 // The indent configuration below will create a body of text that will sit asymmetrically on the page.
 // The "center" that we align the text to will be the middle of the body of text, not the middle of the page.
 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setAlignment(ParagraphAlignment.CENTER);
 paragraphFormat.setLeftIndent(100.0);
 paragraphFormat.setRightIndent(50.0);
 paragraphFormat.setSpaceAfter(25.0);

 builder.writeln(
         "This paragraph demonstrates how left and right indentation affects word wrapping.");
 builder.writeln(
         "The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

 doc.save(getArtifactsDir() + "DocumentBuilder.SetParagraphFormatting.docx");
 
```

**Returns:**
double - El valor (en puntos) que representa la sangría izquierda para el párrafo.
### getLineSpacing() {#getLineSpacing}
```
public double getLineSpacing()
```


Obtiene el interlineado (en puntos) del párrafo.

 **Remarks:** 

Cuando la propiedad [getLineSpacingRule()](../../com.aspose.words/paragraphformat/\#getLineSpacingRule) / [setLineSpacingRule(int)](../../com.aspose.words/paragraphformat/\#setLineSpacingRule-int) se establece en [LineSpacingRule.AT\_LEAST](../../com.aspose.words/linespacingrule/\#AT-LEAST), el interlineado puede ser mayor o igual, pero nunca menor que el valor especificado de [getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double).

Cuando la propiedad [getLineSpacingRule()](../../com.aspose.words/paragraphformat/\#getLineSpacingRule) / [setLineSpacingRule(int)](../../com.aspose.words/paragraphformat/\#setLineSpacingRule-int) se establece en [LineSpacingRule.EXACTLY](../../com.aspose.words/linespacingrule/\#EXACTLY), el interlineado nunca cambia del valor especificado de [getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double), incluso si se usa una fuente más grande dentro del párrafo.

 **Examples:** 

Muestra cómo trabajar con el interlineado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are three line spacing rules that we can define using the
 // paragraph's "LineSpacingRule" property to configure spacing between paragraphs.
 // 1 -  Set a minimum amount of spacing.
 // This will give vertical padding to lines of text of any size
 // that is too small to maintain the minimum line-height.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.AT_LEAST);
 builder.getParagraphFormat().setLineSpacing(20.0);

 builder.writeln("Minimum line spacing of 20.");
 builder.writeln("Minimum line spacing of 20.");

 // 2 -  Set exact spacing.
 // Using font sizes that are too large for the spacing will truncate the text.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.EXACTLY);
 builder.getParagraphFormat().setLineSpacing(5.0);

 builder.writeln("Line spacing of exactly 5.");
 builder.writeln("Line spacing of exactly 5.");

 // 3 -  Set spacing as a multiple of default line spacing, which is 12 points by default.
 // This kind of spacing will scale to different font sizes.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.MULTIPLE);
 builder.getParagraphFormat().setLineSpacing(18.0);

 builder.writeln("Line spacing of 1.5 default lines.");
 builder.writeln("Line spacing of 1.5 default lines.");

 doc.save(getArtifactsDir() + "ParagraphFormat.LineSpacing.docx");
 
```

**Returns:**
double - El interlineado (en puntos) del párrafo.
### getLineSpacingRule() {#getLineSpacingRule}
```
public int getLineSpacingRule()
```


Obtiene el interlineado del párrafo.

 **Examples:** 

Muestra cómo trabajar con el interlineado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are three line spacing rules that we can define using the
 // paragraph's "LineSpacingRule" property to configure spacing between paragraphs.
 // 1 -  Set a minimum amount of spacing.
 // This will give vertical padding to lines of text of any size
 // that is too small to maintain the minimum line-height.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.AT_LEAST);
 builder.getParagraphFormat().setLineSpacing(20.0);

 builder.writeln("Minimum line spacing of 20.");
 builder.writeln("Minimum line spacing of 20.");

 // 2 -  Set exact spacing.
 // Using font sizes that are too large for the spacing will truncate the text.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.EXACTLY);
 builder.getParagraphFormat().setLineSpacing(5.0);

 builder.writeln("Line spacing of exactly 5.");
 builder.writeln("Line spacing of exactly 5.");

 // 3 -  Set spacing as a multiple of default line spacing, which is 12 points by default.
 // This kind of spacing will scale to different font sizes.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.MULTIPLE);
 builder.getParagraphFormat().setLineSpacing(18.0);

 builder.writeln("Line spacing of 1.5 default lines.");
 builder.writeln("Line spacing of 1.5 default lines.");

 doc.save(getArtifactsDir() + "ParagraphFormat.LineSpacing.docx");
 
```

**Returns:**
int - El interlineado del párrafo. El valor devuelto es uno de los constantes de [LineSpacingRule](../../com.aspose.words/linespacingrule/).
### getLineUnitAfter() {#getLineUnitAfter}
```
public double getLineUnitAfter()
```


Obtiene la cantidad de espacio (en líneas de cuadrícula) después de los párrafos.

 **Examples:** 

Muestra cómo cambiar el espaciado y las sangrías del párrafo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();

 // Below are five different spacing options, along with the properties that their configuration indirectly affects.
 // 1 -  Left indent:
 Assert.assertEquals(format.getLeftIndent(), 0.0d);

 format.setCharacterUnitLeftIndent(10.0);

 Assert.assertEquals(format.getLeftIndent(), 120.0d);

 // 2 -  Right indent:
 Assert.assertEquals(format.getRightIndent(), 0.0d);

 format.setCharacterUnitRightIndent(-5.5);

 Assert.assertEquals(format.getRightIndent(), -66.0d);

 // 3 -  Hanging indent:
 Assert.assertEquals(format.getFirstLineIndent(), 0.0d);

 format.setCharacterUnitFirstLineIndent(20.3);

 Assert.assertEquals(format.getFirstLineIndent(), 243.59d, 0.1d);

 // 4 -  Line spacing before paragraphs:
 Assert.assertEquals(format.getSpaceBefore(), 0.0d);

 format.setLineUnitBefore(5.1);

 Assert.assertEquals(format.getSpaceBefore(), 61.1d, 0.1d);

 // 5 -  Line spacing after paragraphs:
 Assert.assertEquals(format.getSpaceAfter(), 0.0d);

 format.setLineUnitAfter(10.9);

 Assert.assertEquals(format.getSpaceAfter(), 130.8d, 0.1d);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5" +
         "\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863");
 
```

**Returns:**
double - La cantidad de espacio (en líneas de cuadrícula) después de los párrafos.
### getLineUnitBefore() {#getLineUnitBefore}
```
public double getLineUnitBefore()
```


Obtiene la cantidad de espacio (en líneas de cuadrícula) antes de los párrafos.

 **Examples:** 

Muestra cómo cambiar el espaciado y las sangrías del párrafo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();

 // Below are five different spacing options, along with the properties that their configuration indirectly affects.
 // 1 -  Left indent:
 Assert.assertEquals(format.getLeftIndent(), 0.0d);

 format.setCharacterUnitLeftIndent(10.0);

 Assert.assertEquals(format.getLeftIndent(), 120.0d);

 // 2 -  Right indent:
 Assert.assertEquals(format.getRightIndent(), 0.0d);

 format.setCharacterUnitRightIndent(-5.5);

 Assert.assertEquals(format.getRightIndent(), -66.0d);

 // 3 -  Hanging indent:
 Assert.assertEquals(format.getFirstLineIndent(), 0.0d);

 format.setCharacterUnitFirstLineIndent(20.3);

 Assert.assertEquals(format.getFirstLineIndent(), 243.59d, 0.1d);

 // 4 -  Line spacing before paragraphs:
 Assert.assertEquals(format.getSpaceBefore(), 0.0d);

 format.setLineUnitBefore(5.1);

 Assert.assertEquals(format.getSpaceBefore(), 61.1d, 0.1d);

 // 5 -  Line spacing after paragraphs:
 Assert.assertEquals(format.getSpaceAfter(), 0.0d);

 format.setLineUnitAfter(10.9);

 Assert.assertEquals(format.getSpaceAfter(), 130.8d, 0.1d);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5" +
         "\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863");
 
```

**Returns:**
double - La cantidad de espacio (en líneas de cuadrícula) antes de los párrafos.
### getLinesToDrop() {#getLinesToDrop}
```
public int getLinesToDrop()
```


Obtiene el número de líneas del texto del párrafo usadas para calcular la altura de la letra capitular.

 **Examples:** 

Muestra cómo establecer el tamaño de una letra capitular.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the "LinesToDrop" property to designate a paragraph as a drop cap,
 // which will turn it into a large capital letter that will decorate the next paragraph.
 // Give this property a value of 4 to give the drop cap the height of four text lines.
 builder.getParagraphFormat().setLinesToDrop(4);
 builder.writeln("H");

 // Reset the "LinesToDrop" property to 0 to turn the next paragraph into an ordinary paragraph.
 // The text in this paragraph will wrap around the drop cap.
 builder.getParagraphFormat().setLinesToDrop(0);
 builder.writeln("ello world!");

 doc.save(getArtifactsDir() + "ParagraphFormat.LinesToDrop.odt");
 
```

**Returns:**
int - El número de líneas del texto del párrafo usadas para calcular la altura de la letra capitular.
### getMirrorIndents() {#getMirrorIndents}
```
public boolean getMirrorIndents()
```


Obtiene una bandera que indica si las sangrías izquierda y derecha tienen la misma anchura.

 **Examples:** 

Muestra cómo hacer que los sangrados izquierdo y derecho sean iguales.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 ParagraphFormat format = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat();

 format.setMirrorIndents(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.MirrorIndents.docx");
 
```

**Returns:**
boolean - Un indicador que muestra si los sangrados izquierdo y derecho tienen la misma anchura.
### getNoSpaceBetweenParagraphsOfSameStyle() {#getNoSpaceBetweenParagraphsOfSameStyle}
```
public boolean getNoSpaceBetweenParagraphsOfSameStyle()
```


Cuando verdadero, [getSpaceBefore()](../../com.aspose.words/paragraphformat/\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat/\#setSpaceBefore-double) y [getSpaceAfter()](../../com.aspose.words/paragraphformat/\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat/\#setSpaceAfter-double) serán ignorados entre los párrafos del mismo estilo.

 **Remarks:** 

Esta configuración solo tiene efecto cuando se aplica a un estilo de párrafo. Si se aplica directamente a un párrafo, no tiene efecto.

 **Examples:** 

Muestra cómo aplicar sin espacio entre párrafos con el mismo estilo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply a large amount of spacing before and after paragraphs that this builder will create.
 builder.getParagraphFormat().setSpaceBefore(24.0);
 builder.getParagraphFormat().setSpaceAfter(24.0);

 // Set the "NoSpaceBetweenParagraphsOfSameStyle" flag to "true" to apply
 // no spacing between paragraphs with the same style, which will group similar paragraphs.
 // Leave the "NoSpaceBetweenParagraphsOfSameStyle" flag as "false"
 // to evenly apply spacing to every paragraph.
 builder.getParagraphFormat().setNoSpaceBetweenParagraphsOfSameStyle(noSpaceBetweenParagraphsOfSameStyle);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Quote"));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphSpacingSameStyle.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getOutlineLevel() {#getOutlineLevel}
```
public int getOutlineLevel()
```


Especifica el nivel de esquema del párrafo en el documento.

 **Examples:** 

Muestra cómo configurar los niveles de esquema de párrafo para crear texto plegable.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Each paragraph has an OutlineLevel, which could be any number from 1 to 9, or at the default "BodyText" value.
 // Setting the property to one of the numbered values will show an arrow to the left
 // of the beginning of the paragraph.
 builder.getParagraphFormat().setOutlineLevel(OutlineLevel.LEVEL_1);
 builder.writeln("Paragraph outline level 1.");

 // Level 1 is the topmost level. If there is a paragraph with a lower level below a paragraph with a higher level,
 // collapsing the higher-level paragraph will collapse the lower level paragraph.
 builder.getParagraphFormat().setOutlineLevel(OutlineLevel.LEVEL_2);
 builder.writeln("Paragraph outline level 2.");

 // Two paragraphs of the same level will not collapse each other,
 // and the arrows do not collapse the paragraphs they point to.
 builder.getParagraphFormat().setOutlineLevel(OutlineLevel.LEVEL_3);
 builder.writeln("Paragraph outline level 3.");
 builder.writeln("Paragraph outline level 3.");

 // The default "BodyText" value is the lowest, which a paragraph of any level can collapse.
 builder.getParagraphFormat().setOutlineLevel(OutlineLevel.BODY_TEXT);
 builder.writeln("Paragraph at main text level.");

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphOutlineLevel.docx");
 
```

**Returns:**
int - El valor entero correspondiente. El valor devuelto es uno de los constantes de [OutlineLevel](../../com.aspose.words/outlinelevel/).
### getPageBreakBefore() {#getPageBreakBefore}
```
public boolean getPageBreakBefore()
```


Verdadero si se fuerza un salto de página antes del párrafo.

 **Examples:** 

Muestra cómo crear párrafos con saltos de página al inicio.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set this flag to "true" to apply a page break to each paragraph's beginning
 // that the document builder will create under this ParagraphFormat configuration.
 // The first paragraph will not receive a page break.
 // Leave this flag as "false" to start each new paragraph on the same page
 // as the previous, provided there is sufficient space.
 builder.getParagraphFormat().setPageBreakBefore(pageBreakBefore);

 builder.writeln("Paragraph 1.");
 builder.writeln("Paragraph 2.");

 LayoutCollector layoutCollector = new LayoutCollector(doc);
 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 if (pageBreakBefore) {
     Assert.assertEquals(1, layoutCollector.getStartPageIndex(paragraphs.get(0)));
     Assert.assertEquals(2, layoutCollector.getStartPageIndex(paragraphs.get(1)));
 } else {
     Assert.assertEquals(1, layoutCollector.getStartPageIndex(paragraphs.get(0)));
     Assert.assertEquals(1, layoutCollector.getStartPageIndex(paragraphs.get(1)));
 }

 doc.save(getArtifactsDir() + "ParagraphFormat.PageBreakBefore.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getRightIndent() {#getRightIndent}
```
public double getRightIndent()
```


Obtiene el valor (en puntos) que representa la sangría derecha del párrafo.

 **Examples:** 

Muestra cómo configurar el formato de párrafo para crear texto fuera de centro.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Center all text that the document builder writes, and set up indents.
 // The indent configuration below will create a body of text that will sit asymmetrically on the page.
 // The "center" that we align the text to will be the middle of the body of text, not the middle of the page.
 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setAlignment(ParagraphAlignment.CENTER);
 paragraphFormat.setLeftIndent(100.0);
 paragraphFormat.setRightIndent(50.0);
 paragraphFormat.setSpaceAfter(25.0);

 builder.writeln(
         "This paragraph demonstrates how left and right indentation affects word wrapping.");
 builder.writeln(
         "The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

 doc.save(getArtifactsDir() + "DocumentBuilder.SetParagraphFormatting.docx");
 
```

**Returns:**
double - El valor (en puntos) que representa el sangrado derecho del párrafo.
### getShading() {#getShading}
```
public Shading getShading()
```


Devuelve un objeto [Shading](../../com.aspose.words/shading/) que se refiere al formato de sombreado del párrafo.

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
[Shading](../../com.aspose.words/shading/) - A [Shading](../../com.aspose.words/shading/) object that refers to the shading formatting for the paragraph.
### getSnapToGrid() {#getSnapToGrid}
```
public boolean getSnapToGrid()
```


Especifica si el párrafo actual debe usar la configuración de líneas de cuadrícula del documento por página al organizar el contenido en el párrafo.

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
boolean - El valor  boolean  correspondiente.
### getSpaceAfter() {#getSpaceAfter}
```
public double getSpaceAfter()
```


Obtiene la cantidad de espacio (en puntos) después del párrafo.

**Returns:**
double - La cantidad de espacio (en puntos) después del párrafo.
### getSpaceAfterAuto() {#getSpaceAfterAuto}
```
public boolean getSpaceAfterAuto()
```


Verdadero si la cantidad de espacio después del párrafo se establece automáticamente.

 **Remarks:** 

Cuando se establece en  true , anula el efecto de [getSpaceAfter()](../../com.aspose.words/paragraphformat/\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat/\#setSpaceAfter-double).

Cuando estableces Space Before y Space After del párrafo en Auto, Microsoft Word agrega automáticamente 14 puntos de espacio entre párrafos según las siguientes reglas:

 *  Normally, spacing is added after all paragraphs.
 *  In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
 *  In a nested bulleted or numbered list spacing is not added.
 *  Spacing is normally added after a table.
 *  Spacing is not added after a table if it is the last block in a table cell.
 *  Spacing is not added after the last paragraph in a table cell.

 **Examples:** 

Muestra cómo establecer el espaciado automático de párrafos.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply a large amount of spacing before and after paragraphs that this builder will create.
 builder.getParagraphFormat().setSpaceBefore(24.0);
 builder.getParagraphFormat().setSpaceAfter(24.0);

 // Set these flags to "true" to apply automatic spacing,
 // effectively ignoring the spacing in the properties we set above.
 // Leave them as "false" will apply our custom paragraph spacing.
 builder.getParagraphFormat().setSpaceAfterAuto(autoSpacing);
 builder.getParagraphFormat().setSpaceBeforeAuto(autoSpacing);

 // Insert two paragraphs that will have spacing above and below them and save the document.
 builder.writeln("Paragraph 1.");
 builder.writeln("Paragraph 2.");

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphSpacingAuto.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getSpaceBefore() {#getSpaceBefore}
```
public double getSpaceBefore()
```


Obtiene la cantidad de espacio (en puntos) antes del párrafo.

**Returns:**
double - La cantidad de espacio (en puntos) antes del párrafo.
### getSpaceBeforeAuto() {#getSpaceBeforeAuto}
```
public boolean getSpaceBeforeAuto()
```


Verdadero si la cantidad de espacio antes del párrafo se establece automáticamente.

 **Remarks:** 

Cuando se establece en  true , anula el efecto de [getSpaceBefore()](../../com.aspose.words/paragraphformat/\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat/\#setSpaceBefore-double).

Cuando estableces Space Before y Space After del párrafo en Auto, Microsoft Word agrega automáticamente 14 puntos de espacio entre párrafos según las siguientes reglas:

 *  Normally, spacing is added after all paragraphs.
 *  In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
 *  In a nested bulleted or numbered list spacing is not added.
 *  Spacing is normally added after a table.
 *  Spacing is not added after a table if it is the last block in a table cell.
 *  Spacing is not added after the last paragraph in a table cell.

 **Examples:** 

Muestra cómo establecer el espaciado automático de párrafos.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply a large amount of spacing before and after paragraphs that this builder will create.
 builder.getParagraphFormat().setSpaceBefore(24.0);
 builder.getParagraphFormat().setSpaceAfter(24.0);

 // Set these flags to "true" to apply automatic spacing,
 // effectively ignoring the spacing in the properties we set above.
 // Leave them as "false" will apply our custom paragraph spacing.
 builder.getParagraphFormat().setSpaceAfterAuto(autoSpacing);
 builder.getParagraphFormat().setSpaceBeforeAuto(autoSpacing);

 // Insert two paragraphs that will have spacing above and below them and save the document.
 builder.writeln("Paragraph 1.");
 builder.writeln("Paragraph 2.");

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphSpacingAuto.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getStyle() {#getStyle}
```
public Style getStyle()
```


Obtiene el estilo de párrafo aplicado a este formato.

 **Examples:** 

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

**Returns:**
[Style](../../com.aspose.words/style/) - The paragraph style applied to this formatting.
### getStyleIdentifier() {#getStyleIdentifier}
```
public int getStyleIdentifier()
```


Obtiene el identificador de estilo independiente de la configuración regional del estilo de párrafo aplicado a este formato.

 **Examples:** 

Muestra cómo insertar una tabla de contenido (TOC) en un documento usando estilos de encabezado como entradas.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a table of contents for the first page of the document.
 // Configure the table to pick up paragraphs with headings of levels 1 to 3.
 // Also, set its entries to be hyperlinks that will take us
 // to the location of the heading when left-clicked in Microsoft Word.
 builder.insertTableOfContents("\\o \"1-3\" \\h \\z \\u");
 builder.insertBreak(BreakType.PAGE_BREAK);

 // Populate the table of contents by adding paragraphs with heading styles.
 // Each such heading with a level between 1 and 3 will create an entry in the table.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("Heading 1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 1.1");
 builder.writeln("Heading 1.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("Heading 2");
 builder.writeln("Heading 3");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 3.1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_3);
 builder.writeln("Heading 3.1.1");
 builder.writeln("Heading 3.1.2");
 builder.writeln("Heading 3.1.3");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_4);
 builder.writeln("Heading 3.1.3.1");
 builder.writeln("Heading 3.1.3.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 3.2");
 builder.writeln("Heading 3.3");

 // A table of contents is a field of a type that needs to be updated to show an up-to-date result.
 doc.updateFields();
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertToc.docx");
 
```

**Returns:**
int - El identificador de estilo independiente de la configuración regional del estilo de párrafo aplicado a este formato. El valor devuelto es uno de los constantes de [StyleIdentifier](../../com.aspose.words/styleidentifier/).
### getStyleName() {#getStyleName}
```
public String getStyleName()
```


Obtiene el nombre del estilo de párrafo aplicado a este formato.

 **Examples:** 

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
java.lang.String - El nombre del estilo de párrafo aplicado a este formato.
### getSuppressAutoHyphens() {#getSuppressAutoHyphens}
```
public boolean getSuppressAutoHyphens()
```


Especifica si el párrafo actual debe estar exento de cualquier guionado que se aplique en la configuración del documento.

 **Examples:** 

Muestra cómo suprimir la guionización de un párrafo.

```

 Hyphenation.registerDictionary("de-CH", getMyDir() + "hyph_de_CH.dic");

 Assert.assertTrue(Hyphenation.isDictionaryRegistered("de-CH"));

 // Open a document containing text with a locale matching that of our dictionary.
 // When we save this document to a fixed page save format, its text will have hyphenation.
 Document doc = new Document(getMyDir() + "German text.docx");

 // We can set the "SuppressAutoHyphens" property to "true" to disable hyphenation
 // for a specific paragraph while keeping it enabled for the rest of the document.
 // The default value for this property is "false",
 // which means every paragraph by default uses hyphenation if any is available.
 doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().setSuppressAutoHyphens(suppressAutoHyphens);

 doc.save(getArtifactsDir() + "ParagraphFormat.SuppressHyphens.pdf");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getSuppressLineNumbers() {#getSuppressLineNumbers}
```
public boolean getSuppressLineNumbers()
```


Especifica si las líneas del párrafo actual deben estar exentas de la numeración de líneas que se aplica en la sección principal.

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
boolean - El valor  boolean  correspondiente.
### getTabStops() {#getTabStops}
```
public TabStopCollection getTabStops()
```


Obtiene la colección de tabuladores personalizados definidos para este objeto.

 **Examples:** 

Muestra cómo modificar la posición del tabulador derecho en los párrafos relacionados con el TOC.

```

 Document doc = new Document(getMyDir() + "Table of contents.docx");

 // Iterate through all paragraphs with TOC result-based styles; this is any style between TOC and TOC9.
 for (Paragraph para : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     if (para.getParagraphFormat().getStyle().getStyleIdentifier() >= StyleIdentifier.TOC_1
             && para.getParagraphFormat().getStyle().getStyleIdentifier() <= StyleIdentifier.TOC_9) {
         // Get the first tab used in this paragraph, this should be the tab used to align the page numbers.
         TabStop tab = para.getParagraphFormat().getTabStops().get(0);

         // Replace the first default tab, stop with a custom tab stop.
         para.getParagraphFormat().getTabStops().removeByPosition(tab.getPosition());
         para.getParagraphFormat().getTabStops().add(tab.getPosition() - 50.0, tab.getAlignment(), tab.getLeader());
     }
 }

 doc.save(getArtifactsDir() + "Styles.ChangeTocsTabStops.docx");
 
```

**Returns:**
[TabStopCollection](../../com.aspose.words/tabstopcollection/) - The collection of custom tab stops defined for this object.
### getWidowControl() {#getWidowControl}
```
public boolean getWidowControl()
```


Verdadero si la primera y la última línea del párrafo deben permanecer en la misma página que el resto del párrafo.

 **Examples:** 

Muestra cómo habilitar el control de viudas y huérfanas para un párrafo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // When we write the text that does not fit onto one page, one line may spill over onto the next page.
 // The single line that ends up on the next page is called an "Orphan",
 // and the previous line where the orphan broke off is called a "Widow".
 // We can fix orphans and widows by rearranging text via font size, spacing, or page margins.
 // If we wish to preserve our document's dimensions, we can set this flag to "true"
 // to push widows onto the same page as their respective orphans.
 // Leave this flag as "false" will leave widow/orphan pairs in text.
 // Every paragraph has this setting accessible in Microsoft Word via Home -> Paragraph -> Paragraph Settings
 // (button on bottom right hand corner of "Paragraph" tab) -> "Widow/Orphan control".
 builder.getParagraphFormat().setWidowControl(widowControl);

 // Insert text that produces an orphan and a widow.
 builder.getFont().setSize(68.0);
 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "ParagraphFormat.WidowControl.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getWordWrap() {#getWordWrap}
```
public boolean getWordWrap()
```


Si esta propiedad es  false , el texto latino en medio de una palabra puede dividirse en el párrafo actual. De lo contrario, el texto latino se divide por palabras completas.

 **Examples:** 

Muestra cómo establecer propiedades especiales para la tipografía asiática.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setFarEastLineBreakControl(true);
 format.setWordWrap(false);
 format.setHangingPunctuation(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.AsianTypographyProperties.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### isHeading() {#isHeading}
```
public boolean isHeading()
```


Verdadero cuando el estilo de párrafo es uno de los estilos de encabezado incorporados.

 **Examples:** 

Muestra cómo limitar el nivel de encabezados que aparecerá en el esquema de un documento PDF guardado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert headings that can serve as TOC entries of levels 1, 2, and then 3.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);

 Assert.assertTrue(builder.getParagraphFormat().isHeading());

 builder.writeln("Heading 1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);

 builder.writeln("Heading 1.1");
 builder.writeln("Heading 1.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_3);

 builder.writeln("Heading 1.2.1");
 builder.writeln("Heading 1.2.2");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();
 saveOptions.setSaveFormat(SaveFormat.PDF);

 // The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
 // Clicking on an entry in this outline will take us to the location of its respective heading.
 // Set the "HeadingsOutlineLevels" property to "2" to exclude all headings whose levels are above 2 from the outline.
 // The last two headings we have inserted above will not appear.
 saveOptions.getOutlineOptions().setHeadingsOutlineLevels(2);

 doc.save(getArtifactsDir() + "PdfSaveOptions.HeadingsOutlineLevels.pdf", saveOptions);
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### isListItem() {#isListItem}
```
public boolean isListItem()
```


Verdadero cuando el párrafo es un elemento de una lista con viñetas o numerada.

 **Examples:** 

Muestra cómo anidar una lista dentro de otra lista.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Create an outline list for the headings.
 List outlineList = doc.getLists().add(ListTemplate.OUTLINE_NUMBERS);
 builder.getListFormat().setList(outlineList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("This is my Chapter 1");

 // Create a numbered list.
 List numberedList = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);
 builder.getListFormat().setList(numberedList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.NORMAL);
 builder.writeln("Numbered list item 1.");

 // Every paragraph that comprises a list will have this flag.
 Assert.assertTrue(builder.getCurrentParagraph().isListItem());
 Assert.assertTrue(builder.getParagraphFormat().isListItem());

 // Create a bulleted list.
 List bulletedList = doc.getLists().add(ListTemplate.BULLET_DEFAULT);
 builder.getListFormat().setList(bulletedList);
 builder.getParagraphFormat().setLeftIndent(72.0);
 builder.writeln("Bulleted list item 1.");
 builder.writeln("Bulleted list item 2.");
 builder.getParagraphFormat().clearFormatting();

 // Revert to the numbered list.
 builder.getListFormat().setList(numberedList);
 builder.writeln("Numbered list item 2.");
 builder.writeln("Numbered list item 3.");

 // Revert to the outline list.
 builder.getListFormat().setList(outlineList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("This is my Chapter 2");

 builder.getParagraphFormat().clearFormatting();

 builder.getDocument().save(getArtifactsDir() + "Lists.NestedLists.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### setAddSpaceBetweenFarEastAndAlpha(boolean value) {#setAddSpaceBetweenFarEastAndAlpha-boolean}
```
public void setAddSpaceBetweenFarEastAndAlpha(boolean value)
```


Establece una bandera que indica si el espaciado entre caracteres se ajusta automáticamente entre regiones de texto latino y regiones de texto de Asia Oriental en el párrafo actual.

 **Examples:** 

Muestra cómo insertar un párrafo en el documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Arial");
 font.setUnderline(Underline.DASH);

 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setFirstLineIndent(8.0);
 paragraphFormat.setAlignment(ParagraphAlignment.JUSTIFY);
 paragraphFormat.setAddSpaceBetweenFarEastAndAlpha(true);
 paragraphFormat.setAddSpaceBetweenFarEastAndDigit(true);
 paragraphFormat.setKeepTogether(true);

 // The "Writeln" method ends the paragraph after appending text
 // and then starts a new line, adding a new paragraph.
 builder.writeln("Hello world!");

 Assert.assertTrue(builder.getCurrentParagraph().isEndOfDocument());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Una bandera que indica si el espaciado entre caracteres se ajusta automáticamente entre regiones de texto latino y regiones de texto de Asia Oriental en el párrafo actual. |

### setAddSpaceBetweenFarEastAndDigit(boolean value) {#setAddSpaceBetweenFarEastAndDigit-boolean}
```
public void setAddSpaceBetweenFarEastAndDigit(boolean value)
```


Establece una bandera que indica si el espaciado entre caracteres se ajusta automáticamente entre regiones de números y regiones de texto de Asia Oriental en el párrafo actual.

 **Examples:** 

Muestra cómo insertar un párrafo en el documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Arial");
 font.setUnderline(Underline.DASH);

 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setFirstLineIndent(8.0);
 paragraphFormat.setAlignment(ParagraphAlignment.JUSTIFY);
 paragraphFormat.setAddSpaceBetweenFarEastAndAlpha(true);
 paragraphFormat.setAddSpaceBetweenFarEastAndDigit(true);
 paragraphFormat.setKeepTogether(true);

 // The "Writeln" method ends the paragraph after appending text
 // and then starts a new line, adding a new paragraph.
 builder.writeln("Hello world!");

 Assert.assertTrue(builder.getCurrentParagraph().isEndOfDocument());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Una bandera que indica si el espaciado entre caracteres se ajusta automáticamente entre regiones de números y regiones de texto de Asia Oriental en el párrafo actual. |

### setAlignment(int value) {#setAlignment-int}
```
public void setAlignment(int value)
```


Establece la alineación del texto para el párrafo.

 **Examples:** 

Muestra cómo insertar un párrafo en el documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Arial");
 font.setUnderline(Underline.DASH);

 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setFirstLineIndent(8.0);
 paragraphFormat.setAlignment(ParagraphAlignment.JUSTIFY);
 paragraphFormat.setAddSpaceBetweenFarEastAndAlpha(true);
 paragraphFormat.setAddSpaceBetweenFarEastAndDigit(true);
 paragraphFormat.setKeepTogether(true);

 // The "Writeln" method ends the paragraph after appending text
 // and then starts a new line, adding a new paragraph.
 builder.writeln("Hello world!");

 Assert.assertTrue(builder.getCurrentParagraph().isEndOfDocument());
 
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
| value | int | Alineación de texto para el párrafo. El valor debe ser uno de los constantes [ParagraphAlignment](../../com.aspose.words/paragraphalignment/). |

### setBaselineAlignment(int value) {#setBaselineAlignment-int}
```
public void setBaselineAlignment(int value)
```


Establece la posición vertical de las fuentes en una línea.

 **Examples:** 

Muestra cómo establecer la posición vertical de las fuentes en una línea.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat();
 if (format.getBaselineAlignment() == BaselineAlignment.AUTO)
 {
     format.setBaselineAlignment(BaselineAlignment.TOP);
 }

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphBaselineAlignment.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | Posición vertical de las fuentes en una línea. El valor debe ser uno de los constantes [BaselineAlignment](../../com.aspose.words/baselinealignment/). |

### setBidi(boolean value) {#setBidi-boolean}
```
public void setBidi(boolean value)
```


Establece si este es un párrafo de derecha a izquierda.

 **Remarks:** 

Cuando  true , las ejecuciones y otros objetos en línea en este párrafo se disponen de derecha a izquierda.

 **Examples:** 

Muestra cómo crear listas compatibles con idiomas de derecha a izquierda usando campos BIDIOUTLINE.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // The BIDIOUTLINE field numbers paragraphs like the AUTONUM/LISTNUM fields,
 // but is only visible when a right-to-left editing language is enabled, such as Hebrew or Arabic.
 // The following field will display ".1", the RTL equivalent of list number "1.".
 FieldBidiOutline field = (FieldBidiOutline) builder.insertField(FieldType.FIELD_BIDI_OUTLINE, true);
 builder.writeln("\u05e9\u05dc\u05d5\u05dd");

 Assert.assertEquals(" BIDIOUTLINE ", field.getFieldCode());

 // Add two more BIDIOUTLINE fields, which will display ".2" and ".3".
 builder.insertField(FieldType.FIELD_BIDI_OUTLINE, true);
 builder.writeln("\u05e9\u05dc\u05d5\u05dd");
 builder.insertField(FieldType.FIELD_BIDI_OUTLINE, true);
 builder.writeln("\u05e9\u05dc\u05d5\u05dd");

 // Set the horizontal text alignment for every paragraph in the document to RTL.
 for (Paragraph para : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     para.getParagraphFormat().setBidi(true);
 }

 // If we enable a right-to-left editing language in Microsoft Word, our fields will display numbers.
 // Otherwise, they will display "###".
 doc.save(getArtifactsDir() + "Field.BIDIOUTLINE.docx");
 
```

Muestra cómo detectar la dirección del texto en un documento de texto plano.

```

 // Create a "TxtLoadOptions" object, which we can pass to a document's constructor
 // to modify how we load a plaintext document.
 TxtLoadOptions loadOptions = new TxtLoadOptions();

 // Set the "DocumentDirection" property to "DocumentDirection.Auto" automatically detects
 // the direction of every paragraph of text that Aspose.Words loads from plaintext.
 // Each paragraph's "Bidi" property will store its direction.
 loadOptions.setDocumentDirection(DocumentDirection.AUTO);

 // Detect Hebrew text as right-to-left.
 Document doc = new Document(getMyDir() + "Hebrew text.txt", loadOptions);

 Assert.assertTrue(doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBidi());

 // Detect English text as right-to-left.
 doc = new Document(getMyDir() + "English text.txt", loadOptions);

 Assert.assertFalse(doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBidi());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Indica si este es un párrafo de derecha a izquierda. |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |
| valor | java.lang.Object |  |

### setCharacterUnitFirstLineIndent(double value) {#setCharacterUnitFirstLineIndent-double}
```
public void setCharacterUnitFirstLineIndent(double value)
```


Establece el valor (en caracteres) para la sangría de primera línea o colgante.

Use valores positivos para establecer la sangría de la primera línea y valores negativos para establecer la sangría colgante.

 **Examples:** 

Muestra cómo cambiar el espaciado y las sangrías del párrafo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();

 // Below are five different spacing options, along with the properties that their configuration indirectly affects.
 // 1 -  Left indent:
 Assert.assertEquals(format.getLeftIndent(), 0.0d);

 format.setCharacterUnitLeftIndent(10.0);

 Assert.assertEquals(format.getLeftIndent(), 120.0d);

 // 2 -  Right indent:
 Assert.assertEquals(format.getRightIndent(), 0.0d);

 format.setCharacterUnitRightIndent(-5.5);

 Assert.assertEquals(format.getRightIndent(), -66.0d);

 // 3 -  Hanging indent:
 Assert.assertEquals(format.getFirstLineIndent(), 0.0d);

 format.setCharacterUnitFirstLineIndent(20.3);

 Assert.assertEquals(format.getFirstLineIndent(), 243.59d, 0.1d);

 // 4 -  Line spacing before paragraphs:
 Assert.assertEquals(format.getSpaceBefore(), 0.0d);

 format.setLineUnitBefore(5.1);

 Assert.assertEquals(format.getSpaceBefore(), 61.1d, 0.1d);

 // 5 -  Line spacing after paragraphs:
 Assert.assertEquals(format.getSpaceAfter(), 0.0d);

 format.setLineUnitAfter(10.9);

 Assert.assertEquals(format.getSpaceAfter(), 130.8d, 0.1d);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5" +
         "\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | El valor (en caracteres) para la sangría de primera línea o colgante. |

### setCharacterUnitLeftIndent(double value) {#setCharacterUnitLeftIndent-double}
```
public void setCharacterUnitLeftIndent(double value)
```


Establece el valor de sangría izquierda (en caracteres) para los párrafos especificados.

 **Examples:** 

Muestra cómo cambiar el espaciado y las sangrías del párrafo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();

 // Below are five different spacing options, along with the properties that their configuration indirectly affects.
 // 1 -  Left indent:
 Assert.assertEquals(format.getLeftIndent(), 0.0d);

 format.setCharacterUnitLeftIndent(10.0);

 Assert.assertEquals(format.getLeftIndent(), 120.0d);

 // 2 -  Right indent:
 Assert.assertEquals(format.getRightIndent(), 0.0d);

 format.setCharacterUnitRightIndent(-5.5);

 Assert.assertEquals(format.getRightIndent(), -66.0d);

 // 3 -  Hanging indent:
 Assert.assertEquals(format.getFirstLineIndent(), 0.0d);

 format.setCharacterUnitFirstLineIndent(20.3);

 Assert.assertEquals(format.getFirstLineIndent(), 243.59d, 0.1d);

 // 4 -  Line spacing before paragraphs:
 Assert.assertEquals(format.getSpaceBefore(), 0.0d);

 format.setLineUnitBefore(5.1);

 Assert.assertEquals(format.getSpaceBefore(), 61.1d, 0.1d);

 // 5 -  Line spacing after paragraphs:
 Assert.assertEquals(format.getSpaceAfter(), 0.0d);

 format.setLineUnitAfter(10.9);

 Assert.assertEquals(format.getSpaceAfter(), 130.8d, 0.1d);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5" +
         "\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | El valor de sangría izquierda (en caracteres) para los párrafos especificados. |

### setCharacterUnitRightIndent(double value) {#setCharacterUnitRightIndent-double}
```
public void setCharacterUnitRightIndent(double value)
```


Establece el valor de sangría derecha (en caracteres) para los párrafos especificados.

 **Examples:** 

Muestra cómo cambiar el espaciado y las sangrías del párrafo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();

 // Below are five different spacing options, along with the properties that their configuration indirectly affects.
 // 1 -  Left indent:
 Assert.assertEquals(format.getLeftIndent(), 0.0d);

 format.setCharacterUnitLeftIndent(10.0);

 Assert.assertEquals(format.getLeftIndent(), 120.0d);

 // 2 -  Right indent:
 Assert.assertEquals(format.getRightIndent(), 0.0d);

 format.setCharacterUnitRightIndent(-5.5);

 Assert.assertEquals(format.getRightIndent(), -66.0d);

 // 3 -  Hanging indent:
 Assert.assertEquals(format.getFirstLineIndent(), 0.0d);

 format.setCharacterUnitFirstLineIndent(20.3);

 Assert.assertEquals(format.getFirstLineIndent(), 243.59d, 0.1d);

 // 4 -  Line spacing before paragraphs:
 Assert.assertEquals(format.getSpaceBefore(), 0.0d);

 format.setLineUnitBefore(5.1);

 Assert.assertEquals(format.getSpaceBefore(), 61.1d, 0.1d);

 // 5 -  Line spacing after paragraphs:
 Assert.assertEquals(format.getSpaceAfter(), 0.0d);

 format.setLineUnitAfter(10.9);

 Assert.assertEquals(format.getSpaceAfter(), 130.8d, 0.1d);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5" +
         "\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | El valor de sangría derecha (en caracteres) para los párrafos especificados. |

### setDropCapPosition(int value) {#setDropCapPosition-int}
```
public void setDropCapPosition(int value)
```


Establece la posición para un texto de letra capitular.

 **Examples:** 

Muestra cómo anidar una lista dentro de otra lista.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Create an outline list for the headings.
 List outlineList = doc.getLists().add(ListTemplate.OUTLINE_NUMBERS);
 builder.getListFormat().setList(outlineList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("This is my Chapter 1");

 // Create a numbered list.
 List numberedList = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);
 builder.getListFormat().setList(numberedList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.NORMAL);
 builder.writeln("Numbered list item 1.");

 // Every paragraph that comprises a list will have this flag.
 Assert.assertTrue(builder.getCurrentParagraph().isListItem());
 Assert.assertTrue(builder.getParagraphFormat().isListItem());

 // Create a bulleted list.
 List bulletedList = doc.getLists().add(ListTemplate.BULLET_DEFAULT);
 builder.getListFormat().setList(bulletedList);
 builder.getParagraphFormat().setLeftIndent(72.0);
 builder.writeln("Bulleted list item 1.");
 builder.writeln("Bulleted list item 2.");
 builder.getParagraphFormat().clearFormatting();

 // Revert to the numbered list.
 builder.getListFormat().setList(numberedList);
 builder.writeln("Numbered list item 2.");
 builder.writeln("Numbered list item 3.");

 // Revert to the outline list.
 builder.getListFormat().setList(outlineList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("This is my Chapter 2");

 builder.getParagraphFormat().clearFormatting();

 builder.getDocument().save(getArtifactsDir() + "Lists.NestedLists.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | La posición para un texto de iniciales decorativas. El valor debe ser uno de los constantes [DropCapPosition](../../com.aspose.words/dropcapposition/). |

### setFarEastLineBreakControl(boolean value) {#setFarEastLineBreakControl-boolean}
```
public void setFarEastLineBreakControl(boolean value)
```


Establece una bandera que indica si se aplican las reglas de salto de línea de Asia Oriental al párrafo actual.

 **Examples:** 

Muestra cómo establecer propiedades especiales para la tipografía asiática.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setFarEastLineBreakControl(true);
 format.setWordWrap(false);
 format.setHangingPunctuation(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.AsianTypographyProperties.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Una bandera que indica si se aplican las reglas de salto de línea de Asia Oriental al párrafo actual. |

### setFirstLineIndent(double value) {#setFirstLineIndent-double}
```
public void setFirstLineIndent(double value)
```


Establece el valor (en puntos) para una primera línea o sangría colgante.

Use valores positivos para establecer la sangría de la primera línea y valores negativos para establecer la sangría colgante.

 **Examples:** 

Muestra cómo insertar un párrafo en el documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Arial");
 font.setUnderline(Underline.DASH);

 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setFirstLineIndent(8.0);
 paragraphFormat.setAlignment(ParagraphAlignment.JUSTIFY);
 paragraphFormat.setAddSpaceBetweenFarEastAndAlpha(true);
 paragraphFormat.setAddSpaceBetweenFarEastAndDigit(true);
 paragraphFormat.setKeepTogether(true);

 // The "Writeln" method ends the paragraph after appending text
 // and then starts a new line, adding a new paragraph.
 builder.writeln("Hello world!");

 Assert.assertTrue(builder.getCurrentParagraph().isEndOfDocument());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | El valor (en puntos) para una sangría de primera línea o colgante. |

### setHangingPunctuation(boolean value) {#setHangingPunctuation-boolean}
```
public void setHangingPunctuation(boolean value)
```


Establece una bandera que indica si la puntuación colgante está habilitada para el párrafo actual.

 **Examples:** 

Muestra cómo establecer propiedades especiales para la tipografía asiática.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setFarEastLineBreakControl(true);
 format.setWordWrap(false);
 format.setHangingPunctuation(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.AsianTypographyProperties.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Una bandera que indica si la puntuación colgante está habilitada para el párrafo actual. |

### setKeepTogether(boolean value) {#setKeepTogether-boolean}
```
public void setKeepTogether(boolean value)
```


Verdadero si todas las líneas del párrafo deben permanecer en la misma página.

 **Examples:** 

Muestra cómo insertar un párrafo en el documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Arial");
 font.setUnderline(Underline.DASH);

 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setFirstLineIndent(8.0);
 paragraphFormat.setAlignment(ParagraphAlignment.JUSTIFY);
 paragraphFormat.setAddSpaceBetweenFarEastAndAlpha(true);
 paragraphFormat.setAddSpaceBetweenFarEastAndDigit(true);
 paragraphFormat.setKeepTogether(true);

 // The "Writeln" method ends the paragraph after appending text
 // and then starts a new line, adding a new paragraph.
 builder.writeln("Hello world!");

 Assert.assertTrue(builder.getCurrentParagraph().isEndOfDocument());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setKeepWithNext(boolean value) {#setKeepWithNext-boolean}
```
public void setKeepWithNext(boolean value)
```


Verdadero si el párrafo debe permanecer en la misma página que el párrafo que lo sigue.

 **Examples:** 

Muestra cómo configurar una tabla para que permanezca junta en la misma página.

```

 Document doc = new Document(getMyDir() + "Table spanning two pages.docx");
 Table table = doc.getFirstSection().getBody().getTables().get(0);

 // Enabling KeepWithNext for every paragraph in the table except for the
 // last ones in the last row will prevent the table from splitting across multiple pages.
 for (Cell cell : (Iterable) table.getChildNodes(NodeType.CELL, true))
     for (Paragraph para : cell.getParagraphs()) {
         Assert.assertTrue(para.isInCell());

         if (!(cell.getParentRow().isLastRow() && para.isEndOfCell()))
             para.getParagraphFormat().setKeepWithNext(true);
     }

 doc.save(getArtifactsDir() + "Table.KeepTableTogether.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setLeftIndent(double value) {#setLeftIndent-double}
```
public void setLeftIndent(double value)
```


Establece el valor (en puntos) que representa la sangría izquierda para el párrafo.

 **Examples:** 

Muestra cómo configurar el formato de párrafo para crear texto fuera de centro.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Center all text that the document builder writes, and set up indents.
 // The indent configuration below will create a body of text that will sit asymmetrically on the page.
 // The "center" that we align the text to will be the middle of the body of text, not the middle of the page.
 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setAlignment(ParagraphAlignment.CENTER);
 paragraphFormat.setLeftIndent(100.0);
 paragraphFormat.setRightIndent(50.0);
 paragraphFormat.setSpaceAfter(25.0);

 builder.writeln(
         "This paragraph demonstrates how left and right indentation affects word wrapping.");
 builder.writeln(
         "The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

 doc.save(getArtifactsDir() + "DocumentBuilder.SetParagraphFormatting.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | El valor (en puntos) que representa la sangría izquierda del párrafo. |

### setLineSpacing(double value) {#setLineSpacing-double}
```
public void setLineSpacing(double value)
```


Establece el interlineado (en puntos) para el párrafo.

 **Remarks:** 

Cuando la propiedad [getLineSpacingRule()](../../com.aspose.words/paragraphformat/\#getLineSpacingRule) / [setLineSpacingRule(int)](../../com.aspose.words/paragraphformat/\#setLineSpacingRule-int) se establece en [LineSpacingRule.AT\_LEAST](../../com.aspose.words/linespacingrule/\#AT-LEAST), el interlineado puede ser mayor o igual, pero nunca menor que el valor especificado de [getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double).

Cuando la propiedad [getLineSpacingRule()](../../com.aspose.words/paragraphformat/\#getLineSpacingRule) / [setLineSpacingRule(int)](../../com.aspose.words/paragraphformat/\#setLineSpacingRule-int) se establece en [LineSpacingRule.EXACTLY](../../com.aspose.words/linespacingrule/\#EXACTLY), el interlineado nunca cambia del valor especificado de [getLineSpacing()](../../com.aspose.words/paragraphformat/\#getLineSpacing) / [setLineSpacing(double)](../../com.aspose.words/paragraphformat/\#setLineSpacing-double), incluso si se usa una fuente más grande dentro del párrafo.

 **Examples:** 

Muestra cómo trabajar con el interlineado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are three line spacing rules that we can define using the
 // paragraph's "LineSpacingRule" property to configure spacing between paragraphs.
 // 1 -  Set a minimum amount of spacing.
 // This will give vertical padding to lines of text of any size
 // that is too small to maintain the minimum line-height.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.AT_LEAST);
 builder.getParagraphFormat().setLineSpacing(20.0);

 builder.writeln("Minimum line spacing of 20.");
 builder.writeln("Minimum line spacing of 20.");

 // 2 -  Set exact spacing.
 // Using font sizes that are too large for the spacing will truncate the text.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.EXACTLY);
 builder.getParagraphFormat().setLineSpacing(5.0);

 builder.writeln("Line spacing of exactly 5.");
 builder.writeln("Line spacing of exactly 5.");

 // 3 -  Set spacing as a multiple of default line spacing, which is 12 points by default.
 // This kind of spacing will scale to different font sizes.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.MULTIPLE);
 builder.getParagraphFormat().setLineSpacing(18.0);

 builder.writeln("Line spacing of 1.5 default lines.");
 builder.writeln("Line spacing of 1.5 default lines.");

 doc.save(getArtifactsDir() + "ParagraphFormat.LineSpacing.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | El interlineado (en puntos) del párrafo. |

### setLineSpacingRule(int value) {#setLineSpacingRule-int}
```
public void setLineSpacingRule(int value)
```


Establece el interlineado para el párrafo.

 **Examples:** 

Muestra cómo trabajar con el interlineado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are three line spacing rules that we can define using the
 // paragraph's "LineSpacingRule" property to configure spacing between paragraphs.
 // 1 -  Set a minimum amount of spacing.
 // This will give vertical padding to lines of text of any size
 // that is too small to maintain the minimum line-height.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.AT_LEAST);
 builder.getParagraphFormat().setLineSpacing(20.0);

 builder.writeln("Minimum line spacing of 20.");
 builder.writeln("Minimum line spacing of 20.");

 // 2 -  Set exact spacing.
 // Using font sizes that are too large for the spacing will truncate the text.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.EXACTLY);
 builder.getParagraphFormat().setLineSpacing(5.0);

 builder.writeln("Line spacing of exactly 5.");
 builder.writeln("Line spacing of exactly 5.");

 // 3 -  Set spacing as a multiple of default line spacing, which is 12 points by default.
 // This kind of spacing will scale to different font sizes.
 builder.getParagraphFormat().setLineSpacingRule(LineSpacingRule.MULTIPLE);
 builder.getParagraphFormat().setLineSpacing(18.0);

 builder.writeln("Line spacing of 1.5 default lines.");
 builder.writeln("Line spacing of 1.5 default lines.");

 doc.save(getArtifactsDir() + "ParagraphFormat.LineSpacing.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El interlineado del párrafo. El valor debe ser uno de los constantes [LineSpacingRule](../../com.aspose.words/linespacingrule/). |

### setLineUnitAfter(double value) {#setLineUnitAfter-double}
```
public void setLineUnitAfter(double value)
```


Establece la cantidad de espacio (en líneas de cuadrícula) después de los párrafos.

 **Examples:** 

Muestra cómo cambiar el espaciado y las sangrías del párrafo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();

 // Below are five different spacing options, along with the properties that their configuration indirectly affects.
 // 1 -  Left indent:
 Assert.assertEquals(format.getLeftIndent(), 0.0d);

 format.setCharacterUnitLeftIndent(10.0);

 Assert.assertEquals(format.getLeftIndent(), 120.0d);

 // 2 -  Right indent:
 Assert.assertEquals(format.getRightIndent(), 0.0d);

 format.setCharacterUnitRightIndent(-5.5);

 Assert.assertEquals(format.getRightIndent(), -66.0d);

 // 3 -  Hanging indent:
 Assert.assertEquals(format.getFirstLineIndent(), 0.0d);

 format.setCharacterUnitFirstLineIndent(20.3);

 Assert.assertEquals(format.getFirstLineIndent(), 243.59d, 0.1d);

 // 4 -  Line spacing before paragraphs:
 Assert.assertEquals(format.getSpaceBefore(), 0.0d);

 format.setLineUnitBefore(5.1);

 Assert.assertEquals(format.getSpaceBefore(), 61.1d, 0.1d);

 // 5 -  Line spacing after paragraphs:
 Assert.assertEquals(format.getSpaceAfter(), 0.0d);

 format.setLineUnitAfter(10.9);

 Assert.assertEquals(format.getSpaceAfter(), 130.8d, 0.1d);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5" +
         "\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | La cantidad de espaciado (en líneas de cuadrícula) después de los párrafos. |

### setLineUnitBefore(double value) {#setLineUnitBefore-double}
```
public void setLineUnitBefore(double value)
```


Establece la cantidad de espacio (en líneas de cuadrícula) antes de los párrafos.

 **Examples:** 

Muestra cómo cambiar el espaciado y las sangrías del párrafo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();

 // Below are five different spacing options, along with the properties that their configuration indirectly affects.
 // 1 -  Left indent:
 Assert.assertEquals(format.getLeftIndent(), 0.0d);

 format.setCharacterUnitLeftIndent(10.0);

 Assert.assertEquals(format.getLeftIndent(), 120.0d);

 // 2 -  Right indent:
 Assert.assertEquals(format.getRightIndent(), 0.0d);

 format.setCharacterUnitRightIndent(-5.5);

 Assert.assertEquals(format.getRightIndent(), -66.0d);

 // 3 -  Hanging indent:
 Assert.assertEquals(format.getFirstLineIndent(), 0.0d);

 format.setCharacterUnitFirstLineIndent(20.3);

 Assert.assertEquals(format.getFirstLineIndent(), 243.59d, 0.1d);

 // 4 -  Line spacing before paragraphs:
 Assert.assertEquals(format.getSpaceBefore(), 0.0d);

 format.setLineUnitBefore(5.1);

 Assert.assertEquals(format.getSpaceBefore(), 61.1d, 0.1d);

 // 5 -  Line spacing after paragraphs:
 Assert.assertEquals(format.getSpaceAfter(), 0.0d);

 format.setLineUnitAfter(10.9);

 Assert.assertEquals(format.getSpaceAfter(), 130.8d, 0.1d);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5" +
         "\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863\u6d4b\u8bd5\u6587\u6863");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | La cantidad de espaciado (en líneas de cuadrícula) antes de los párrafos. |

### setLinesToDrop(int value) {#setLinesToDrop-int}
```
public void setLinesToDrop(int value)
```


Establece el número de líneas del texto del párrafo usadas para calcular la altura de la letra capitular.

 **Examples:** 

Muestra cómo establecer el tamaño de una letra capitular.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the "LinesToDrop" property to designate a paragraph as a drop cap,
 // which will turn it into a large capital letter that will decorate the next paragraph.
 // Give this property a value of 4 to give the drop cap the height of four text lines.
 builder.getParagraphFormat().setLinesToDrop(4);
 builder.writeln("H");

 // Reset the "LinesToDrop" property to 0 to turn the next paragraph into an ordinary paragraph.
 // The text in this paragraph will wrap around the drop cap.
 builder.getParagraphFormat().setLinesToDrop(0);
 builder.writeln("ello world!");

 doc.save(getArtifactsDir() + "ParagraphFormat.LinesToDrop.odt");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El número de líneas del texto del párrafo usadas para calcular la altura de la inicial decorativa. |

### setMirrorIndents(boolean value) {#setMirrorIndents-boolean}
```
public void setMirrorIndents(boolean value)
```


Establece una bandera que indica si las sangrías izquierda y derecha tienen la misma anchura.

 **Examples:** 

Muestra cómo hacer que los sangrados izquierdo y derecho sean iguales.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 ParagraphFormat format = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat();

 format.setMirrorIndents(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.MirrorIndents.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Una bandera que indica si las sangrías izquierda y derecha tienen la misma anchura. |

### setNoSpaceBetweenParagraphsOfSameStyle(boolean value) {#setNoSpaceBetweenParagraphsOfSameStyle-boolean}
```
public void setNoSpaceBetweenParagraphsOfSameStyle(boolean value)
```


Cuando verdadero, [getSpaceBefore()](../../com.aspose.words/paragraphformat/\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat/\#setSpaceBefore-double) y [getSpaceAfter()](../../com.aspose.words/paragraphformat/\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat/\#setSpaceAfter-double) serán ignorados entre los párrafos del mismo estilo.

 **Remarks:** 

Esta configuración solo tiene efecto cuando se aplica a un estilo de párrafo. Si se aplica directamente a un párrafo, no tiene efecto.

 **Examples:** 

Muestra cómo aplicar sin espacio entre párrafos con el mismo estilo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply a large amount of spacing before and after paragraphs that this builder will create.
 builder.getParagraphFormat().setSpaceBefore(24.0);
 builder.getParagraphFormat().setSpaceAfter(24.0);

 // Set the "NoSpaceBetweenParagraphsOfSameStyle" flag to "true" to apply
 // no spacing between paragraphs with the same style, which will group similar paragraphs.
 // Leave the "NoSpaceBetweenParagraphsOfSameStyle" flag as "false"
 // to evenly apply spacing to every paragraph.
 builder.getParagraphFormat().setNoSpaceBetweenParagraphsOfSameStyle(noSpaceBetweenParagraphsOfSameStyle);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Quote"));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));
 builder.writeln(MessageFormat.format("Paragraph in the \"{0}\" style.", builder.getParagraphFormat().getStyle().getName()));

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphSpacingSameStyle.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setOutlineLevel(int value) {#setOutlineLevel-int}
```
public void setOutlineLevel(int value)
```


Especifica el nivel de esquema del párrafo en el documento.

 **Examples:** 

Muestra cómo configurar los niveles de esquema de párrafo para crear texto plegable.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Each paragraph has an OutlineLevel, which could be any number from 1 to 9, or at the default "BodyText" value.
 // Setting the property to one of the numbered values will show an arrow to the left
 // of the beginning of the paragraph.
 builder.getParagraphFormat().setOutlineLevel(OutlineLevel.LEVEL_1);
 builder.writeln("Paragraph outline level 1.");

 // Level 1 is the topmost level. If there is a paragraph with a lower level below a paragraph with a higher level,
 // collapsing the higher-level paragraph will collapse the lower level paragraph.
 builder.getParagraphFormat().setOutlineLevel(OutlineLevel.LEVEL_2);
 builder.writeln("Paragraph outline level 2.");

 // Two paragraphs of the same level will not collapse each other,
 // and the arrows do not collapse the paragraphs they point to.
 builder.getParagraphFormat().setOutlineLevel(OutlineLevel.LEVEL_3);
 builder.writeln("Paragraph outline level 3.");
 builder.writeln("Paragraph outline level 3.");

 // The default "BodyText" value is the lowest, which a paragraph of any level can collapse.
 builder.getParagraphFormat().setOutlineLevel(OutlineLevel.BODY_TEXT);
 builder.writeln("Paragraph at main text level.");

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphOutlineLevel.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor entero correspondiente. El valor debe ser uno de los constantes [OutlineLevel](../../com.aspose.words/outlinelevel/). |

### setPageBreakBefore(boolean value) {#setPageBreakBefore-boolean}
```
public void setPageBreakBefore(boolean value)
```


Verdadero si se fuerza un salto de página antes del párrafo.

 **Examples:** 

Muestra cómo crear párrafos con saltos de página al inicio.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set this flag to "true" to apply a page break to each paragraph's beginning
 // that the document builder will create under this ParagraphFormat configuration.
 // The first paragraph will not receive a page break.
 // Leave this flag as "false" to start each new paragraph on the same page
 // as the previous, provided there is sufficient space.
 builder.getParagraphFormat().setPageBreakBefore(pageBreakBefore);

 builder.writeln("Paragraph 1.");
 builder.writeln("Paragraph 2.");

 LayoutCollector layoutCollector = new LayoutCollector(doc);
 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 if (pageBreakBefore) {
     Assert.assertEquals(1, layoutCollector.getStartPageIndex(paragraphs.get(0)));
     Assert.assertEquals(2, layoutCollector.getStartPageIndex(paragraphs.get(1)));
 } else {
     Assert.assertEquals(1, layoutCollector.getStartPageIndex(paragraphs.get(0)));
     Assert.assertEquals(1, layoutCollector.getStartPageIndex(paragraphs.get(1)));
 }

 doc.save(getArtifactsDir() + "ParagraphFormat.PageBreakBefore.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setRightIndent(double value) {#setRightIndent-double}
```
public void setRightIndent(double value)
```


Establece el valor (en puntos) que representa la sangría derecha para el párrafo.

 **Examples:** 

Muestra cómo configurar el formato de párrafo para crear texto fuera de centro.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Center all text that the document builder writes, and set up indents.
 // The indent configuration below will create a body of text that will sit asymmetrically on the page.
 // The "center" that we align the text to will be the middle of the body of text, not the middle of the page.
 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setAlignment(ParagraphAlignment.CENTER);
 paragraphFormat.setLeftIndent(100.0);
 paragraphFormat.setRightIndent(50.0);
 paragraphFormat.setSpaceAfter(25.0);

 builder.writeln(
         "This paragraph demonstrates how left and right indentation affects word wrapping.");
 builder.writeln(
         "The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

 doc.save(getArtifactsDir() + "DocumentBuilder.SetParagraphFormatting.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | El valor (en puntos) que representa la sangría derecha del párrafo. |

### setSnapToGrid(boolean value) {#setSnapToGrid-boolean}
```
public void setSnapToGrid(boolean value)
```


Especifica si el párrafo actual debe usar la configuración de líneas de cuadrícula del documento por página al organizar el contenido en el párrafo.

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
| valor | boolean | El valor  boolean  correspondiente. |

### setSpaceAfter(double value) {#setSpaceAfter-double}
```
public void setSpaceAfter(double value)
```


Establece la cantidad de espacio (en puntos) después del párrafo.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | La cantidad de espaciado (en puntos) después del párrafo. |

### setSpaceAfterAuto(boolean value) {#setSpaceAfterAuto-boolean}
```
public void setSpaceAfterAuto(boolean value)
```


Verdadero si la cantidad de espacio después del párrafo se establece automáticamente.

 **Remarks:** 

Cuando se establece en  true , anula el efecto de [getSpaceAfter()](../../com.aspose.words/paragraphformat/\#getSpaceAfter) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat/\#setSpaceAfter-double).

Cuando estableces Space Before y Space After del párrafo en Auto, Microsoft Word agrega automáticamente 14 puntos de espacio entre párrafos según las siguientes reglas:

 *  Normally, spacing is added after all paragraphs.
 *  In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
 *  In a nested bulleted or numbered list spacing is not added.
 *  Spacing is normally added after a table.
 *  Spacing is not added after a table if it is the last block in a table cell.
 *  Spacing is not added after the last paragraph in a table cell.

 **Examples:** 

Muestra cómo establecer el espaciado automático de párrafos.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply a large amount of spacing before and after paragraphs that this builder will create.
 builder.getParagraphFormat().setSpaceBefore(24.0);
 builder.getParagraphFormat().setSpaceAfter(24.0);

 // Set these flags to "true" to apply automatic spacing,
 // effectively ignoring the spacing in the properties we set above.
 // Leave them as "false" will apply our custom paragraph spacing.
 builder.getParagraphFormat().setSpaceAfterAuto(autoSpacing);
 builder.getParagraphFormat().setSpaceBeforeAuto(autoSpacing);

 // Insert two paragraphs that will have spacing above and below them and save the document.
 builder.writeln("Paragraph 1.");
 builder.writeln("Paragraph 2.");

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphSpacingAuto.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setSpaceBefore(double value) {#setSpaceBefore-double}
```
public void setSpaceBefore(double value)
```


Establece la cantidad de espacio (en puntos) antes del párrafo.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double | La cantidad de espaciado (en puntos) antes del párrafo. |

### setSpaceBeforeAuto(boolean value) {#setSpaceBeforeAuto-boolean}
```
public void setSpaceBeforeAuto(boolean value)
```


Verdadero si la cantidad de espacio antes del párrafo se establece automáticamente.

 **Remarks:** 

Cuando se establece en  true , anula el efecto de [getSpaceBefore()](../../com.aspose.words/paragraphformat/\#getSpaceBefore) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat/\#setSpaceBefore-double).

Cuando estableces Space Before y Space After del párrafo en Auto, Microsoft Word agrega automáticamente 14 puntos de espacio entre párrafos según las siguientes reglas:

 *  Normally, spacing is added after all paragraphs.
 *  In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
 *  In a nested bulleted or numbered list spacing is not added.
 *  Spacing is normally added after a table.
 *  Spacing is not added after a table if it is the last block in a table cell.
 *  Spacing is not added after the last paragraph in a table cell.

 **Examples:** 

Muestra cómo establecer el espaciado automático de párrafos.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply a large amount of spacing before and after paragraphs that this builder will create.
 builder.getParagraphFormat().setSpaceBefore(24.0);
 builder.getParagraphFormat().setSpaceAfter(24.0);

 // Set these flags to "true" to apply automatic spacing,
 // effectively ignoring the spacing in the properties we set above.
 // Leave them as "false" will apply our custom paragraph spacing.
 builder.getParagraphFormat().setSpaceAfterAuto(autoSpacing);
 builder.getParagraphFormat().setSpaceBeforeAuto(autoSpacing);

 // Insert two paragraphs that will have spacing above and below them and save the document.
 builder.writeln("Paragraph 1.");
 builder.writeln("Paragraph 2.");

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphSpacingAuto.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setStyle(Style value) {#setStyle-com.aspose.words.Style}
```
public void setStyle(Style value)
```


Establece el estilo de párrafo aplicado a este formato.

 **Examples:** 

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

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | [Style](../../com.aspose.words/style/) | El estilo de párrafo aplicado a este formato. |

### setStyleIdentifier(int value) {#setStyleIdentifier-int}
```
public void setStyleIdentifier(int value)
```


Establece el identificador de estilo independiente de la configuración regional del estilo de párrafo aplicado a este formato.

 **Examples:** 

Muestra cómo insertar una tabla de contenido (TOC) en un documento usando estilos de encabezado como entradas.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a table of contents for the first page of the document.
 // Configure the table to pick up paragraphs with headings of levels 1 to 3.
 // Also, set its entries to be hyperlinks that will take us
 // to the location of the heading when left-clicked in Microsoft Word.
 builder.insertTableOfContents("\\o \"1-3\" \\h \\z \\u");
 builder.insertBreak(BreakType.PAGE_BREAK);

 // Populate the table of contents by adding paragraphs with heading styles.
 // Each such heading with a level between 1 and 3 will create an entry in the table.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("Heading 1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 1.1");
 builder.writeln("Heading 1.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("Heading 2");
 builder.writeln("Heading 3");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 3.1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_3);
 builder.writeln("Heading 3.1.1");
 builder.writeln("Heading 3.1.2");
 builder.writeln("Heading 3.1.3");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_4);
 builder.writeln("Heading 3.1.3.1");
 builder.writeln("Heading 3.1.3.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 3.2");
 builder.writeln("Heading 3.3");

 // A table of contents is a field of a type that needs to be updated to show an up-to-date result.
 doc.updateFields();
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertToc.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El identificador de estilo independiente de la configuración regional del estilo de párrafo aplicado a este formato. El valor debe ser uno de los constantes [StyleIdentifier](../../com.aspose.words/styleidentifier/). |

### setStyleName(String value) {#setStyleName-java.lang.String}
```
public void setStyleName(String value)
```


Establece el nombre del estilo de párrafo aplicado a este formato.

 **Examples:** 

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
| valor | java.lang.String | El nombre del estilo de párrafo aplicado a este formato. |

### setSuppressAutoHyphens(boolean value) {#setSuppressAutoHyphens-boolean}
```
public void setSuppressAutoHyphens(boolean value)
```


Especifica si el párrafo actual debe estar exento de cualquier guionado que se aplique en la configuración del documento.

 **Examples:** 

Muestra cómo suprimir la guionización de un párrafo.

```

 Hyphenation.registerDictionary("de-CH", getMyDir() + "hyph_de_CH.dic");

 Assert.assertTrue(Hyphenation.isDictionaryRegistered("de-CH"));

 // Open a document containing text with a locale matching that of our dictionary.
 // When we save this document to a fixed page save format, its text will have hyphenation.
 Document doc = new Document(getMyDir() + "German text.docx");

 // We can set the "SuppressAutoHyphens" property to "true" to disable hyphenation
 // for a specific paragraph while keeping it enabled for the rest of the document.
 // The default value for this property is "false",
 // which means every paragraph by default uses hyphenation if any is available.
 doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().setSuppressAutoHyphens(suppressAutoHyphens);

 doc.save(getArtifactsDir() + "ParagraphFormat.SuppressHyphens.pdf");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setSuppressLineNumbers(boolean value) {#setSuppressLineNumbers-boolean}
```
public void setSuppressLineNumbers(boolean value)
```


Especifica si las líneas del párrafo actual deben estar exentas de la numeración de líneas que se aplica en la sección principal.

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
| valor | boolean | El valor  boolean  correspondiente. |

### setWidowControl(boolean value) {#setWidowControl-boolean}
```
public void setWidowControl(boolean value)
```


Verdadero si la primera y la última línea del párrafo deben permanecer en la misma página que el resto del párrafo.

 **Examples:** 

Muestra cómo habilitar el control de viudas y huérfanas para un párrafo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // When we write the text that does not fit onto one page, one line may spill over onto the next page.
 // The single line that ends up on the next page is called an "Orphan",
 // and the previous line where the orphan broke off is called a "Widow".
 // We can fix orphans and widows by rearranging text via font size, spacing, or page margins.
 // If we wish to preserve our document's dimensions, we can set this flag to "true"
 // to push widows onto the same page as their respective orphans.
 // Leave this flag as "false" will leave widow/orphan pairs in text.
 // Every paragraph has this setting accessible in Microsoft Word via Home -> Paragraph -> Paragraph Settings
 // (button on bottom right hand corner of "Paragraph" tab) -> "Widow/Orphan control".
 builder.getParagraphFormat().setWidowControl(widowControl);

 // Insert text that produces an orphan and a widow.
 builder.getFont().setSize(68.0);
 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "ParagraphFormat.WidowControl.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setWordWrap(boolean value) {#setWordWrap-boolean}
```
public void setWordWrap(boolean value)
```


Si esta propiedad es  false , el texto latino en medio de una palabra puede dividirse en el párrafo actual. De lo contrario, el texto latino se divide por palabras completas.

 **Examples:** 

Muestra cómo establecer propiedades especiales para la tipografía asiática.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat();
 format.setFarEastLineBreakControl(true);
 format.setWordWrap(false);
 format.setHangingPunctuation(true);

 doc.save(getArtifactsDir() + "ParagraphFormat.AsianTypographyProperties.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

