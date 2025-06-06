---
title: FootnotePosition Enum
linktitle: FootnotePosition
articleTitle: FootnotePosition
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Notes.FootnotePosition para la colocación personalizable de notas al pie, mejorando el formato y la legibilidad del documento.
type: docs
weight: 4980
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
| BottomOfPage | `1` | Las notas al pie se muestran en la parte inferior de cada página. |
| BeneathText | `2` | Las notas al pie se muestran debajo del texto en cada página. |

## Ejemplos

Muestra cómo seleccionar un lugar diferente donde el documento recopila y muestra sus notas al pie.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Una nota al pie es una forma de adjuntar una referencia o un comentario al margen del texto.
 // que no interfiera con el flujo del texto del cuerpo principal.
// Insertar una nota al pie agrega un pequeño símbolo de referencia en superíndice
// en el cuerpo principal del texto donde insertamos la nota al pie.
// Cada nota al pie también crea una entrada en la parte inferior de la página, que consiste en un símbolo
// que coincide con el símbolo de referencia en el texto del cuerpo principal.
// El texto de referencia que pasamos al método "InsertFootnote" del generador de documentos.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

//Podemos utilizar la propiedad "Posición" para determinar dónde colocará el documento todas sus notas al pie.
// Si establecemos el valor de la propiedad "Posición" en "FootnotePosition.BottomOfPage",
Cada nota al pie se mostrará al final de la página que contiene su marca de referencia. Este es el valor predeterminado.
// Si establecemos el valor de la propiedad "Posición" en "FootnotePosition.BeneathText",
// Cada nota al pie aparecerá al final del texto de la página que contiene su marca de referencia.
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

### Ver también

* class [FootnoteOptions](../footnoteoptions/)
* espacio de nombres [Aspose.Words.Notes](../../aspose.words.notes/)
* asamblea [Aspose.Words](../../)
