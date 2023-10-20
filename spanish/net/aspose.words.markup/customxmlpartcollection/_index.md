---
title: CustomXmlPartCollection Class
linktitle: CustomXmlPartCollection
articleTitle: CustomXmlPartCollection
second_title: Aspose.Words para .NET
description: Aspose.Words.Markup.CustomXmlPartCollection clase. Representa una colección de elementos XML personalizados. Los artículos sonCustomXmlPart objetos en C#.
type: docs
weight: 3930
url: /es/net/aspose.words.markup/customxmlpartcollection/
---
## CustomXmlPartCollection class

Representa una colección de elementos XML personalizados. Los artículos son[`CustomXmlPart`](../customxmlpart/) objetos.

Para obtener más información, visite el[Etiquetas de documentos estructurados o control de contenido](https://docs.aspose.com/words/net/working-with-content-control-sdt/) artículo de documentación.

```csharp
public class CustomXmlPartCollection : IEnumerable<CustomXmlPart>
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [CustomXmlPartCollection](customxmlpartcollection/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.markup/customxmlpartcollection/count/) { get; } | Obtiene el número de elementos contenidos en la colección. |
| [Item](../../aspose.words.markup/customxmlpartcollection/item/) { get; set; } | Obtiene o establece un elemento en el índice especificado. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlpartcollection/add/#add_1)(*[CustomXmlPart](../customxmlpart/)*) | Agrega un elemento a la colección. |
| [Add](../../aspose.words.markup/customxmlpartcollection/add/#add)(*string, string*) | Crea una nueva parte XML con el XML especificado y lo agrega a la colección. |
| [Clear](../../aspose.words.markup/customxmlpartcollection/clear/)() | Elimina todos los elementos de la colección. |
| [Clone](../../aspose.words.markup/customxmlpartcollection/clone/)() | Hace una copia profunda de esta colección y sus elementos. |
| [GetById](../../aspose.words.markup/customxmlpartcollection/getbyid/)(*string*) | Busca y devuelve una parte XML personalizada por su identificador. |
| [GetEnumerator](../../aspose.words.markup/customxmlpartcollection/getenumerator/)() | Devuelve un objeto enumerador que se puede utilizar para iterar sobre todos los elementos de la colección. |
| [RemoveAt](../../aspose.words.markup/customxmlpartcollection/removeat/)(*int*) | Elimina un elemento en el índice especificado. |

## Observaciones

Normalmente no es necesario crear instancias de esta clase. Puede acceder a datos XML personalizados almacenados en un documento a través del[`CustomXmlParts`](../../aspose.words/document/customxmlparts/) propiedad.

## Ejemplos

Muestra cómo crear una etiqueta de documento estructurado con datos XML personalizados.

```csharp
Document doc = new Document();

// Construya una parte XML que contenga datos y agréguela a la colección del documento.
// Si habilitamos la pestaña "Desarrollador" en Microsoft Word,
// podemos encontrar elementos de esta colección en el "Panel de asignación XML", junto con algunos elementos predeterminados.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello world!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual(Encoding.ASCII.GetBytes(xmlPartContent), xmlPart.Data);
Assert.AreEqual(xmlPartId, xmlPart.Id);

// A continuación se muestran dos formas de hacer referencia a partes XML.
// 1 - Por un índice en la colección de piezas XML personalizada:
Assert.AreEqual(xmlPart, doc.CustomXmlParts[0]);

// 2 - Por GUID:
Assert.AreEqual(xmlPart, doc.CustomXmlParts.GetById(xmlPartId));

// Agregar una asociación de esquema XML.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Clona una parte y luego la inserta en la colección.
CustomXmlPart xmlPartClone = xmlPart.Clone();
xmlPartClone.Id = Guid.NewGuid().ToString("B");
doc.CustomXmlParts.Add(xmlPartClone);

Assert.AreEqual(2, doc.CustomXmlParts.Count);

// Iterar a través de la colección e imprimir el contenido de cada parte.
using (IEnumerator<CustomXmlPart> enumerator = doc.CustomXmlParts.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"XML part index {index}, ID: {enumerator.Current.Id}");
        Console.WriteLine($"\tContent: {Encoding.UTF8.GetString(enumerator.Current.Data)}");
        index++;
    }
}

// Utilice el método "RemoveAt" para eliminar la parte clonada por índice.
doc.CustomXmlParts.RemoveAt(1);

Assert.AreEqual(1, doc.CustomXmlParts.Count);

// Clona la colección de piezas XML y luego usa el método "Borrar" para eliminar todos sus elementos a la vez.
CustomXmlPartCollection customXmlParts = doc.CustomXmlParts.Clone();
customXmlParts.Clear();

// Crea una etiqueta de documento estructurada que mostrará el contenido de nuestra parte y la insertará en el cuerpo del documento.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[1]", string.Empty);

doc.FirstSection.Body.AppendChild(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CustomXml.docx");
```

### Ver también

* class [CustomXmlPart](../customxmlpart/)
* espacio de nombres [Aspose.Words.Markup](../../aspose.words.markup/)
* asamblea [Aspose.Words](../../)
