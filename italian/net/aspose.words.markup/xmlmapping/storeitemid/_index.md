---
title: XmlMapping.StoreItemId
linktitle: StoreItemId
articleTitle: StoreItemId
second_title: Aspose.Words per .NET
description: Scopri la proprietà StoreItemId di XmlMapping per gli identificatori di dati XML personalizzati. Migliora la valutazione XPath con le nostre soluzioni esclusive per una gestione efficiente dei dati.
type: docs
weight: 40
url: /it/net/aspose.words.markup/xmlmapping/storeitemid/
---
## XmlMapping.StoreItemId property

Specifica l'identificatore di dati XML personalizzato per la parte di dati XML personalizzata che deve essere utilizzata per valutare il[`XPath`](../xpath/) espressione.

```csharp
public string StoreItemId { get; }
```

## Esempi

Mostra come ottenere l'identificatore di dati XML personalizzato di una parte XML.

```csharp
Document doc = new Document(MyDir + "Custom XML part in structured document tag.docx");

// I tag dei documenti strutturati hanno ID sotto forma di GUID.
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 0, true);

Assert.AreEqual("{F3029283-4FF8-4DD2-9F31-395F19ACEE85}", tag.XmlMapping.StoreItemId);
```

### Guarda anche

* class [XmlMapping](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
