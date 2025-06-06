---
title: CustomXmlSchemaCollection Class
linktitle: CustomXmlSchemaCollection
articleTitle: CustomXmlSchemaCollection
second_title: Aspose.Words para .NET
description: Explore la clase Aspose.Words.Markup.CustomXmlSchemaCollection para administrar esquemas XML vinculados a partes XML personalizadas, mejorando la flexibilidad y el control del documento.
type: docs
weight: 4650
url: /es/net/aspose.words.markup/customxmlschemacollection/
---
## CustomXmlSchemaCollection class

Una colección de cadenas que representan esquemas XML asociados con una parte XML personalizada.

Para obtener más información, visite el[Etiquetas de documentos estructurados o control de contenido](https://docs.aspose.com/words/net/working-with-content-control-sdt/) Artículo de documentación.

```csharp
public class CustomXmlSchemaCollection : IEnumerable<string>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.markup/customxmlschemacollection/count/) { get; } | Obtiene el número de elementos contenidos en la colección. |
| [Item](../../aspose.words.markup/customxmlschemacollection/item/) { get; set; } | Obtiene o establece el elemento en el índice especificado. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlschemacollection/add/)(*string*) | Agrega un elemento a la colección. |
| [Clear](../../aspose.words.markup/customxmlschemacollection/clear/)() | Elimina todos los elementos de la colección. |
| [Clone](../../aspose.words.markup/customxmlschemacollection/clone/)() | Realiza un clon profundo de este objeto. |
| [GetEnumerator](../../aspose.words.markup/customxmlschemacollection/getenumerator/)() | Devuelve un objeto enumerador que se puede utilizar para iterar sobre todos los elementos de la colección. |
| [IndexOf](../../aspose.words.markup/customxmlschemacollection/indexof/)(*string*) | Devuelve el índice basado en cero del valor especificado en la colección. |
| [Remove](../../aspose.words.markup/customxmlschemacollection/remove/)(*string*) | Elimina el valor especificado de la colección. |
| [RemoveAt](../../aspose.words.markup/customxmlschemacollection/removeat/)(*int*) | Elimina un valor en el índice especificado. |

## Observaciones

No se crean instancias de esta clase. Se accede a la colección de esquemas XML de un XML personalizado part mediante[`Schemas`](../customxmlpart/schemas/) propiedad.

## Ejemplos

Muestra cómo trabajar con una colección de esquemas XML.

```csharp
Document doc = new Document();

string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello, World!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

//Agrega una asociación de esquema XML.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Clonar la colección de asociaciones de esquemas XML de la parte XML personalizada,
// y luego agregue un par de esquemas nuevos al clon.
CustomXmlSchemaCollection schemas = xmlPart.Schemas.Clone();
schemas.Add("http://www.w3.org/2001/XMLSchema-instance");
schemas.Add("http://schemas.microsoft.com/office/2006/metadata/contentType");

Assert.AreEqual(3, schemas.Count);
Assert.AreEqual(2, schemas.IndexOf("http://schemas.microsoft.com/office/2006/metadata/contentType"));

// Enumera los esquemas e imprime cada elemento.
using (IEnumerator<string> enumerator = schemas.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine(enumerator.Current);
}

A continuación se muestran tres formas de eliminar esquemas de la colección.
// 1 - Eliminar un esquema por índice:
schemas.RemoveAt(2);

// 2 - Eliminar un esquema por valor:
schemas.Remove("http://www.w3.org/2001/XMLSchema");

// 3 - Utilice el método "Clear" para vaciar la colección de una vez.
schemas.Clear();

Assert.AreEqual(0, schemas.Count);
```

### Ver también

* espacio de nombres [Aspose.Words.Markup](../../aspose.words.markup/)
* asamblea [Aspose.Words](../../)
