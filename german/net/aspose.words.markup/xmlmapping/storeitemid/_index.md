---
title: XmlMapping.StoreItemId
linktitle: StoreItemId
articleTitle: StoreItemId
second_title: Aspose.Words für .NET
description: Entdecken Sie die XmlMapping StoreItemId-Eigenschaft für benutzerdefinierte XML-Datenkennungen. Verbessern Sie die XPath-Auswertung mit unseren einzigartigen Lösungen für effizientes Datenmanagement.
type: docs
weight: 40
url: /de/net/aspose.words.markup/xmlmapping/storeitemid/
---
## XmlMapping.StoreItemId property

Gibt den benutzerdefinierten XML-Datenbezeichner für den benutzerdefinierten XML-Datenteil an, der zur Auswertung der[`XPath`](../xpath/) Ausdruck.

```csharp
public string StoreItemId { get; }
```

## Beispiele

Zeigt, wie die benutzerdefinierte XML-Datenkennung eines XML-Teils abgerufen wird.

```csharp
Document doc = new Document(MyDir + "Custom XML part in structured document tag.docx");

// Strukturierte Dokument-Tags haben IDs in Form von GUIDs.
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 0, true);

Assert.AreEqual("{F3029283-4FF8-4DD2-9F31-395F19ACEE85}", tag.XmlMapping.StoreItemId);
```

### Siehe auch

* class [XmlMapping](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
