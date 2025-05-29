---
title: EndnoteOptions.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad Posición de EndnoteOptions mejora el diseño de su documento al especificar la ubicación ideal para las notas finales. ¡Optimice su escritura hoy mismo!
type: docs
weight: 20
url: /es/net/aspose.words.notes/endnoteoptions/position/
---
## EndnoteOptions.Position property

Especifica la posición de las notas finales.

```csharp
public EndnotePosition Position { get; set; }
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

### Ver también

* enum [EndnotePosition](../../endnoteposition/)
* class [EndnoteOptions](../)
* espacio de nombres [Aspose.Words.Notes](../../../aspose.words.notes/)
* asamblea [Aspose.Words](../../../)
