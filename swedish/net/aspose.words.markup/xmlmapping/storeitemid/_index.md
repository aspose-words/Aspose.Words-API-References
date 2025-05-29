---
title: XmlMapping.StoreItemId
linktitle: StoreItemId
articleTitle: StoreItemId
second_title: Aspose.Words för .NET
description: Upptäck egenskapen XmlMapping StoreItemId för anpassade XML-dataidentifierare. Förbättra XPath-utvärderingen med våra unika lösningar för effektiv datahantering.
type: docs
weight: 40
url: /sv/net/aspose.words.markup/xmlmapping/storeitemid/
---
## XmlMapping.StoreItemId property

Anger den anpassade XML-dataidentifieraren för den anpassade XML-datadelen som ska användas för att utvärdera[`XPath`](../xpath/) uttryck.

```csharp
public string StoreItemId { get; }
```

## Exempel

Visar hur man hämtar den anpassade XML-dataidentifieraren för en XML-del.

```csharp
Document doc = new Document(MyDir + "Custom XML part in structured document tag.docx");

// Taggar för strukturerade dokument har ID:n i form av GUID:er.
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 0, true);

Assert.AreEqual("{F3029283-4FF8-4DD2-9F31-395F19ACEE85}", tag.XmlMapping.StoreItemId);
```

### Se även

* class [XmlMapping](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
