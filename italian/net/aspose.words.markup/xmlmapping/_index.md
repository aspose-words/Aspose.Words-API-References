---
title: XmlMapping Class
linktitle: XmlMapping
articleTitle: XmlMapping
second_title: Aspose.Words per .NET
description: Aspose.Words.Markup.XmlMapping classe. Specifica le informazioni utilizzate per stabilire una mappatura tra il tag del documento strutturato parent e un elemento XML archiviato allinterno di una parte di dati XML personalizzata nel documento in C#.
type: docs
weight: 4100
url: /it/net/aspose.words.markup/xmlmapping/
---
## XmlMapping class

Specifica le informazioni utilizzate per stabilire una mappatura tra il tag del documento strutturato parent e un elemento XML archiviato all'interno di una parte di dati XML personalizzata nel documento.

Per saperne di più, visita il[Tag di documenti strutturati o controllo del contenuto](https://docs.aspose.com/words/net/working-with-content-control-sdt/) articolo di documentazione.

```csharp
public class XmlMapping
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [CustomXmlPart](../../aspose.words.markup/xmlmapping/customxmlpart/) { get; } | Restituisce la parte di dati XML personalizzata a cui è mappato il tag del documento strutturato principale. |
| [IsMapped](../../aspose.words.markup/xmlmapping/ismapped/) { get; } | Restituisce`VERO` se il tag del documento strutturato principale è stato mappato correttamente sui dati XML. |
| [PrefixMappings](../../aspose.words.markup/xmlmapping/prefixmappings/) { get; } | Restituisce le mappature dei prefissi dello spazio dei nomi XML per valutare il file[`XPath`](./xpath/) . |
| [StoreItemId](../../aspose.words.markup/xmlmapping/storeitemid/) { get; } | Specifica l'identificatore di dati XML personalizzato per la parte di dati XML personalizzata che dovrà essere utilizzato per valutare il[`XPath`](./xpath/) espressione. |
| [XPath](../../aspose.words.markup/xmlmapping/xpath/) { get; } | Restituisce l'espressione XPath, che viene valutata per trovare il nodo XML personalizzato mappato al tag del documento strutturato padre. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Delete](../../aspose.words.markup/xmlmapping/delete/)() | Elimina la mappatura del documento strutturato principale ai dati XML. |
| [SetMapping](../../aspose.words.markup/xmlmapping/setmapping/)(*[CustomXmlPart](../customxmlpart/), string, string*) | Imposta una mappatura tra il tag del documento strutturato principale e un nodo XML di una parte di dati XML personalizzata. |

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

* spazio dei nomi [Aspose.Words.Markup](../../aspose.words.markup/)
* assemblea [Aspose.Words](../../)
