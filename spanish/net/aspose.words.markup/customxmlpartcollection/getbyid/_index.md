---
title: CustomXmlPartCollection.GetById
linktitle: GetById
articleTitle: GetById
second_title: Aspose.Words para .NET
description: Descubra el método GetById de CustomXmlPartCollection para recuperar sin esfuerzo partes XML personalizadas por sus identificadores únicos para una mejor gestión de datos.
type: docs
weight: 70
url: /es/net/aspose.words.markup/customxmlpartcollection/getbyid/
---
## CustomXmlPartCollection.GetById method

Busca y devuelve una parte XML personalizada por su identificador.

```csharp
public CustomXmlPart GetById(string id)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| id | String | Cadena que distingue entre mayúsculas y minúsculas que identifica la parte XML personalizada. |

### Valor_devuelto

Devoluciones`nulo` si no se encuentra una parte XML personalizada con el identificador especificado.

## Ejemplos

Muestra cómo crear una etiqueta de documento estructurado con datos XML personalizados.

```csharp
Document doc = new Document();

// Construya una parte XML que contenga datos y agréguela a la colección del documento.
// Si habilitamos la pestaña "Desarrollador" en Microsoft Word,
//Podemos encontrar elementos de esta colección en el "Panel de mapeo XML", junto con algunos elementos predeterminados.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello world!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual(Encoding.ASCII.GetBytes(xmlPartContent), xmlPart.Data);
Assert.AreEqual(xmlPartId, xmlPart.Id);

A continuación se muestran dos formas de hacer referencia a partes XML.
// 1 - Por un índice en la colección de partes XML personalizadas:
Assert.AreEqual(xmlPart, doc.CustomXmlParts[0]);

// 2 - Por GUID:
Assert.AreEqual(xmlPart, doc.CustomXmlParts.GetById(xmlPartId));

//Agrega una asociación de esquema XML.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Clona una parte y luego insértala en la colección.
CustomXmlPart xmlPartClone = xmlPart.Clone();
xmlPartClone.Id = Guid.NewGuid().ToString("B");
doc.CustomXmlParts.Add(xmlPartClone);

Assert.AreEqual(2, doc.CustomXmlParts.Count);

// Itera a través de la colección e imprime el contenido de cada parte.
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

// Clone la colección de partes XML y luego use el método "Clear" para eliminar todos sus elementos a la vez.
CustomXmlPartCollection customXmlParts = doc.CustomXmlParts.Clone();
customXmlParts.Clear();

// Cree una etiqueta de documento estructurada que mostrará el contenido de nuestra parte y la insertará en el cuerpo del documento.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[1]", string.Empty);

doc.FirstSection.Body.AppendChild(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CustomXml.docx");
```

### Ver también

* class [CustomXmlPart](../../customxmlpart/)
* class [CustomXmlPartCollection](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
