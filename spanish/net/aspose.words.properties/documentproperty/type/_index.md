---
title: DocumentProperty.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words para .NET
description: Descubra el tipo DocumentProperty para recuperar y utilizar de manera eficiente tipos de datos de propiedad para una mejor gestión y automatización de documentos.
type: docs
weight: 40
url: /es/net/aspose.words.properties/documentproperty/type/
---
## DocumentProperty.Type property

Obtiene el tipo de datos de la propiedad.

```csharp
public PropertyType Type { get; }
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

Muestra cómo trabajar con las propiedades personalizadas de un documento.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Las propiedades de documento personalizadas son pares clave-valor que podemos agregar al documento.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

//La colección ordena las propiedades personalizadas en orden alfabético.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// Imprime cada propiedad personalizada en el documento.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Muestra el valor de una propiedad personalizada utilizando un campo DOCPROPERTY.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Podemos encontrar estas propiedades personalizadas en Microsoft Word a través de "Archivo" -> "Propiedades" -> "Propiedades avanzadas" -> "Personalizado".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

A continuación se muestran tres formas de eliminar propiedades personalizadas de un documento.
// 1 - Eliminar por índice:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - Eliminar por nombre:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Vaciar toda la colección de una vez:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Ver también

* enum [PropertyType](../../propertytype/)
* class [DocumentProperty](../)
* espacio de nombres [Aspose.Words.Properties](../../../aspose.words.properties/)
* asamblea [Aspose.Words](../../../)
