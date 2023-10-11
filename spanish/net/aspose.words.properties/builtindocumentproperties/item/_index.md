---
title: BuiltInDocumentProperties.Item
second_title: Referencia de API de Aspose.Words para .NET
description: BuiltInDocumentProperties propiedad. Devuelve unDocumentProperty objeto por el nombre de la propiedad.
type: docs
weight: 130
url: /es/net/aspose.words.properties/builtindocumentproperties/item/
---
## BuiltInDocumentProperties indexer

Devuelve un[`DocumentProperty`](../../documentproperty/) objeto por el nombre de la propiedad.

```csharp
public override DocumentProperty this[string name] { get; }
```

| Parámetro | Descripción |
| --- | --- |
| name | El nombre de la propiedad que se va a recuperar, sin distinguir entre mayúsculas y minúsculas. |

### Observaciones

Los nombres de cadena de las propiedades corresponden a los nombres de las propiedades typed disponibles en[`BuiltInDocumentProperties`](../).

Si solicita una propiedad que no está presente en el documento, pero el nombre de la propiedad se reconoce como un nombre integrado válido, se creará una nueva[`DocumentProperty`](../../documentproperty/) se crea, se agrega a la colección y se devuelve. A la propiedad recién creada se le asigna un valor predeterminado (cadena vacía, cero,`FALSO` o DateTime.MinValue dependiendo del type de la propiedad incorporada).

Si solicita una propiedad que no está presente en el documento y el nombre no se reconoce como un nombre incorporado, un`nulo` es regresado.

### Ejemplos

Muestra cómo trabajar con propiedades de documentos personalizados.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// Cada documento contiene una colección de propiedades personalizadas que, al igual que las propiedades integradas, son pares clave-valor.
 // El documento tiene una lista fija de propiedades integradas. El usuario crea todas las propiedades personalizadas.
Assert.AreEqual("Value of custom document property", doc.CustomDocumentProperties["CustomProperty"].ToString());

doc.CustomDocumentProperties.Add("CustomProperty2", "Value of custom document property #2");

Console.WriteLine("Custom Properties:");
foreach (var customDocumentProperty in doc.CustomDocumentProperties)
{
    Console.WriteLine(customDocumentProperty.Name);
    Console.WriteLine($"\tType:\t{customDocumentProperty.Type}");
    Console.WriteLine($"\tValue:\t\"{customDocumentProperty.Value}\"");
}
```

### Ver también

* class [DocumentProperty](../../documentproperty/)
* class [BuiltInDocumentProperties](../)
* espacio de nombres [Aspose.Words.Properties](../../builtindocumentproperties/)
* asamblea [Aspose.Words](../../../)


