---
title: FindReplaceOptions.IgnoreFieldCodes
second_title: Referencia de API de Aspose.Words para .NET
description: FindReplaceOptions propiedad. Obtiene o establece un valor booleano que indica ignorar el texto dentro de los códigos de campo. El valor predeterminado esfalso .
type: docs
weight: 70
url: /es/net/aspose.words.replacing/findreplaceoptions/ignorefieldcodes/
---
## FindReplaceOptions.IgnoreFieldCodes property

Obtiene o establece un valor booleano que indica ignorar el texto dentro de los códigos de campo. El valor predeterminado es`falso` .

```csharp
public bool IgnoreFieldCodes { get; set; }
```

### Observaciones

Esta opción afecta solo a los códigos de campo (no ignora los nodos between FieldSeparator yFieldEnd).

Para ignorar todo el campo, utilice la opción correspondiente[`IgnoreFields`](../ignorefields/).

### Ejemplos

Muestra cómo ignorar el texto dentro de los códigos de campo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField("INCLUDETEXT", "Test IT!");

FindReplaceOptions options = new FindReplaceOptions {IgnoreFieldCodes = ignoreFieldCodes};

// Reemplace 'T' en el documento ignorando el texto dentro del código de campo o no.
doc.Range.Replace(new Regex("T"), "*", options);
Console.WriteLine(doc.GetText());

Assert.AreEqual(
    ignoreFieldCodes
        ? "\u0013INCLUDETEXT\u0014*est I*!\u0015"
        : "\u0013INCLUDE*EX*\u0014*est I*!\u0015", doc.GetText().Trim());
```

### Ver también

* class [FindReplaceOptions](../)
* espacio de nombres [Aspose.Words.Replacing](../../findreplaceoptions/)
* asamblea [Aspose.Words](../../../)


