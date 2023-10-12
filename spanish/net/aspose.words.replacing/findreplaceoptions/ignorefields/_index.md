---
title: FindReplaceOptions.IgnoreFields
second_title: Referencia de API de Aspose.Words para .NET
description: FindReplaceOptions propiedad. Obtiene o establece un valor booleano que indica que se debe ignorar el texto dentro de los campos. El valor predeterminado esFALSO .
type: docs
weight: 80
url: /es/net/aspose.words.replacing/findreplaceoptions/ignorefields/
---
## FindReplaceOptions.IgnoreFields property

Obtiene o establece un valor booleano que indica que se debe ignorar el texto dentro de los campos. El valor predeterminado es`FALSO` .

```csharp
public bool IgnoreFields { get; set; }
```

### Observaciones

Esta opción afecta a todo el campo (todos los nodos entre FieldStart yFieldEnd).

Para ignorar solo los códigos de campo, utilice la opción correspondiente[`IgnoreFieldCodes`](../ignorefieldcodes/).

### Ejemplos

Muestra cómo ignorar el texto dentro de los campos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertField("QUOTE", "Hello again!");

// Podemos utilizar un objeto "FindReplaceOptions" para modificar el proceso de buscar y reemplazar.
FindReplaceOptions options = new FindReplaceOptions();

// Establece el indicador "IgnoreFields" en "true" para obtener la función de buscar y reemplazar
// operación para ignorar el texto dentro de los campos.
// Establece el indicador "IgnoreFields" en "falso" para obtener la función de buscar y reemplazar
// operación para buscar también texto dentro de los campos.
options.IgnoreFields = ignoreTextInsideFields;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideFields
        ? "Greetings world!\r\u0013QUOTE\u0014Hello again!\u0015"
        : "Greetings world!\r\u0013QUOTE\u0014Greetings again!\u0015", doc.GetText().Trim());
```

### Ver también

* class [FindReplaceOptions](../)
* espacio de nombres [Aspose.Words.Replacing](../../findreplaceoptions/)
* asamblea [Aspose.Words](../../../)


