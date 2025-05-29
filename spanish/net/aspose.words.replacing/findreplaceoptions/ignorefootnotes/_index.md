---
title: FindReplaceOptions.IgnoreFootnotes
linktitle: IgnoreFootnotes
articleTitle: IgnoreFootnotes
second_title: Aspose.Words para .NET
description: Descubre la propiedad FindReplaceOptions IgnoreFootnotes para gestionar fácilmente las notas al pie de tus documentos. ¡Mejora la eficiencia de la edición con este sencillo interruptor!
type: docs
weight: 90
url: /es/net/aspose.words.replacing/findreplaceoptions/ignorefootnotes/
---
## FindReplaceOptions.IgnoreFootnotes property

Obtiene o establece un valor booleano que indica si se deben ignorar las notas al pie. El valor predeterminado es`FALSO` .

```csharp
public bool IgnoreFootnotes { get; set; }
```

## Ejemplos

Muestra cómo ignorar notas al pie durante una operación de búsqueda y reemplazo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Footnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder.InsertParagraph();

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Endnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

// Establezca el indicador "IgnoreFootnotes" en "verdadero" para obtener la función de búsqueda y reemplazo
// operación para ignorar el texto dentro de las notas al pie.
// Establezca el indicador "IgnoreFootnotes" en "falso" para obtener la función de búsqueda y reemplazo
// operación para buscar también texto dentro de notas al pie.
FindReplaceOptions options = new FindReplaceOptions { IgnoreFootnotes = isIgnoreFootnotes };
doc.Range.Replace("Lorem ipsum", "Replaced Lorem ipsum", options);
```

### Ver también

* class [FindReplaceOptions](../)
* espacio de nombres [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* asamblea [Aspose.Words](../../../)
