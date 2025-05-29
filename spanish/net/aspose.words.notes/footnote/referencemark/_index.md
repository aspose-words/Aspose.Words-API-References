---
title: Footnote.ReferenceMark
linktitle: ReferenceMark
articleTitle: ReferenceMark
second_title: Aspose.Words para .NET
description: Personaliza tus notas al pie con la propiedad ReferenceMark. Define fácilmente marcadores únicos para mayor claridad y organización en tus documentos. ¡Mejora la legibilidad hoy mismo!
type: docs
weight: 60
url: /es/net/aspose.words.notes/footnote/referencemark/
---
## Footnote.ReferenceMark property

Obtiene/establece la marca de referencia personalizada que se utilizará para esta nota al pie. El valor predeterminado es**cadena vacía** (Empty ), lo que significa que se utilizan notas al pie numeradas automáticamente.

```csharp
public string ReferenceMark { get; set; }
```

## Observaciones

Si esta propiedad está establecida en**cadena vacía** (Empty ) o`nulo` , entonces[`IsAuto`](../isauto/) La propiedad se establecerá automáticamente en`verdadero` , si se establece en cualquier otro valor entonces[`IsAuto`](../isauto/) se establecerá en`FALSO` .

El formato RTF solo puede almacenar 1 símbolo como marca de referencia personalizada, por lo que al exportar solo se escribirá el primer símbolo y los demás se descartarán.

## Ejemplos

Muestra cómo insertar y personalizar notas al pie.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Agregue texto y referencialo con una nota al pie. Esta nota al pie colocará una pequeña referencia en superíndice.
// marca después del texto al que hace referencia y crea una entrada debajo del texto del cuerpo principal en la parte inferior de la página.
// Esta entrada contendrá la marca de referencia de la nota al pie y el texto de referencia,
// que pasaremos al método "InsertFootnote" del generador de documentos.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Si esta propiedad se establece en "verdadero", entonces la marca de referencia de nuestra nota al pie
// será su índice entre todas las notas a pie de página de la sección.
//Esta es la primera nota a pie de página, por lo que la marca de referencia será "1".
Assert.True(footnote.IsAuto);

 //Podemos mover el generador de documentos dentro de la nota al pie para editar su texto de referencia.
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

//Podemos establecer una marca de referencia personalizada que la nota al pie utilizará en lugar de su número de índice.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// Un marcador con el indicador "IsAuto" establecido como verdadero seguirá mostrando su índice real
// incluso si los marcadores anteriores muestran marcas de referencia personalizadas, la marca de referencia de este marcador será un "3".
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### Ver también

* class [Footnote](../)
* espacio de nombres [Aspose.Words.Notes](../../../aspose.words.notes/)
* asamblea [Aspose.Words](../../../)
