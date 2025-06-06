---
title: Document.BuiltInDocumentProperties
linktitle: BuiltInDocumentProperties
articleTitle: BuiltInDocumentProperties
second_title: Aspose.Words para .NET
description: Explore la propiedad BuiltInDocumentProperties para acceder a propiedades esenciales del documento, mejorando así la gestión y la eficiencia de sus documentos.
type: docs
weight: 50
url: /es/net/aspose.words/document/builtindocumentproperties/
---
## Document.BuiltInDocumentProperties property

Devuelve una colección que representa todas las propiedades de documento integradas del documento.

```csharp
public BuiltInDocumentProperties BuiltInDocumentProperties { get; }
```

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

* class [BuiltInDocumentProperties](../../../aspose.words.properties/builtindocumentproperties/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
