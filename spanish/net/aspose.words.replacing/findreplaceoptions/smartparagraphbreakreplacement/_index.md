---
title: FindReplaceOptions.SmartParagraphBreakReplacement
linktitle: SmartParagraphBreakReplacement
articleTitle: SmartParagraphBreakReplacement
second_title: Aspose.Words para .NET
description: FindReplaceOptions SmartParagraphBreakReplacement propiedad. Obtiene o establece un valor booleano que indica que se permite reemplazar el párrafo break cuando no hay un siguiente párrafo hermano en C#.
type: docs
weight: 160
url: /es/net/aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/
---
## FindReplaceOptions.SmartParagraphBreakReplacement property

Obtiene o establece un valor booleano que indica que se permite reemplazar el párrafo break cuando no hay un siguiente párrafo hermano.

El valor predeterminado es`FALSO`.

```csharp
public bool SmartParagraphBreakReplacement { get; set; }
```

## Observaciones

Esta opción permite reemplazar el salto de párrafo cuando no hay un siguiente párrafo hermano al que se puedan mover todos los nodos child , al encontrar cualquier párrafo siguiente (no necesariamente hermano) después del párrafo que se reemplaza.

## Ejemplos

Muestra cómo eliminar un párrafo de una celda de una tabla con una tabla anidada.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea una tabla con un párrafo y una tabla interna en la primera celda.
builder.StartTable();
builder.InsertCell();
builder.Write("TEXT1");
builder.StartTable();
builder.InsertCell();
builder.EndTable();
builder.EndTable();
builder.Writeln();

FindReplaceOptions options = new FindReplaceOptions();
// Cuando la siguiente opción se establece en "verdadero", Aspose.Words eliminará el texto del párrafo
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
