---
title: DocumentProperty.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words para .NET
description: Descubra la función DocumentProperty Name que recupera sin esfuerzo los nombres de las propiedades, mejorando la gestión de sus documentos y la eficiencia del flujo de trabajo.
type: docs
weight: 30
url: /es/net/aspose.words.properties/documentproperty/name/
---
## DocumentProperty.Name property

Devuelve el nombre de la propiedad.

```csharp
public string Name { get; }
```

## Observaciones

No puede ser`nulo` y no puede ser una cadena vacía.

## Ejemplos

Muestra cómo trabajar con propiedades de documento integradas.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// El objeto "Documento" contiene algunos de sus metadatos en sus miembros.
Console.WriteLine($"Document filename:\n\t \"{doc.OriginalFileName}\"");

//El documento también almacena metadatos en sus propiedades integradas.
// Cada propiedad incorporada es un miembro del objeto "BuiltInDocumentProperties" del documento.
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

* class [DocumentProperty](../)
* espacio de nombres [Aspose.Words.Properties](../../../aspose.words.properties/)
* asamblea [Aspose.Words](../../../)
