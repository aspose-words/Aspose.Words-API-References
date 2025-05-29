---
title: CustomXmlSchemaCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words para .NET
description: Administre sin esfuerzo su CustomXmlSchemaCollection con el método RemoveAt: elimine rápidamente valores por índice para un manejo optimizado de los datos.
type: docs
weight: 90
url: /es/net/aspose.words.markup/customxmlschemacollection/removeat/
---
## CustomXmlSchemaCollection.RemoveAt method

Elimina un valor en el índice especificado.

```csharp
public void RemoveAt(int index)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| index | Int32 | El índice basado en cero. |

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

* class [CustomXmlSchemaCollection](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
