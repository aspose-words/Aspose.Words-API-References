---
title: StructuredDocumentTagRangeStart.XmlMapping
linktitle: XmlMapping
articleTitle: XmlMapping
second_title: Aspose.Words per .NET
description: Scopri come la proprietà StructuredDocumentTagRangeStart XmlMapping collega l'intervallo di tag del tuo documento ai dati XML personalizzati, migliorando l'integrazione dei documenti.
type: docs
weight: 190
url: /it/net/aspose.words.markup/structureddocumenttagrangestart/xmlmapping/
---
## StructuredDocumentTagRangeStart.XmlMapping property

Ottiene un oggetto che rappresenta la mappatura di questo intervallo di tag di documenti strutturati ai dati XML in una parte XML personalizzata del documento corrente.

```csharp
public XmlMapping XmlMapping { get; }
```

## Osservazioni

Puoi usare il[`SetMapping`](../../xmlmapping/setmapping/) metodo dell'oggetto this per mappare un intervallo di tag di documento strutturato ai dati XML.

## Esempi

Mostra come impostare i mapping XML per l'inizio dell'intervallo di un tag di documento strutturato.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");

// Crea una parte XML che contiene testo e aggiungila alla raccolta CustomXmlPart del documento.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Text element #1</text><text>Text element #2</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual("<root><text>Text element #1</text><text>Text element #2</text></root>",
    Encoding.UTF8.GetString(xmlPart.Data));

// Crea un tag di documento strutturato che visualizzerà il contenuto del nostro CustomXmlPart nel documento.
StructuredDocumentTagRangeStart sdtRangeStart = (StructuredDocumentTagRangeStart)doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true);

// Se impostiamo una mappatura per il nostro tag di documento strutturato,
// verrà visualizzata solo una parte di CustomXmlPart a cui punta XPath.
// Questo XPath punterà al contenuto del secondo elemento "<text>" del primo elemento "<root>" del nostro CustomXmlPart.
sdtRangeStart.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", null);

doc.Save(ArtifactsDir + "StructuredDocumentTag.StructuredDocumentTagRangeStartXmlMapping.docx");
```

### Guarda anche

* class [XmlMapping](../../xmlmapping/)
* class [StructuredDocumentTagRangeStart](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
