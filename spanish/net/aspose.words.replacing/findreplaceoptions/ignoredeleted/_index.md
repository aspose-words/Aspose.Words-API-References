---
title: FindReplaceOptions.IgnoreDeleted
second_title: Referencia de API de Aspose.Words para .NET
description: FindReplaceOptions propiedad. Obtiene o establece un valor booleano que indica que se debe ignorar el texto dentro de las revisiones de eliminación. El valor predeterminado esFALSO .
type: docs
weight: 60
url: /es/net/aspose.words.replacing/findreplaceoptions/ignoredeleted/
---
## FindReplaceOptions.IgnoreDeleted property

Obtiene o establece un valor booleano que indica que se debe ignorar el texto dentro de las revisiones de eliminación. El valor predeterminado es`FALSO` .

```csharp
public bool IgnoreDeleted { get; set; }
```

### Ejemplos

Muestra cómo incluir o ignorar texto dentro de revisiones de eliminación durante una operación de buscar y reemplazar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Comience a rastrear las revisiones y elimine el segundo párrafo, lo que creará una revisión eliminada.
// Ese párrafo persistirá en el documento hasta que aceptemos la revisión eliminada.
doc.StartTrackRevisions("John Doe", DateTime.Now);
doc.FirstSection.Body.Paragraphs[1].Remove();
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsDeleteRevision);

// Podemos utilizar un objeto "FindReplaceOptions" para modificar el proceso de búsqueda y reemplazo.
FindReplaceOptions options = new FindReplaceOptions();

// Establece el indicador "IgnorarDeleted" en "true" para obtener la función de buscar y reemplazar
// operación para ignorar párrafos que son revisiones de eliminación.
// Establece el indicador "IgnorarDeleted" en "falso" para obtener la función de buscar y reemplazar
// operación para buscar también texto dentro de las revisiones de eliminación.
options.IgnoreDeleted = ignoreTextInsideDeleteRevisions;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideDeleteRevisions
        ? "Greetings world!\rHello again!"
        : "Greetings world!\rGreetings again!", doc.GetText().Trim());
```

### Ver también

* class [FindReplaceOptions](../)
* espacio de nombres [Aspose.Words.Replacing](../../findreplaceoptions/)
* asamblea [Aspose.Words](../../../)


