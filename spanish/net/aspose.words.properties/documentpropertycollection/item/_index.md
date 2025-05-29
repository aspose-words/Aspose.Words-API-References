---
title: DocumentPropertyCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words para .NET
description: Acceda fácilmente a los objetos DocumentProperty con nuestro elemento DocumentPropertyCollection. Recupere propiedades por nombre para una gestión documental fluida.
type: docs
weight: 20
url: /es/net/aspose.words.properties/documentpropertycollection/item/
---
## DocumentPropertyCollection indexer (1 of 2)

Devuelve un[`DocumentProperty`](../../documentproperty/) objeto por el nombre de la propiedad.

```csharp
public virtual DocumentProperty this[string name] { get; }
```

| Parámetro | Descripción |
| --- | --- |
| name | El nombre sin distinción entre mayúsculas y minúsculas de la propiedad que se recuperará. |

## Observaciones

Devoluciones`nulo` si no se encuentra una propiedad con el nombre especificado.

## Ejemplos

Muestra cómo crear una propiedad de documento personalizada que contiene una fecha y una hora.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);
DateTime authorizationDate = doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime();
Console.WriteLine($"Document authorized on {authorizationDate}");
```

### Ver también

* class [DocumentProperty](../../documentproperty/)
* class [DocumentPropertyCollection](../)
* espacio de nombres [Aspose.Words.Properties](../../../aspose.words.properties/)
* asamblea [Aspose.Words](../../../)

---

## DocumentPropertyCollection indexer (2 of 2)

Devuelve un[`DocumentProperty`](../../documentproperty/) objeto por índice.

```csharp
public DocumentProperty this[int index] { get; }
```

| Parámetro | Descripción |
| --- | --- |
| index | Índice basado en cero de la[`DocumentProperty`](../../documentproperty/) Para recuperar. |

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

* class [DocumentProperty](../../documentproperty/)
* class [DocumentPropertyCollection](../)
* espacio de nombres [Aspose.Words.Properties](../../../aspose.words.properties/)
* asamblea [Aspose.Words](../../../)
