---
title: XmlMapping.XPath
linktitle: XPath
articleTitle: XPath
second_title: Aspose.Words per .NET
description: XmlMapping XPath proprietà. Restituisce lespressione XPath che viene valutata per trovare il nodo XML personalizzato mappato al tag del documento strutturato padre in C#.
type: docs
weight: 50
url: /it/net/aspose.words.markup/xmlmapping/xpath/
---
## XmlMapping.XPath property

Restituisce l'espressione XPath, che viene valutata per trovare il nodo XML personalizzato mappato al tag del documento strutturato padre.

```csharp
public string XPath { get; }
```

## Esempi

Mostra come impostare mapping XML per parti XML personalizzate.

```csharp
Document doc = new Document();

// Costruisce una parte XML che contiene testo e la aggiunge alla raccolta CustomXmlPart del documento.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Text element #1</text><text>Text element #2</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual("<root><text>Text element #1</text><text>Text element #2</text></root>", 
    Encoding.UTF8.GetString(xmlPart.Data));

// Crea un tag di documento strutturato che visualizzerà il contenuto della nostra CustomXmlPart.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);

// Imposta una mappatura per il nostro tag di documento strutturato. Questa mappatura darà istruzioni
// il nostro tag di documento strutturato per visualizzare una parte del contenuto testuale della parte XML a cui punta XPath.
// In questo caso, sarà il contenuto del secondo "<text>" elemento del primo "<root>" elemento: "Elemento di testo n. 2".
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
