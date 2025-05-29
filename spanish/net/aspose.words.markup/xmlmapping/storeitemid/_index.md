---
title: XmlMapping.StoreItemId
linktitle: StoreItemId
articleTitle: StoreItemId
second_title: Aspose.Words para .NET
description: Descubra la propiedad StoreItemId de XmlMapping para identificadores de datos XML personalizados. Mejore la evaluación de XPath con nuestras soluciones únicas para una gestión de datos eficiente.
type: docs
weight: 40
url: /es/net/aspose.words.markup/xmlmapping/storeitemid/
---
## XmlMapping.StoreItemId property

Especifica el identificador de datos XML personalizado para la parte de datos XML personalizada que se utilizará para evaluar[`XPath`](../xpath/) expresión.

```csharp
public string StoreItemId { get; }
```

## Ejemplos

Muestra cómo obtener el identificador de datos XML personalizado de una parte XML.

```csharp
Document doc = new Document(MyDir + "Custom XML part in structured document tag.docx");

// Las etiquetas de documentos estructurados tienen identificadores en forma de GUID.
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 0, true);

Assert.AreEqual("{F3029283-4FF8-4DD2-9F31-395F19ACEE85}", tag.XmlMapping.StoreItemId);
```

### Ver también

* class [XmlMapping](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
