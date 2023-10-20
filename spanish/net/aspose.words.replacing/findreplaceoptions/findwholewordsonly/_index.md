---
title: FindReplaceOptions.FindWholeWordsOnly
linktitle: FindWholeWordsOnly
articleTitle: FindWholeWordsOnly
second_title: Aspose.Words para .NET
description: FindReplaceOptions FindWholeWordsOnly propiedad. Verdadero indica que oldValue debe ser una palabra independiente en C#.
type: docs
weight: 50
url: /es/net/aspose.words.replacing/findreplaceoptions/findwholewordsonly/
---
## FindReplaceOptions.FindWholeWordsOnly property

Verdadero indica que oldValue debe ser una palabra independiente.

```csharp
public bool FindWholeWordsOnly { get; set; }
```

## Ejemplos

Muestra cómo alternar operaciones independientes de búsqueda y reemplazo de solo palabras.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Podemos utilizar un objeto "FindReplaceOptions" para modificar el proceso de buscar y reemplazar.
FindReplaceOptions options = new FindReplaceOptions();

// Establece el indicador "FindWholeWordsOnly" en "true" para reemplazar el texto encontrado si no forma parte de otra palabra.
// Establece el indicador "FindWholeWordsOnly" en "false" para reemplazar todo el texto independientemente de su entorno.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

### Ver también

* class [FindReplaceOptions](../)
* espacio de nombres [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* asamblea [Aspose.Words](../../../)
