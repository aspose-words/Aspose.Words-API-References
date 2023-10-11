---
title: DocumentProperty.Value
second_title: Referencia de API de Aspose.Words para .NET
description: DocumentProperty propiedad. Obtiene o establece el valor de la propiedad.
type: docs
weight: 50
url: /es/net/aspose.words.properties/documentproperty/value/
---
## DocumentProperty.Value property

Obtiene o establece el valor de la propiedad.

```csharp
public object Value { get; set; }
```

### Observaciones

No puede ser`nulo`.

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

* class [DocumentProperty](../)
* espacio de nombres [Aspose.Words.Properties](../../documentproperty/)
* asamblea [Aspose.Words](../../../)


