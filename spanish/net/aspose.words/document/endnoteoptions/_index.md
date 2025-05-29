---
title: Document.EndnoteOptions
linktitle: EndnoteOptions
articleTitle: EndnoteOptions
second_title: Aspose.Words para .NET
description: Explore la propiedad EndnoteOptions para personalizar la numeración y el posicionamiento de las notas finales, mejorando la claridad y el profesionalismo de su documento.
type: docs
weight: 120
url: /es/net/aspose.words/document/endnoteoptions/
---
## Document.EndnoteOptions property

Proporciona opciones que controlan la numeración y la posición de las notas finales en este documento.

```csharp
public EndnoteOptions EndnoteOptions { get; }
```

## Ejemplos

Muestra cómo seleccionar un lugar diferente donde el documento recopila y muestra sus notas finales.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Una nota final es una forma de adjuntar una referencia o un comentario al margen del texto.
 // que no interfiera con el flujo del texto del cuerpo principal.
// Insertar una nota final agrega un pequeño símbolo de referencia en superíndice
// en el cuerpo principal del texto donde insertamos la nota final.
// Cada nota final también crea una entrada al final del documento, que consiste en un símbolo
// que coincide con el símbolo de referencia en el texto del cuerpo principal.
// El texto de referencia que pasamos al método "InsertEndnote" del generador de documentos.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote contents.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("This is the second section.");

//Podemos utilizar la propiedad "Posición" para determinar dónde colocará el documento todas sus notas finales.
// Si establecemos el valor de la propiedad "Posición" en "EndnotePosition.EndOfDocument",
Cada nota al pie se mostrará en una colección al final del documento. Este es el valor predeterminado.
// Si establecemos el valor de la propiedad "Posición" en "EndnotePosition.EndOfSection",
// Cada nota al pie aparecerá en una colección al final de la sección cuyo texto contiene la marca de referencia de la nota final.
doc.EndnoteOptions.Position = endnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionEndnote.docx");
```

Muestra cómo establecer un número en el que el documento inicia el recuento de notas al pie/notas finales.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Las notas a pie de página y las notas finales son una forma de adjuntar una referencia o un comentario al margen del texto.
 // que no interfiera con el flujo del texto del cuerpo principal.
// Insertar una nota al pie o una nota final agrega un pequeño símbolo de referencia en superíndice
// en el cuerpo principal del texto donde insertamos la nota al pie/nota final.
// Cada nota al pie/nota final también crea una entrada, que consta de un símbolo
// que coincide con el símbolo de referencia en el texto del cuerpo principal.
// El texto de referencia que pasamos al método "InsertEndnote" del generador de documentos.
// Las entradas de notas al pie, de forma predeterminada, aparecen en la parte inferior de cada página que contiene
// sus símbolos de referencia y notas finales aparecen al final del documento.
builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.");

builder.InsertParagraph();

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.");

// De forma predeterminada, el símbolo de referencia para cada nota al pie y nota final es su índice.
// entre todas las notas al pie y al final del documento. Cada documento mantiene recuentos separados.
// para notas a pie de página y para notas finales, que comienzan ambas en 1.
Assert.AreEqual(1, doc.FootnoteOptions.StartNumber);
Assert.AreEqual(1, doc.EndnoteOptions.StartNumber);

// Podemos usar la propiedad "StartNumber" para obtener el documento
// comienza un recuento de notas al pie o notas finales en un número diferente.
doc.EndnoteOptions.NumberStyle = NumberStyle.Arabic;
doc.EndnoteOptions.StartNumber = 50;

doc.Save(ArtifactsDir + "InlineStory.StartNumber.docx");
```

Muestra cómo cambiar el estilo de número de las marcas de referencia de notas al pie/notas finales.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Las notas a pie de página y las notas finales son una forma de adjuntar una referencia o un comentario al margen del texto.
 // que no interfiera con el flujo del texto del cuerpo principal.
// Insertar una nota al pie o una nota final agrega un pequeño símbolo de referencia en superíndice
// en el cuerpo principal del texto donde insertamos la nota al pie/nota final.
// Cada nota al pie/nota final también crea una entrada, que consiste en un símbolo que coincide con la referencia.
// Símbolo en el cuerpo principal del texto. El texto de referencia que pasamos al método "InsertEndnote" del generador de documentos.
// Las entradas de notas al pie, de forma predeterminada, aparecen en la parte inferior de cada página que contiene
// sus símbolos de referencia y notas finales aparecen al final del documento.
builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.", "Custom footnote reference mark");

builder.InsertParagraph();

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.", "Custom endnote reference mark");

// De forma predeterminada, el símbolo de referencia para cada nota al pie y nota final es su índice.
// entre todas las notas al pie y al final del documento. Cada documento mantiene recuentos separados.
// para notas al pie y notas finales. Por defecto, las notas al pie se numeran en números arábigos.
// y las notas finales muestran sus números en números romanos en minúscula.
Assert.AreEqual(NumberStyle.Arabic, doc.FootnoteOptions.NumberStyle);
Assert.AreEqual(NumberStyle.LowercaseRoman, doc.EndnoteOptions.NumberStyle);

// Podemos utilizar la propiedad "NumberStyle" para aplicar estilos de numeración personalizados a notas al pie y notas finales.
// Esto no afectará a las notas al pie/notas finales con marcas de referencia personalizadas.
doc.FootnoteOptions.NumberStyle = NumberStyle.UppercaseRoman;
doc.EndnoteOptions.NumberStyle = NumberStyle.UppercaseLetter;

doc.Save(ArtifactsDir + "InlineStory.RefMarkNumberStyle.docx");
```

Muestra cómo reiniciar la numeración de notas al pie y notas finales en determinados lugares del documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Las notas a pie de página y las notas finales son una forma de adjuntar una referencia o un comentario al margen del texto.
 // que no interfiera con el flujo del texto del cuerpo principal.
// Insertar una nota al pie o una nota final agrega un pequeño símbolo de referencia en superíndice
// en el cuerpo principal del texto donde insertamos la nota al pie/nota final.
// Cada nota al pie/nota final también crea una entrada, que consiste en un símbolo que coincide con la referencia.
// Símbolo en el cuerpo principal del texto. El texto de referencia que pasamos al método "InsertEndnote" del generador de documentos.
// Las entradas de notas al pie, de forma predeterminada, aparecen en la parte inferior de cada página que contiene
// sus símbolos de referencia y notas finales aparecen al final del documento.
builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.");
builder.Write("Text 4. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 4.");

builder.InsertBreak(BreakType.PageBreak);

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.");
builder.Write("Text 4. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 4.");

// De forma predeterminada, el símbolo de referencia para cada nota al pie y nota final es su índice.
// entre todas las notas al pie y al final del documento. Cada documento mantiene recuentos separados.
// para notas al pie y notas finales y no reinicia estos recuentos en ningún momento.
Assert.AreEqual(doc.FootnoteOptions.RestartRule, FootnoteNumberingRule.Default);
Assert.AreEqual(FootnoteNumberingRule.Default, FootnoteNumberingRule.Continuous);

// Podemos usar la propiedad "RestartRule" para que el documento se reinicie
// La nota al pie o nota final cuenta en una nueva página o sección.
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

### Ver también

* class [EndnoteOptions](../../../aspose.words.notes/endnoteoptions/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
