---
title: DocumentPropertyCollection.Remove
second_title: Referencia de API de Aspose.Words para .NET
description: DocumentPropertyCollection método. Elimina una propiedad con el nombre especificado de la colección.
type: docs
weight: 70
url: /es/net/aspose.words.properties/documentpropertycollection/remove/
---
## DocumentPropertyCollection.Remove method

Elimina una propiedad con el nombre especificado de la colección.

```csharp
public void Remove(string name)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| name | String | El nombre de la propiedad que no distingue entre mayúsculas y minúsculas. |

### Ejemplos

Muestra cómo trabajar con las propiedades personalizadas de un documento.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Las propiedades personalizadas del documento son pares clave-valor que podemos agregar al documento.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// La colección ordena las propiedades personalizadas en orden alfabético.
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

// Podemos encontrar estas propiedades personalizadas en Microsoft Word a través de "Archivo" -> "Propiedades" > "Propiedades avanzadas" > "Disfraz".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// A continuación se muestran tres formas de eliminar propiedades personalizadas de un documento.
// 1 - Eliminar por índice:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - Eliminar por nombre:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Vaciar toda la colección a la vez:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Ver también

* class [DocumentPropertyCollection](../)
* espacio de nombres [Aspose.Words.Properties](../../documentpropertycollection/)
* asamblea [Aspose.Words](../../../)


