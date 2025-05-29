---
title: CustomXmlSchemaCollection.IndexOf
linktitle: IndexOf
articleTitle: IndexOf
second_title: Aspose.Words para .NET
description: Descubra el método IndexOf de CustomXmlSchemaCollection, que encuentra de manera eficiente el índice basado en cero de cualquier valor especificado en su colección XML.
type: docs
weight: 70
url: /es/net/aspose.words.markup/customxmlschemacollection/indexof/
---
## CustomXmlSchemaCollection.IndexOf method

Devuelve el índice basado en cero del valor especificado en la colección.

```csharp
public int IndexOf(string value)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| value | String | El valor que distingue entre mayúsculas y minúsculas que se va a localizar. |

### Valor_devuelto

Índice basado en cero. Valor negativo si no se encuentra.

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
