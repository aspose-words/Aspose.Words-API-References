---
title: Class FootnoteOptions
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Notes.FootnoteOptions clase. Representa las opciones de numeración de notas al pie de un documento o sección.
type: docs
weight: 4280
url: /es/net/aspose.words.notes/footnoteoptions/
---
## FootnoteOptions class

Representa las opciones de numeración de notas al pie de un documento o sección.

Para obtener más información, visite el[Trabajar con notas al pie y notas finales](https://docs.aspose.com/words/net/working-with-footnote-and-endnote/) artículo de documentación.

```csharp
public sealed class FootnoteOptions
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Columns](../../aspose.words.notes/footnoteoptions/columns/) { get; set; } | Especifica el número de columnas con las que se formatea el área de notas al pie. |
| [NumberStyle](../../aspose.words.notes/footnoteoptions/numberstyle/) { get; set; } | Especifica el formato numérico para las notas al pie numeradas automáticamente. |
| [Position](../../aspose.words.notes/footnoteoptions/position/) { get; set; } | Especifica la posición de las notas al pie. |
| [RestartRule](../../aspose.words.notes/footnoteoptions/restartrule/) { get; set; } | Determina cuándo se reinicia la numeración automática. |
| [StartNumber](../../aspose.words.notes/footnoteoptions/startnumber/) { get; set; } | Especifica el número o carácter inicial de las primeras notas al pie numeradas automáticamente. |

### Ejemplos

Muestra cómo dividir la sección de notas al pie en un número determinado de columnas.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");
doc.FootnoteOptions.Columns = 2;
doc.Save(ArtifactsDir + "Document.FootnoteColumns.docx");
```

Muestra cómo seleccionar un lugar diferente donde el documento recopila y muestra sus notas a pie de página.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Una nota al pie es una forma de adjuntar una referencia o un comentario lateral al texto
 // que no interfiere con el flujo del texto del cuerpo principal.
// Al insertar una nota al pie se agrega un pequeño símbolo de referencia en superíndice
// en el cuerpo principal del texto donde insertamos la nota al pie.
// Cada nota al pie también crea una entrada en la parte inferior de la página, que consta de un símbolo
// que coincide con el símbolo de referencia en el texto del cuerpo principal.
// El texto de referencia que pasamos al método "InsertFootnote" del creador de documentos.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// Podemos usar la propiedad "Posición" para determinar dónde colocará el documento todas sus notas al pie.
// Si establecemos el valor de la propiedad "Position" en "FootnotePosition.BottomOfPage",
// cada nota al pie aparecerá en la parte inferior de la página que contiene su marca de referencia. Este es el valor predeterminado.
// Si establecemos el valor de la propiedad "Position" en "FootnotePosition.BeneathText",
// cada nota al pie aparecerá al final del texto de la página que contiene su marca de referencia.
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

Muestra cómo establecer un número en el que el documento comienza el recuento de notas al pie/notas al final.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Las notas al pie y al final son una forma de adjuntar una referencia o un comentario lateral al texto
 // que no interfiere con el flujo del texto del cuerpo principal.
// Insertar una nota al pie/nota al final agrega un pequeño símbolo de referencia en superíndice
// en el cuerpo principal del texto donde insertamos la nota al pie/nota al final.
// Cada nota al pie/nota al final también crea una entrada, que consta de un símbolo
// que coincide con el símbolo de referencia en el texto del cuerpo principal.
// El texto de referencia que pasamos al método "InsertEndnote" del creador de documentos.
// Las entradas de notas al pie, de forma predeterminada, aparecen en la parte inferior de cada página que contiene
// sus símbolos de referencia y las notas finales aparecen al final del documento.
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

// De forma predeterminada, el símbolo de referencia para cada nota al pie y nota al final es su índice
// entre todas las notas al pie/notas finales del documento. Cada documento mantiene recuentos separados
// para notas a pie de página y notas finales, que comienzan en 1.
Assert.AreEqual(1, doc.FootnoteOptions.StartNumber);
Assert.AreEqual(1, doc.EndnoteOptions.StartNumber);

// Podemos usar la propiedad "StartNumber" para obtener el documento
// comenzar un recuento de notas al pie o al final en un número diferente.
doc.EndnoteOptions.NumberStyle = NumberStyle.Arabic;
doc.EndnoteOptions.StartNumber = 50;

doc.Save(ArtifactsDir + "InlineStory.StartNumber.docx");
```

Muestra cómo cambiar el estilo numérico de las marcas de referencia de notas al pie/notas al final.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Las notas al pie y al final son una forma de adjuntar una referencia o un comentario lateral al texto
 // que no interfiere con el flujo del texto del cuerpo principal.
// Insertar una nota al pie/nota al final agrega un pequeño símbolo de referencia en superíndice
// en el cuerpo principal del texto donde insertamos la nota al pie/nota al final.
// Cada nota al pie/nota al final también crea una entrada, que consta de un símbolo que coincide con la referencia
// símbolo en el texto del cuerpo principal. El texto de referencia que pasamos al método "InsertEndnote" del generador de documentos.
// Las entradas de notas al pie, de forma predeterminada, aparecen en la parte inferior de cada página que contiene
// sus símbolos de referencia y las notas finales aparecen al final del documento.
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

// De forma predeterminada, el símbolo de referencia para cada nota al pie y nota al final es su índice
// entre todas las notas al pie/notas finales del documento. Cada documento mantiene recuentos separados
// para notas a pie de página y para notas finales. De forma predeterminada, las notas a pie de página muestran sus números utilizando números arábigos,
// y las notas finales muestran sus números en números romanos minúsculas.
Assert.AreEqual(NumberStyle.Arabic, doc.FootnoteOptions.NumberStyle);
Assert.AreEqual(NumberStyle.LowercaseRoman, doc.EndnoteOptions.NumberStyle);

// Podemos usar la propiedad "NumberStyle" para aplicar estilos de numeración personalizados a notas al pie y notas al final.
// Esto no afectará las notas al pie/notas al final con marcas de referencia personalizadas.
doc.FootnoteOptions.NumberStyle = NumberStyle.UppercaseRoman;
doc.EndnoteOptions.NumberStyle = NumberStyle.UppercaseLetter;

doc.Save(ArtifactsDir + "InlineStory.RefMarkNumberStyle.docx");
```

Muestra cómo reiniciar la numeración de notas al pie/notas al final en ciertos lugares del documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Las notas al pie y al final son una forma de adjuntar una referencia o un comentario lateral al texto
 // que no interfiere con el flujo del texto del cuerpo principal.
// Insertar una nota al pie/nota al final agrega un pequeño símbolo de referencia en superíndice
// en el cuerpo principal del texto donde insertamos la nota al pie/nota al final.
// Cada nota al pie/nota al final también crea una entrada, que consta de un símbolo que coincide con la referencia
// símbolo en el texto del cuerpo principal. El texto de referencia que pasamos al método "InsertEndnote" del generador de documentos.
// Las entradas de notas al pie, de forma predeterminada, aparecen en la parte inferior de cada página que contiene
// sus símbolos de referencia y las notas finales aparecen al final del documento.
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

// De forma predeterminada, el símbolo de referencia para cada nota al pie y nota al final es su índice
// entre todas las notas al pie/notas finales del documento. Cada documento mantiene recuentos separados
// para notas a pie de página y notas finales y no reinicia estos conteos en ningún momento.
Assert.AreEqual(doc.FootnoteOptions.RestartRule, FootnoteNumberingRule.Default);
Assert.AreEqual(FootnoteNumberingRule.Default, FootnoteNumberingRule.Continuous);

// Podemos usar la propiedad "RestartRule" para que el documento se reinicie
// la nota al pie/nota al final cuenta en una nueva página o sección.
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

### Ver también

* property [FootnoteOptions](../../aspose.words/document/footnoteoptions/)
* property [FootnoteOptions](../../aspose.words/pagesetup/footnoteoptions/)
* espacio de nombres [Aspose.Words.Notes](../../aspose.words.notes/)
* asamblea [Aspose.Words](../../)


