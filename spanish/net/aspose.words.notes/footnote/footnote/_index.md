---
title: Footnote
linktitle: Footnote
articleTitle: Footnote
second_title: Aspose.Words para .NET
description: Footnote constructor. Inicializa una instancia delFootnote clase en C#.
type: docs
weight: 10
url: /es/net/aspose.words.notes/footnote/footnote/
---
## Footnote constructor

Inicializa una instancia del[`Footnote`](../) clase.

```csharp
public Footnote(DocumentBase doc, FootnoteType footnoteType)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| doc | DocumentBase | El documento del propietario. |
| footnoteType | FootnoteType | A[`FootnoteType`](../footnotetype/) value que especifica si se trata de una nota al pie o al final. |

## Observaciones

Cuando[`Footnote`](../) se crea, pertenece al documento especificado, pero aún no es parte del documento y[`ParentNode`](../../../aspose.words/node/parentnode/) es`nulo`.

Para anexar[`Footnote`](../) al uso del documento[`InsertAfter`](../../../aspose.words/compositenode/insertafter/) o[`InsertBefore`](../../../aspose.words/compositenode/insertbefore/) en el párrafo donde desea insertar la nota al pie.

## Ejemplos

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

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [FootnoteType](../../footnotetype/)
* class [Footnote](../)
* espacio de nombres [Aspose.Words.Notes](../../../aspose.words.notes/)
* asamblea [Aspose.Words](../../../)
