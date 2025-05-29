---
title: EndnoteOptions.NumberStyle
linktitle: NumberStyle
articleTitle: NumberStyle
second_title: Aspose.Words para .NET
description: Descubra la propiedad EndnoteOptions NumberStyle para personalizar fácilmente el formato numérico de sus notas finales. ¡Mejore la profesionalidad de sus documentos hoy mismo!
type: docs
weight: 10
url: /es/net/aspose.words.notes/endnoteoptions/numberstyle/
---
## EndnoteOptions.NumberStyle property

Especifica el formato de número para las notas finales numeradas automáticamente.

```csharp
public NumberStyle NumberStyle { get; set; }
```

## Observaciones

No todos los estilos de número son aplicables a esta propiedad. Para ver la lista de estilos de número aplicables, consulte el cuadro de diálogo Insertar nota al pie o nota al final de Microsoft Word. Si selecciona un estilo de número no aplicable, Microsoft Word volverá a su valor predeterminado.

## Ejemplos

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

### Ver también

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [EndnoteOptions](../)
* espacio de nombres [Aspose.Words.Notes](../../../aspose.words.notes/)
* asamblea [Aspose.Words](../../../)
