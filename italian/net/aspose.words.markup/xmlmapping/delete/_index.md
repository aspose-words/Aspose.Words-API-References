---
title: XmlMapping.Delete
linktitle: Delete
articleTitle: Delete
second_title: Aspose.Words per .NET
description: Rimuovi senza sforzo i mapping dei dati XML con il metodo XmlMapping Delete. Semplifica i tuoi documenti strutturati per migliorare efficienza e organizzazione.
type: docs
weight: 60
url: /it/net/aspose.words.markup/xmlmapping/delete/
---
## XmlMapping.Delete method

Elimina la mappatura del documento strutturato padre ai dati XML.

```csharp
public void Delete()
```

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
