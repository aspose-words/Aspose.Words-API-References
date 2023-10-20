---
title: XmlMapping.SetMapping
linktitle: SetMapping
articleTitle: SetMapping
second_title: Aspose.Words para .NET
description: XmlMapping SetMapping método. Establece una asignación entre la etiqueta del documento estructurado principal y un nodo XML de una parte de datos XML personalizada en C#.
type: docs
weight: 70
url: /es/net/aspose.words.markup/xmlmapping/setmapping/
---
## XmlMapping.SetMapping method

Establece una asignación entre la etiqueta del documento estructurado principal y un nodo XML de una parte de datos XML personalizada.

```csharp
public bool SetMapping(CustomXmlPart customXmlPart, string xPath, string prefixMapping)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| customXmlPart | CustomXmlPart | Una parte de datos XML personalizada para asignar. |
| xPath | String | Una expresión XPath para encontrar el nodo XML. |
| prefixMapping | String | Asignaciones de prefijos de espacios de nombres XML para evaluar XPath. |

### Valor_devuelto

Un indicador que indica si la etiqueta del documento estructurado principal se asigna correctamente a el nodo XML.

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

* class [CustomXmlPart](../../customxmlpart/)
* class [XmlMapping](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
