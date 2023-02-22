---
title: FindReplaceOptions.IgnoreFields
second_title: Referencia de API de Aspose.Words para .NET
description: FindReplaceOptions propiedad. Obtiene o establece un valor booleano que indica ignorar el texto dentro de los campos. El valor predeterminado esfalso .
type: docs
weight: 80
url: /es/net/aspose.words.replacing/findreplaceoptions/ignorefields/
---
## FindReplaceOptions.IgnoreFields property

Obtiene o establece un valor booleano que indica ignorar el texto dentro de los campos. El valor predeterminado es`falso` .

```csharp
public bool IgnoreFields { get; set; }
```

### Observaciones

Esta opción afecta todo el campo (todos los nodos entre FieldStart yFieldEnd).

Para ignorar solo los códigos de campo, utilice la opción correspondiente[`IgnoreFieldCodes`](../ignorefieldcodes/).

### Ejemplos

Muestra cómo ignorar el texto dentro de los campos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertField("QUOTE", "Hello again!");

// Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de buscar y reemplazar.
FindReplaceOptions options = new FindReplaceOptions();

// Establezca el indicador "IgnoreFields" en "true" para obtener la búsqueda y el reemplazo
// operación para ignorar el texto dentro de los campos.
// Establezca el indicador "IgnoreFields" en "falso" para obtener la función de buscar y reemplazar
// operación para buscar también texto dentro de campos.
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


