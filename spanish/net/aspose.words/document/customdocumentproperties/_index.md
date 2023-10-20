---
title: Document.CustomDocumentProperties
linktitle: CustomDocumentProperties
articleTitle: CustomDocumentProperties
second_title: Aspose.Words para .NET
description: Document CustomDocumentProperties propiedad. Devuelve una colección que representa todas las propiedades personalizadas del documento en C#.
type: docs
weight: 70
url: /es/net/aspose.words/document/customdocumentproperties/
---
## Document.CustomDocumentProperties property

Devuelve una colección que representa todas las propiedades personalizadas del documento.

```csharp
public CustomDocumentProperties CustomDocumentProperties { get; }
```

## Ejemplos

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

* class [CustomDocumentProperties](../../../aspose.words.properties/customdocumentproperties/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
