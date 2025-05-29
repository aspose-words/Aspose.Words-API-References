---
title: FindReplaceOptions.FindWholeWordsOnly
linktitle: FindWholeWordsOnly
articleTitle: FindWholeWordsOnly
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad FindWholeWordsOnly mejora su búsqueda con resultados precisos, garantizando que oldValue coincida solo como una palabra independiente.
type: docs
weight: 50
url: /es/net/aspose.words.replacing/findreplaceoptions/findwholewordsonly/
---
## FindReplaceOptions.FindWholeWordsOnly property

True indica que el valor anterior debe ser una palabra independiente.

```csharp
public bool FindWholeWordsOnly { get; set; }
```

## Ejemplos

Muestra cómo alternar operaciones de búsqueda y reemplazo independientes de solo palabras.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de búsqueda y reemplazo.
FindReplaceOptions options = new FindReplaceOptions();

// Establezca el indicador "FindWholeWordsOnly" en "verdadero" para reemplazar el texto encontrado si no es parte de otra palabra.
// Establezca el indicador "FindWholeWordsOnly" en "falso" para reemplazar todo el texto independientemente de su entorno.
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
