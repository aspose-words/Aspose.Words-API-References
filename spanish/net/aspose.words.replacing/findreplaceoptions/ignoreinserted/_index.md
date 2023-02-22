---
title: FindReplaceOptions.IgnoreInserted
second_title: Referencia de API de Aspose.Words para .NET
description: FindReplaceOptions propiedad. Obtiene o establece un valor booleano que indica ignorar el texto dentro de las revisiones de inserción. El valor predeterminado esfalso .
type: docs
weight: 100
url: /es/net/aspose.words.replacing/findreplaceoptions/ignoreinserted/
---
## FindReplaceOptions.IgnoreInserted property

Obtiene o establece un valor booleano que indica ignorar el texto dentro de las revisiones de inserción. El valor predeterminado es`falso` .

```csharp
public bool IgnoreInserted { get; set; }
```

### Ejemplos

Muestra cómo incluir o ignorar texto dentro de las revisiones de inserción durante una operación de buscar y reemplazar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Comience a rastrear las revisiones e inserte un párrafo. Ese párrafo será una revisión de inserción.
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("Hello again!");
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsInsertRevision);

// Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de buscar y reemplazar.
FindReplaceOptions options = new FindReplaceOptions();

// Establezca el indicador "Ignorar insertado" en "verdadero" para obtener la función de buscar y reemplazar
// operación para ignorar párrafos que son revisiones de inserción.
// Establezca el indicador "Ignorar insertado" en "falso" para obtener la búsqueda y el reemplazo
// operación para buscar también texto dentro de insertar revisiones.
options.IgnoreInserted = ignoreTextInsideInsertRevisions;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideInsertRevisions
        ? "Greetings world!\rHello again!"
        : "Greetings world!\rGreetings again!", doc.GetText().Trim());
```

### Ver también

* class [FindReplaceOptions](../)
* espacio de nombres [Aspose.Words.Replacing](../../findreplaceoptions/)
* asamblea [Aspose.Words](../../../)


