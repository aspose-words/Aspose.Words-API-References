---
title: Class CustomXmlPart
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Markup.CustomXmlPart clase. Representa una parte de almacenamiento de datos XML personalizados datos XML personalizados dentro de un paquete.
type: docs
weight: 3680
url: /es/net/aspose.words.markup/customxmlpart/
---
## CustomXmlPart class

Representa una parte de almacenamiento de datos XML personalizados (datos XML personalizados dentro de un paquete).

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
| [Data](../../aspose.words.markup/customxmlpart/data/) { get; set; } | Obtiene o establece el contenido XML de esta parte de almacenamiento de datos XML personalizados. |
| [DataChecksum](../../aspose.words.markup/customxmlpart/datachecksum/) { get; } | Especifica una suma de verificación de verificación de redundancia cíclica (CRC) del[`Data`](./data/) contenido. |
| [Id](../../aspose.words.markup/customxmlpart/id/) { get; set; } | Obtiene o establece la cadena que identifica esta parte XML personalizada dentro de un documento OOXML. |
| [Schemas](../../aspose.words.markup/customxmlpart/schemas/) { get; } | Especifica el conjunto de esquemas XML que están asociados con esta parte XML personalizada. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Clone](../../aspose.words.markup/customxmlpart/clone/)() | Realiza una copia "suficientemente profunda" del objeto. No duplica los bytes del[`Data`](./data/) valor. |

### Observaciones

Un documento DOCX o DOC puede contener una o más partes de almacenamiento de datos XML personalizado. Aspose.Words conserva y permite crear y extraer datos XML personalizados a través de la[`CustomXmlParts`](../../aspose.words/document/customxmlparts/) recopilación.

### Ejemplos

Muestra cómo crear una etiqueta de documento estructurado con datos XML personalizados.

```csharp
Document doc = new Document();

// Construya una parte XML que contenga datos y agréguela a la colección del documento.
// Si habilitamos la pestaña "Desarrollador" en Microsoft Word,
// podemos encontrar elementos de esta colección en el "Panel de mapeo XML", junto con algunos elementos predeterminados.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello world!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual(Encoding.ASCII.GetBytes(xmlPartContent), xmlPart.Data);
Assert.AreEqual(xmlPartId, xmlPart.Id);

// A continuación hay dos formas de referirse a las partes XML.
// 1 - Por un índice en la colección de piezas XML personalizadas:
Assert.AreEqual(xmlPart, doc.CustomXmlParts[0]);

// 2 - Por GUID:
Assert.AreEqual(xmlPart, doc.CustomXmlParts.GetById(xmlPartId));

// Agregar una asociación de esquema XML.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Clonar una parte y luego insertarla en la colección.
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

// Use el método "RemoveAt" para eliminar la parte clonada por índice.
doc.CustomXmlParts.RemoveAt(1);

Assert.AreEqual(1, doc.CustomXmlParts.Count);

// Clona la colección de piezas XML y luego usa el método "Borrar" para eliminar todos sus elementos a la vez.
CustomXmlPartCollection customXmlParts = doc.CustomXmlParts.Clone();
customXmlParts.Clear();

// Crear una etiqueta de documento estructurado que mostrará el contenido de nuestra parte e insertarlo en el cuerpo del documento.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[1]", string.Empty);

doc.FirstSection.Body.AppendChild(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CustomXml.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Markup](../../aspose.words.markup/)
* asamblea [Aspose.Words](../../)


