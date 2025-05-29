---
title: CustomXmlPart Class
linktitle: CustomXmlPart
articleTitle: CustomXmlPart
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Markup.CustomXmlPart para una gestión eficiente del almacenamiento de datos XML personalizados dentro de paquetes. ¡Mejore su procesamiento de documentos hoy mismo!
type: docs
weight: 4610
url: /es/net/aspose.words.markup/customxmlpart/
---
## CustomXmlPart class

Representa una parte de almacenamiento de datos XML personalizados (datos XML personalizados dentro de un paquete).

Para obtener más información, visite el[Etiquetas de documentos estructurados o control de contenido](https://docs.aspose.com/words/net/working-with-content-control-sdt/) Artículo de documentación.

```csharp
public class CustomXmlPart
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [CustomXmlPart](customxmlpart/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Data](../../aspose.words.markup/customxmlpart/data/) { get; set; } | Obtiene o establece el contenido XML de esta parte de almacenamiento de datos XML personalizada. |
| [DataChecksum](../../aspose.words.markup/customxmlpart/datachecksum/) { get; } | Especifica una suma de comprobación de redundancia cíclica (CRC) de la[`Data`](./data/) contenido. |
| [Id](../../aspose.words.markup/customxmlpart/id/) { get; set; } | Obtiene o establece la cadena que identifica esta parte XML personalizada dentro de un documento OOXML. |
| [Schemas](../../aspose.words.markup/customxmlpart/schemas/) { get; } | Especifica el conjunto de esquemas XML que están asociados con esta parte XML personalizada. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Clone](../../aspose.words.markup/customxmlpart/clone/)() | Realiza una copia "suficientemente profunda" del objeto. No duplica los bytes del objeto.[`Data`](./data/) valor. |

## Observaciones

Un documento DOCX o DOC puede contener una o más partes de almacenamiento de datos XML personalizados. Aspose.Words conserva y permite crear y extraer datos XML personalizados mediante[`CustomXmlParts`](../../aspose.words/document/customxmlparts/) recopilación.

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

* espacio de nombres [Aspose.Words.Markup](../../aspose.words.markup/)
* asamblea [Aspose.Words](../../)
