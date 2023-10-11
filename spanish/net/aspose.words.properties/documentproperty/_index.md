---
title: Class DocumentProperty
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Properties.DocumentProperty clase. Representa una propiedad de documento personalizada o integrada.
type: docs
weight: 4470
url: /es/net/aspose.words.properties/documentproperty/
---
## DocumentProperty class

Representa una propiedad de documento personalizada o integrada.

Para obtener más información, visite el[Trabajar con propiedades de documento](https://docs.aspose.com/words/net/work-with-document-properties/) artículo de documentación.

```csharp
public class DocumentProperty
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [IsLinkToContent](../../aspose.words.properties/documentproperty/islinktocontent/) { get; } | Muestra si esta propiedad está vinculada al contenido o no. |
| [LinkSource](../../aspose.words.properties/documentproperty/linksource/) { get; } | Obtiene el origen de una propiedad de documento personalizada vinculada. |
| [Name](../../aspose.words.properties/documentproperty/name/) { get; } | Devuelve el nombre de la propiedad. |
| [Type](../../aspose.words.properties/documentproperty/type/) { get; } | Obtiene el tipo de datos de la propiedad. |
| [Value](../../aspose.words.properties/documentproperty/value/) { get; set; } | Obtiene o establece el valor de la propiedad. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [ToBool](../../aspose.words.properties/documentproperty/tobool/)() | Devuelve el valor de la propiedad como bool. |
| [ToByteArray](../../aspose.words.properties/documentproperty/tobytearray/)() | Devuelve el valor de la propiedad como matriz de bytes. |
| [ToDateTime](../../aspose.words.properties/documentproperty/todatetime/)() | Devuelve el valor de la propiedad como **Fecha y hora** en UTC. |
| [ToDouble](../../aspose.words.properties/documentproperty/todouble/)() | Devuelve el valor de la propiedad como doble. |
| [ToInt](../../aspose.words.properties/documentproperty/toint/)() | Devuelve el valor de la propiedad como un número entero. |
| override [ToString](../../aspose.words.properties/documentproperty/tostring/)() | Devuelve el valor de la propiedad como una cadena formateada según la configuración regional actual. |

### Ejemplos

Muestra cómo trabajar con propiedades de documentos integradas.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// El objeto "Documento" contiene algunos de sus metadatos en sus miembros.
Console.WriteLine($"Document filename:\n\t \"{doc.OriginalFileName}\"");

// El documento también almacena metadatos en sus propiedades integradas.
// Cada propiedad integrada es miembro del objeto "BuiltInDocumentProperties" del documento.
Console.WriteLine("Built-in Properties:");
foreach (DocumentProperty docProperty in doc.BuiltInDocumentProperties)
{
    Console.WriteLine(docProperty.Name);
    Console.WriteLine($"\tType:\t{docProperty.Type}");

    // Algunas propiedades pueden almacenar múltiples valores.
    if (docProperty.Value is ICollection<object>)
    {
        foreach (object value in docProperty.Value as ICollection<object>)
            Console.WriteLine($"\tValue:\t\"{value}\"");
    }
    else
    {
        Console.WriteLine($"\tValue:\t\"{docProperty.Value}\"");
    }
}
```

### Ver también

* class [DocumentPropertyCollection](../documentpropertycollection/)
* espacio de nombres [Aspose.Words.Properties](../../aspose.words.properties/)
* asamblea [Aspose.Words](../../)


