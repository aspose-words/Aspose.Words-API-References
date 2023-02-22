---
title: Class DocumentPropertyCollection
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Properties.DocumentPropertyCollection clase. Clase base paraBuiltInDocumentProperties yCustomDocumentProperties colecciones.
type: docs
weight: 4230
url: /es/net/aspose.words.properties/documentpropertycollection/
---
## DocumentPropertyCollection class

Clase base para[`BuiltInDocumentProperties`](../builtindocumentproperties/) y[`CustomDocumentProperties`](../customdocumentproperties/) colecciones.

```csharp
public abstract class DocumentPropertyCollection : IEnumerable<DocumentProperty>
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
| [Clear](../../aspose.words.properties/documentpropertycollection/clear/)() | Elimina todas las propiedades de la colección. |
| [Contains](../../aspose.words.properties/documentpropertycollection/contains/)(string) | Devuelve verdadero si existe una propiedad con el nombre especificado en la colección. |
| [GetEnumerator](../../aspose.words.properties/documentpropertycollection/getenumerator/)() | Devuelve un objeto enumerador que se puede usar para iterar sobre todos los elementos de la colección. |
| [IndexOf](../../aspose.words.properties/documentpropertycollection/indexof/)(string) | Obtiene el índice de una propiedad por nombre. |
| [Remove](../../aspose.words.properties/documentpropertycollection/remove/)(string) | Elimina una propiedad con el nombre especificado de la colección. |
| [RemoveAt](../../aspose.words.properties/documentpropertycollection/removeat/)(int) | Elimina una propiedad en el índice especificado. |

### Observaciones

Los nombres de las propiedades no distinguen entre mayúsculas y minúsculas.

Las propiedades de la colección están ordenadas alfabéticamente por nombre.

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

* class [BuiltInDocumentProperties](../builtindocumentproperties/)
* class [CustomDocumentProperties](../customdocumentproperties/)
* class [DocumentProperty](../documentproperty/)
* espacio de nombres [Aspose.Words.Properties](../../aspose.words.properties/)
* asamblea [Aspose.Words](../../)


