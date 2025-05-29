---
title: XmlMapping.XPath
linktitle: XPath
articleTitle: XPath
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad XPath de XmlMapping localiza eficientemente nodos XML personalizados, mejorando la gestión de documentos estructurados con precisión y facilidad.
type: docs
weight: 50
url: /es/net/aspose.words.markup/xmlmapping/xpath/
---
## XmlMapping.XPath property

Devuelve la expresión XPath, que se evalúa para encontrar el nodo XML personalizado que está asignado a la etiqueta del documento estructurado principal.

```csharp
public string XPath { get; }
```

## Ejemplos

Muestra cómo establecer asignaciones XML para partes XML personalizadas.

```csharp
Document doc = new Document();

// Construya una parte XML que contenga texto y agréguela a la colección CustomXmlPart del documento.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Text element #1</text><text>Text element #2</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual("<root><text>Text element #1</text><text>Text element #2</text></root>",
    Encoding.UTF8.GetString(xmlPart.Data));

// Cree una etiqueta de documento estructurado que mostrará el contenido de nuestro CustomXmlPart.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);

// Establezca una asignación para nuestra etiqueta de documento estructurado. Esta asignación indicará
// nuestra etiqueta de documento estructurado para mostrar una parte del contenido de texto de la parte XML a la que apunta XPath.
// En este caso, será el contenido del segundo elemento "<text>" del primer elemento "<root>": "Elemento de texto n.° 2".
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", "xmlns:ns='http://www.w3.org/2001/XMLSchema'");

Assert.True(tag.XmlMapping.IsMapped);
Assert.AreEqual(xmlPart, tag.XmlMapping.CustomXmlPart);
Assert.AreEqual("/root[1]/text[2]", tag.XmlMapping.XPath);
Assert.AreEqual("xmlns:ns='http://www.w3.org/2001/XMLSchema'", etiqueta.XmlMapping.PrefixMappings);

// Agregue la etiqueta de documento estructurado al documento para mostrar el contenido de nuestra parte personalizada.
doc.FirstSection.Body.AppendChild(tag);
doc.Save(ArtifactsDir + "StructuredDocumentTag.XmlMapping.docx");
```

### Ver también

* class [XmlMapping](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
