---
title: FindReplaceOptions.IgnoreDeleted
linktitle: IgnoreDeleted
articleTitle: IgnoreDeleted
second_title: Aspose.Words para .NET
description: Descubre la propiedad FindReplaceOptions IgnoreDeleted y controla la visibilidad del texto en las revisiones eliminadas con un sencillo interruptor booleano. ¡Mejora tu experiencia de edición!
type: docs
weight: 60
url: /es/net/aspose.words.replacing/findreplaceoptions/ignoredeleted/
---
## FindReplaceOptions.IgnoreDeleted property

Obtiene o establece un valor booleano que indica si se debe ignorar el texto dentro de las revisiones eliminadas. El valor predeterminado es`FALSO` .

```csharp
public bool IgnoreDeleted { get; set; }
```

## Ejemplos

Muestra cómo incluir o ignorar texto dentro de las revisiones de eliminación durante una operación de búsqueda y reemplazo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Comience a rastrear las revisiones y elimine el segundo párrafo, lo que creará una revisión de eliminación.
//Ese párrafo persistirá en el documento hasta que aceptemos la revisión de eliminación.
doc.StartTrackRevisions("John Doe", DateTime.Now);
doc.FirstSection.Body.Paragraphs[1].Remove();
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsDeleteRevision);

// Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de búsqueda y reemplazo.
FindReplaceOptions options = new FindReplaceOptions();

// Establezca el indicador "IgnoreDeleted" en "verdadero" para obtener la función de búsqueda y reemplazo
// operación para ignorar párrafos que son revisiones de eliminación.
// Establezca el indicador "IgnoreDeleted" en "falso" para obtener la función de búsqueda y reemplazo
// operación para buscar también texto dentro de las revisiones eliminadas.
options.IgnoreDeleted = ignoreTextInsideDeleteRevisions;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideDeleteRevisions
        ? "Greetings world!\rHello again!"
        : "Greetings world!\rGreetings again!", doc.GetText().Trim());
```

### Ver también

* class [FindReplaceOptions](../)
* espacio de nombres [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* asamblea [Aspose.Words](../../../)
