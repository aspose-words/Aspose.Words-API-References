---
title: Enum FootnotePosition
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Notes.FootnotePosition enumeración. Define la posición de la nota al pie.
type: docs
weight: 4290
url: /es/net/aspose.words.notes/footnoteposition/
---
## FootnotePosition enumeration

Define la posición de la nota al pie.

```csharp
public enum FootnotePosition
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| BottomOfPage | `1` | Las notas a pie de página se publican en la parte inferior de cada página. |
| BeneathText | `2` | Las notas a pie de página se muestran debajo del texto de cada página. |

### Ejemplos

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

### Ver también

* class [FootnoteOptions](../footnoteoptions/)
* espacio de nombres [Aspose.Words.Notes](../../aspose.words.notes/)
* asamblea [Aspose.Words](../../)


