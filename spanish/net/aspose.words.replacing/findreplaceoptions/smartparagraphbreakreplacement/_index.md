---
title: FindReplaceOptions.SmartParagraphBreakReplacement
linktitle: SmartParagraphBreakReplacement
articleTitle: SmartParagraphBreakReplacement
second_title: Aspose.Words para .NET
description: Descubra la propiedad SmartParagraphBreakReplacement en FindReplaceOptions. Controle fácilmente los saltos de párrafo para un formato de texto perfecto.
type: docs
weight: 170
url: /es/net/aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/
---
## FindReplaceOptions.SmartParagraphBreakReplacement property

Obtiene o establece un valor booleano que indica que está permitido reemplazar el párrafo break cuando no hay un siguiente párrafo hermano.

El valor predeterminado es`FALSO`.

```csharp
public bool SmartParagraphBreakReplacement { get; set; }
```

## Observaciones

Esta opción permite reemplazar el salto de párrafo cuando no hay un siguiente párrafo hermano al cual se puedan mover todos los nodos secundarios, encontrando cualquier párrafo siguiente (no necesariamente hermano) después del párrafo que se está reemplazando.

## Ejemplos

Muestra cómo eliminar un párrafo de una celda de una tabla con una tabla anidada.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea una tabla con párrafo y tabla interna en la primera celda.
builder.StartTable();
builder.InsertCell();
builder.Write("TEXT1");
builder.StartTable();
builder.InsertCell();
builder.EndTable();
builder.EndTable();
builder.Writeln();

FindReplaceOptions options = new FindReplaceOptions();
// Cuando la siguiente opción se establece en 'verdadero', Aspose.Words eliminará el texto del párrafo
// completamente con su marca de párrafo. De lo contrario, Aspose.Words imitará a Word y eliminará
// solo el texto del párrafo y deja la marca de párrafo intacta (cuando una tabla sigue al texto).
options.SmartParagraphBreakReplacement = isSmartParagraphBreakReplacement;
doc.Range.Replace(new Regex(@"TEXT1&p"), "", options);

doc.Save(ArtifactsDir + "Table.RemoveParagraphTextAndMark.docx");
```

### Ver también

* class [FindReplaceOptions](../)
* espacio de nombres [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* asamblea [Aspose.Words](../../../)
