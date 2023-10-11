---
title: Class CustomDocumentProperties
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Properties.CustomDocumentProperties clase. Una colección de propiedades de documentos personalizadas.
type: docs
weight: 4460
url: /es/net/aspose.words.properties/customdocumentproperties/
---
## CustomDocumentProperties class

Una colección de propiedades de documentos personalizadas.

Para obtener más información, visite el[Trabajar con propiedades de documento](https://docs.aspose.com/words/net/work-with-document-properties/) artículo de documentación.

```csharp
public class CustomDocumentProperties : DocumentPropertyCollection
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.properties/documentpropertycollection/count/) { get; } | Obtiene el número de elementos de la colección. |
| [Item](../../aspose.words.properties/documentpropertycollection/item/) { get; } | Devuelve un[`DocumentProperty`](../documentproperty/) objeto por index. |
| virtual [Item](../../aspose.words.properties/documentpropertycollection/item/) { get; } | Devuelve un[`DocumentProperty`](../documentproperty/) objeto por el nombre de la propiedad. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add)(string, bool) | Crea una nueva propiedad de documento personalizada delBoolean tipo de datos. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_3)(string, DateTime) | Crea una nueva propiedad de documento personalizada delDateTime tipo de datos. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_1)(string, double) | Crea una nueva propiedad de documento personalizada delDouble tipo de datos. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_2)(string, int) | Crea una nueva propiedad de documento personalizada delNumber tipo de datos. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_4)(string, string) | Crea una nueva propiedad de documento personalizada delString tipo de datos. |
| [AddLinkToContent](../../aspose.words.properties/customdocumentproperties/addlinktocontent/)(string, string) | Crea una nueva propiedad de documento personalizada vinculada al contenido. |
| [Clear](../../aspose.words.properties/documentpropertycollection/clear/)() | Elimina todas las propiedades de la colección. |
| [Contains](../../aspose.words.properties/documentpropertycollection/contains/)(string) | Devoluciones`verdadero` si existe una propiedad con el nombre especificado en la colección. |
| [GetEnumerator](../../aspose.words.properties/documentpropertycollection/getenumerator/)() | Devuelve un objeto enumerador que se puede utilizar para iterar sobre todos los elementos de la colección. |
| [IndexOf](../../aspose.words.properties/documentpropertycollection/indexof/)(string) | Obtiene el índice de una propiedad por nombre. |
| [Remove](../../aspose.words.properties/documentpropertycollection/remove/)(string) | Elimina una propiedad con el nombre especificado de la colección. |
| [RemoveAt](../../aspose.words.properties/documentpropertycollection/removeat/)(int) | Elimina una propiedad en el índice especificado. |

### Observaciones

Cada[`DocumentProperty`](../documentproperty/) El objeto representa una propiedad personalizada de un documento contenedor.

Los nombres de las propiedades no distinguen entre mayúsculas y minúsculas.

Las propiedades de la colección están ordenadas alfabéticamente por nombre.

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

* class [Document](../../aspose.words/document/)
* property [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties/)
* property [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties/)
* class [DocumentPropertyCollection](../documentpropertycollection/)
* espacio de nombres [Aspose.Words.Properties](../../aspose.words.properties/)
* asamblea [Aspose.Words](../../)


