---
title: PropertyType Enum
linktitle: PropertyType
articleTitle: PropertyType
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.PropertyType para definir fácilmente los tipos de datos de propiedades del documento para una mejor gestión y personalización del documento.
type: docs
weight: 5230
url: /es/net/aspose.words.properties/propertytype/
---
## PropertyType enumeration

Especifica el tipo de datos de una propiedad de documento.

```csharp
public enum PropertyType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Boolean | `0` | La propiedad es un valor booleano. |
| DateTime | `1` | La propiedad es un valor de fecha y hora. |
| Double | `2` | La propiedad es un número flotante. |
| Number | `3` | La propiedad es un número entero. |
| String | `4` | La propiedad es un valor de cadena. |
| StringArray | `5` | La propiedad es una matriz de cadenas. |
| ObjectArray | `6` | La propiedad es una matriz de objetos. |
| ByteArray | `7` | La propiedad es una matriz de bytes. |
| Other | `8` | La propiedad es de otro tipo. |

## Ejemplos

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

* class [DocumentProperty](../documentproperty/)
* property [Type](../documentproperty/type/)
* espacio de nombres [Aspose.Words.Properties](../../aspose.words.properties/)
* asamblea [Aspose.Words](../../)
