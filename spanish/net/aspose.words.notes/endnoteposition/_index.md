---
title: EndnotePosition Enum
linktitle: EndnotePosition
articleTitle: EndnotePosition
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words EndnotePosition para obtener un control preciso sobre la ubicación de las notas finales en los documentos, mejorando sus capacidades de formato de texto.
type: docs
weight: 4940
url: /es/net/aspose.words.notes/endnoteposition/
---
## EndnotePosition enumeration

Define la posición de la nota final.

```csharp
public enum EndnotePosition
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| EndOfSection | `0` | Las notas finales se muestran al final de la sección. |
| EndOfDocument | `3` | Las notas finales se muestran al final del documento. |

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

### Ver también

* class [EndnoteOptions](../endnoteoptions/)
* espacio de nombres [Aspose.Words.Notes](../../aspose.words.notes/)
* asamblea [Aspose.Words](../../)
