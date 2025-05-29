---
title: FindReplaceOptions.IgnoreInserted
linktitle: IgnoreInserted
articleTitle: IgnoreInserted
second_title: Aspose.Words para .NET
description: Descubra la propiedad FindReplaceOptions IgnoreInserted y controle el manejo de texto en las revisiones de inserción con esta sencilla configuración booleana. El valor predeterminado es falso.
type: docs
weight: 100
url: /es/net/aspose.words.replacing/findreplaceoptions/ignoreinserted/
---
## FindReplaceOptions.IgnoreInserted property

Obtiene o establece un valor booleano que indica si se debe ignorar el texto dentro de las revisiones de inserción. El valor predeterminado es`FALSO` .

```csharp
public bool IgnoreInserted { get; set; }
```

## Ejemplos

Muestra cómo incluir o ignorar texto dentro de las revisiones de inserción durante una operación de búsqueda y reemplazo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Iniciar el seguimiento de revisiones e insertar un párrafo. Ese párrafo será una revisión de inserción.
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("Hello again!");
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsInsertRevision);

// Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de búsqueda y reemplazo.
FindReplaceOptions options = new FindReplaceOptions();

// Establezca el indicador "IgnoreInserted" en "verdadero" para obtener la función de búsqueda y reemplazo
// operación para ignorar párrafos que son revisiones de inserción.
// Establezca el indicador "IgnoreInserted" en "falso" para obtener la función de búsqueda y reemplazo
// operación para buscar también texto dentro de las revisiones de inserción.
options.IgnoreInserted = ignoreTextInsideInsertRevisions;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideInsertRevisions
        ? "Greetings world!\rHello again!"
        : "Greetings world!\rGreetings again!", doc.GetText().Trim());
```

### Ver también

* class [FindReplaceOptions](../)
* espacio de nombres [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* asamblea [Aspose.Words](../../../)
