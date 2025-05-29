---
title: FindReplaceOptions.IgnoreFields
linktitle: IgnoreFields
articleTitle: IgnoreFields
second_title: Aspose.Words para .NET
description: Descubra la propiedad FindReplaceOptions IgnoreFields para gestionar fácilmente el texto dentro de los campos. ¡Controle cuándo ignorar el contenido para una búsqueda eficiente!
type: docs
weight: 80
url: /es/net/aspose.words.replacing/findreplaceoptions/ignorefields/
---
## FindReplaceOptions.IgnoreFields property

Obtiene o establece un valor booleano que indica si se debe ignorar el texto dentro de los campos. El valor predeterminado es`FALSO` .

```csharp
public bool IgnoreFields { get; set; }
```

## Observaciones

Esta opción afecta a todo el campo (todos los nodos entre FieldStart yFieldEnd).

Para ignorar solo los códigos de campo, utilice la opción correspondiente[`IgnoreFieldCodes`](../ignorefieldcodes/).

## Ejemplos

Muestra cómo ignorar el texto dentro de los campos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertField("QUOTE", "Hello again!");

// Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de búsqueda y reemplazo.
FindReplaceOptions options = new FindReplaceOptions();

// Establezca el indicador "IgnoreFields" en "verdadero" para obtener la función de búsqueda y reemplazo
// operación para ignorar el texto dentro de los campos.
// Establezca el indicador "IgnoreFields" en "falso" para obtener la función de búsqueda y reemplazo
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
* espacio de nombres [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* asamblea [Aspose.Words](../../../)
