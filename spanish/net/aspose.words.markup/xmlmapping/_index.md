---
title: XmlMapping Class
linktitle: XmlMapping
articleTitle: XmlMapping
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Markup.XmlMapping para vincular sin problemas etiquetas de documentos estructurados con elementos XML, mejorando la integración de datos de su documento.
type: docs
weight: 4790
url: /es/net/aspose.words.markup/xmlmapping/
---
## XmlMapping class

Especifica la información que se utiliza para establecer una asignación entre la etiqueta de documento estructurado parent y un elemento XML almacenado dentro de una parte de datos XML personalizada en el documento.

Para obtener más información, visite el[Etiquetas de documentos estructurados o control de contenido](https://docs.aspose.com/words/net/working-with-content-control-sdt/) Artículo de documentación.

```csharp
public class XmlMapping
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CustomXmlPart](../../aspose.words.markup/xmlmapping/customxmlpart/) { get; } | Devuelve la parte de datos XML personalizada a la que está asignada la etiqueta del documento estructurado principal. |
| [IsMapped](../../aspose.words.markup/xmlmapping/ismapped/) { get; } | Devuelve`verdadero` Si la etiqueta del documento estructurado principal se asigna correctamente a los datos XML. |
| [PrefixMappings](../../aspose.words.markup/xmlmapping/prefixmappings/) { get; } | Devuelve las asignaciones de prefijos de espacios de nombres XML para evaluar el[`XPath`](./xpath/) . |
| [StoreItemId](../../aspose.words.markup/xmlmapping/storeitemid/) { get; } | Especifica el identificador de datos XML personalizado para la parte de datos XML personalizada que se utilizará para evaluar[`XPath`](./xpath/) expresión. |
| [XPath](../../aspose.words.markup/xmlmapping/xpath/) { get; } | Devuelve la expresión XPath, que se evalúa para encontrar el nodo XML personalizado que está asignado a la etiqueta del documento estructurado principal. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Delete](../../aspose.words.markup/xmlmapping/delete/)() | Elimina la asignación del documento estructurado principal a datos XML. |
| [SetMapping](../../aspose.words.markup/xmlmapping/setmapping/)(*[CustomXmlPart](../customxmlpart/), string, string*) | Establece una asignación entre la etiqueta del documento estructurado principal y un nodo XML de una parte de datos XML personalizada. |

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

* espacio de nombres [Aspose.Words.Markup](../../aspose.words.markup/)
* asamblea [Aspose.Words](../../)
