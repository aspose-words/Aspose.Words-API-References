---
title: DocumentPropertyCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words para .NET
description: Descubra la propiedad DocumentPropertyCollection Count para recuperar sin esfuerzo la cantidad de elementos de su colección para una gestión de datos eficiente.
type: docs
weight: 10
url: /es/net/aspose.words.properties/documentpropertycollection/count/
---
## DocumentPropertyCollection.Count property

Obtiene el número de elementos en la colección.

```csharp
public int Count { get; }
```

## Ejemplos

Muestra cómo trabajar con propiedades de documentos personalizadas.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// Cada documento contiene una colección de propiedades personalizadas que, al igual que las propiedades integradas, son pares clave-valor.
 El documento tiene una lista fija de propiedades integradas. El usuario crea todas las propiedades personalizadas.
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

* class [DocumentPropertyCollection](../)
* espacio de nombres [Aspose.Words.Properties](../../../aspose.words.properties/)
* asamblea [Aspose.Words](../../../)
