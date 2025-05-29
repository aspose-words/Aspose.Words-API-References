---
title: StructuredDocumentTag.XmlMapping
linktitle: XmlMapping
articleTitle: XmlMapping
second_title: Aspose.Words per .NET
description: Scopri come la proprietà StructuredDocumentTag XmlMapping collega i tuoi tag ai dati XML, migliorando la personalizzazione e l'integrazione dei documenti per flussi di lavoro fluidi.
type: docs
weight: 320
url: /it/net/aspose.words.markup/structureddocumenttag/xmlmapping/
---
## StructuredDocumentTag.XmlMapping property

Ottiene un oggetto che rappresenta la mappatura di questo tag di documento strutturato ai dati XML in una parte XML personalizzata del documento corrente.

```csharp
public XmlMapping XmlMapping { get; }
```

## Osservazioni

Puoi usare il[`SetMapping`](../../xmlmapping/setmapping/) metodo di questo oggetto per mappare un tag di documento strutturato su dati XML.

## Esempi

Mostra come creare un tag di documento strutturato con dati XML personalizzati.

```csharp
Document doc = new Document();

// Costruisci una parte XML che contiene dati e aggiungila alla raccolta del documento.
// Se abilitiamo la scheda "Sviluppatore" in Microsoft Word,
// possiamo trovare gli elementi di questa raccolta nel "XML Mapping Pane", insieme ad alcuni elementi predefiniti.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello world!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual(Encoding.ASCII.GetBytes(xmlPartContent), xmlPart.Data);
Assert.AreEqual(xmlPartId, xmlPart.Id);

// Di seguito sono riportati due modi per fare riferimento alle parti XML.
// 1 - Tramite un indice nella raccolta di parti XML personalizzate:
Assert.AreEqual(xmlPart, doc.CustomXmlParts[0]);

// 2 - Per GUID:
Assert.AreEqual(xmlPart, doc.CustomXmlParts.GetById(xmlPartId));

// Aggiungere un'associazione di schema XML.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Clona una parte e poi inseriscila nella raccolta.
CustomXmlPart xmlPartClone = xmlPart.Clone();
xmlPartClone.Id = Guid.NewGuid().ToString("B");
doc.CustomXmlParts.Add(xmlPartClone);

Assert.AreEqual(2, doc.CustomXmlParts.Count);

// Esegue l'iterazione nella raccolta e stampa il contenuto di ogni parte.
using (IEnumerator<CustomXmlPart> enumerator = doc.CustomXmlParts.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"XML part index {index}, ID: {enumerator.Current.Id}");
        Console.WriteLine($"\tContent: {Encoding.UTF8.GetString(enumerator.Current.Data)}");
        index++;
    }
}

// Utilizzare il metodo "RemoveAt" per rimuovere la parte clonata in base all'indice.
doc.CustomXmlParts.RemoveAt(1);

Assert.AreEqual(1, doc.CustomXmlParts.Count);

// Clonare la raccolta di parti XML, quindi utilizzare il metodo "Clear" per rimuovere tutti i suoi elementi in una volta.
CustomXmlPartCollection customXmlParts = doc.CustomXmlParts.Clone();
customXmlParts.Clear();

// Creiamo un tag di documento strutturato che visualizzerà il contenuto della nostra parte e lo inserirà nel corpo del documento.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[1]", string.Empty);

doc.FirstSection.Body.AppendChild(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CustomXml.docx");
```

### Guarda anche

* class [XmlMapping](../../xmlmapping/)
* class [StructuredDocumentTag](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
