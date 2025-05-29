---
title: StructuredDocumentTagRangeStart.XmlMapping
linktitle: XmlMapping
articleTitle: XmlMapping
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad StructuredDocumentTagRangeStart XmlMapping conecta el rango de etiquetas de su documento a datos XML personalizados, mejorando la integración del documento.
type: docs
weight: 190
url: /es/net/aspose.words.markup/structureddocumenttagrangestart/xmlmapping/
---
## StructuredDocumentTagRangeStart.XmlMapping property

Obtiene un objeto que representa la asignación de este rango de etiquetas de documento estructurado a datos XML en una parte XML personalizada del documento actual.

```csharp
public XmlMapping XmlMapping { get; }
```

## Observaciones

Puedes utilizar el[`SetMapping`](../../xmlmapping/setmapping/) método de este objeto para asignar un rango de etiquetas de documento estructurado a datos XML.

## Ejemplos

Muestra cómo establecer asignaciones XML para el inicio del rango de una etiqueta de documento estructurado.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");

// Construya una parte XML que contenga texto y agréguela a la colección CustomXmlPart del documento.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Text element #1</text><text>Text element #2</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual("<root><text>Text element #1</text><text>Text element #2</text></root>",
    Encoding.UTF8.GetString(xmlPart.Data));

// Cree una etiqueta de documento estructurado que mostrará el contenido de nuestro CustomXmlPart en el documento.
StructuredDocumentTagRangeStart sdtRangeStart = (StructuredDocumentTagRangeStart)doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true);

// Si establecemos una asignación para nuestra etiqueta de documento estructurado,
// solo mostrará una parte de CustomXmlPart a la que apunta XPath.
// Este XPath apuntará al contenido del segundo elemento "<text>" del primer elemento "<root>" de nuestro CustomXmlPart.
sdtRangeStart.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", null);

doc.Save(ArtifactsDir + "StructuredDocumentTag.StructuredDocumentTagRangeStartXmlMapping.docx");
```

### Ver también

* class [XmlMapping](../../xmlmapping/)
* class [StructuredDocumentTagRangeStart](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
