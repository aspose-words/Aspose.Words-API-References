---
title: FootnoteType Enum
linktitle: FootnoteType
articleTitle: FootnoteType
second_title: Aspose.Words para .NET
description: Aspose.Words.Notes.FootnoteType enumeración. Especifica si se trata de una nota al pie o una nota al final en C#.
type: docs
weight: 4300
url: /es/net/aspose.words.notes/footnotetype/
---
## FootnoteType enumeration

Especifica si se trata de una nota al pie o una nota al final.

```csharp
public enum FootnoteType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Footnote | `0` | El objeto es una nota al pie. |
| Endnote | `1` | El objeto es una nota al final. |

## Observaciones

Tanto las notas a pie de página como las notas al final están representadas por objetos mediante elFootnote clase. Usar[`FootnoteType`](../footnote/footnotetype/) para distinguir entre notas al pie y notas al final.

## Ejemplos

Muestra cómo hacer referencia al texto con una nota al pie y una nota al final.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta algo de texto y márcalo con una nota al pie con la propiedad IsAuto establecida en "verdadero" de forma predeterminada,
// por lo que el marcador que se ve en el cuerpo del texto se numerará automáticamente en "1",
// y la nota al pie aparecerá al final de la página.
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// Inserta más texto y márcalo con una nota al final con una marca de referencia personalizada,
// que se utilizará en lugar del número "2" y establecerá "IsAuto" en falso.
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// Las notas a pie de página siempre aparecen al final del texto al que se hace referencia,
// por lo que este salto de página no afectará a la nota al pie.
// Por otro lado, las notas finales siempre están al final del documento.
// para que este salto de página empuje la nota final a la página siguiente.
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
```

Muestra cómo insertar y personalizar notas al pie.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Agrega texto y haz referencia a él con una nota al pie. Esta nota al pie colocará una pequeña referencia en superíndice.
// marque después del texto al que hace referencia y cree una entrada debajo del texto del cuerpo principal en la parte inferior de la página.
// Esta entrada contendrá la marca de referencia de la nota al pie y el texto de referencia,
// que pasaremos al método "InsertFootnote" del generador de documentos.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Si esta propiedad se establece en "verdadero", entonces la marca de referencia de nuestra nota al pie
// será su índice entre todas las notas a pie de página de la sección.
// Esta es la primera nota a pie de página, por lo que la marca de referencia será "1".
Assert.True(footnote.IsAuto);

 // Podemos mover el generador de documentos dentro de la nota al pie para editar su texto de referencia.
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Podemos establecer una marca de referencia personalizada que usará la nota al pie en lugar de su número de índice.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// Un marcador con el indicador "IsAuto" establecido en verdadero seguirá mostrando su índice real
// incluso si los marcadores anteriores muestran marcas de referencia personalizadas, la marca de referencia de este marcador será un "3".
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Notes](../../aspose.words.notes/)
* asamblea [Aspose.Words](../../)
