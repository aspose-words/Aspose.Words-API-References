---
title: FindReplaceOptions.IgnoreFootnotes
second_title: Referencia de API de Aspose.Words para .NET
description: FindReplaceOptions propiedad. Obtiene o establece un valor booleano que indica que se deben ignorar las notas al pie. El valor predeterminado esFALSO .
type: docs
weight: 90
url: /es/net/aspose.words.replacing/findreplaceoptions/ignorefootnotes/
---
## FindReplaceOptions.IgnoreFootnotes property

Obtiene o establece un valor booleano que indica que se deben ignorar las notas al pie. El valor predeterminado es`FALSO` .

```csharp
public bool IgnoreFootnotes { get; set; }
```

### Ejemplos

Muestra cómo ignorar las notas al pie durante una operación de buscar y reemplazar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Footnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder.InsertParagraph();

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Endnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

// Establece el indicador "IgnoreFootnotes" en "true" para obtener la función de buscar y reemplazar
// operación para ignorar el texto dentro de las notas al pie.
// Establece el indicador "Ignorar notas a pie" en "falso" para obtener la opción de buscar y reemplazar
// operación para buscar también texto dentro de las notas al pie.
FindReplaceOptions options = new FindReplaceOptions { IgnoreFootnotes = isIgnoreFootnotes };
doc.Range.Replace("Lorem ipsum", "Replaced Lorem ipsum", options);
```

### Ver también

* class [FindReplaceOptions](../)
* espacio de nombres [Aspose.Words.Replacing](../../findreplaceoptions/)
* asamblea [Aspose.Words](../../../)


