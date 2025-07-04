---
title: XmlMapping.StoreItemId
linktitle: StoreItemId
articleTitle: StoreItemId
second_title: Aspose.Words for .NET
description: Discover the XmlMapping StoreItemId property for custom XML data identifiers. Enhance XPath evaluation with our unique solutions for efficient data management.
type: docs
weight: 40
url: /net/aspose.words.markup/xmlmapping/storeitemid/
---
## XmlMapping.StoreItemId property

Specifies the custom XML data identifier for the custom XML data part which shall be used to evaluate the [`XPath`](../xpath/) expression.

```csharp
public string StoreItemId { get; }
```

## Examples

Shows how to get the custom XML data identifier of an XML part.

```csharp
Document doc = new Document(MyDir + "Custom XML part in structured document tag.docx");

// Structured document tags have IDs in the form of GUIDs.
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 0, true);

Assert.That(tag.XmlMapping.StoreItemId, Is.EqualTo("{F3029283-4FF8-4DD2-9F31-395F19ACEE85}"));
```

### See Also

* class [XmlMapping](../)
* namespace [Aspose.Words.Markup](../../../aspose.words.markup/)
* assembly [Aspose.Words](../../../)
