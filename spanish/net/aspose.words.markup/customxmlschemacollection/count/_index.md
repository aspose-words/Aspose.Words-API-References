---
title: CustomXmlSchemaCollection.Count
second_title: Referencia de API de Aspose.Words para .NET
description: CustomXmlSchemaCollection propiedad. Obtiene el número de elementos que contiene la colección.
type: docs
weight: 10
url: /es/net/aspose.words.markup/customxmlschemacollection/count/
---
## CustomXmlSchemaCollection.Count property

Obtiene el número de elementos que contiene la colección.

```csharp
public int Count { get; }
```

### Ejemplos

Muestra cómo trabajar con una colección de esquemas XML.

```csharp
Document doc = new Document();

string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello, World!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

// Agregar una asociación de esquema XML.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Clonar la colección de asociaciones de esquemas XML de la parte XML personalizada,
// y luego agregue un par de esquemas nuevos al clon.
CustomXmlSchemaCollection schemas = xmlPart.Schemas.Clone();
schemas.Add("http://www.w3.org/2001/XMLSchema-instance");
schemas.Add("http://schemas.microsoft.com/office/2006/metadata/contentType");

Assert.AreEqual(3, schemas.Count);
Assert.AreEqual(2, schemas.IndexOf("http://schemas.microsoft.com/office/2006/metadata/contentType"));

// Enumerar los esquemas e imprimir cada elemento.
using (IEnumerator<string> enumerator = schemas.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine(enumerator.Current);
}

// A continuación se muestran tres formas de eliminar esquemas de la colección.
// 1 - Eliminar un esquema por índice:
schemas.RemoveAt(2);

// 2 - Eliminar un esquema por valor:
schemas.Remove("http://www.w3.org/2001/XMLSchema");

// 3 - Usa el método "Borrar" para vaciar la colección de una vez.
schemas.Clear();

Assert.AreEqual(0, schemas.Count);
```

### Ver también

* class [CustomXmlSchemaCollection](../)
* espacio de nombres [Aspose.Words.Markup](../../customxmlschemacollection/)
* asamblea [Aspose.Words](../../../)


