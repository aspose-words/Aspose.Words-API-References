---
title: XmlMapping.PrefixMappings
linktitle: PrefixMappings
articleTitle: PrefixMappings
second_title: Aspose.Words per .NET
description: Scopri la proprietà XmlMapping PrefixMappings per una mappatura fluida dei prefissi degli spazi dei nomi XML e una valutazione efficiente di XPath. Migliora la tua elaborazione XML oggi stesso!
type: docs
weight: 30
url: /it/net/aspose.words.markup/xmlmapping/prefixmappings/
---
## XmlMapping.PrefixMappings property

Restituisce i mapping dei prefissi dello spazio dei nomi XML per valutare[`XPath`](../xpath/) .

```csharp
public string PrefixMappings { get; }
```

## Osservazioni

Specifica il set di mappature dei prefissi che devono essere utilizzate per interpretare l'espressione XPath quando l'espressione XPath viene valutata rispetto alle parti di dati XML personalizzate nel documento.

## Esempi

Mostra come impostare i mapping XML per le parti XML personalizzate.

```csharp
Document doc = new Document();

// Crea una parte XML che contiene testo e aggiungila alla raccolta CustomXmlPart del documento.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Text element #1</text><text>Text element #2</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual("<root><text>Text element #1</text><text>Text element #2</text></root>",
    Encoding.UTF8.GetString(xmlPart.Data));

// Crea un tag di documento strutturato che visualizzerà il contenuto del nostro CustomXmlPart.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);

// Imposta una mappatura per il nostro tag di documento strutturato. Questa mappatura istruirà
// il nostro tag di documento strutturato per visualizzare una porzione del contenuto di testo della parte XML a cui punta XPath.
// In questo caso, sarà il contenuto del secondo elemento "<text>" del primo elemento "<root>": "Elemento testo n. 2".
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", "xmlns:ns='http://www.w3.org/2001/XMLSchema'");

Assert.True(tag.XmlMapping.IsMapped);
Assert.AreEqual(xmlPart, tag.XmlMapping.CustomXmlPart);
Assert.AreEqual("/root[1]/text[2]", tag.XmlMapping.XPath);
Assert.AreEqual("xmlns:ns='http://www.w3.org/2001/XMLSchema'", tag.XmlMapping.PrefixMappings);

// Aggiungi il tag del documento strutturato al documento per visualizzare il contenuto della nostra parte personalizzata.
doc.FirstSection.Body.AppendChild(tag);
doc.Save(ArtifactsDir + "StructuredDocumentTag.XmlMapping.docx");
```

### Guarda anche

* class [XmlMapping](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
