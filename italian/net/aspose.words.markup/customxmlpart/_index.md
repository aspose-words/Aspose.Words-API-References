---
title: CustomXmlPart Class
linktitle: CustomXmlPart
articleTitle: CustomXmlPart
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Markup.CustomXmlPart per una gestione efficiente dell'archiviazione di dati XML personalizzati all'interno dei pacchetti. Migliora l'elaborazione dei tuoi documenti oggi stesso!
type: docs
weight: 4610
url: /it/net/aspose.words.markup/customxmlpart/
---
## CustomXmlPart class

Rappresenta una parte di archiviazione dati XML personalizzata (dati XML personalizzati all'interno di un pacchetto).

Per saperne di più, visita il[Tag di documenti strutturati o controllo dei contenuti](https://docs.aspose.com/words/net/working-with-content-control-sdt/) articolo di documentazione.

```csharp
public class CustomXmlPart
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [CustomXmlPart](customxmlpart/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Data](../../aspose.words.markup/customxmlpart/data/) { get; set; } | Ottiene o imposta il contenuto XML di questa parte di archiviazione dati XML personalizzata. |
| [DataChecksum](../../aspose.words.markup/customxmlpart/datachecksum/) { get; } | Specifica un checksum del controllo di ridondanza ciclico (CRC) del[`Data`](./data/) contenuto. |
| [Id](../../aspose.words.markup/customxmlpart/id/) { get; set; } | Ottiene o imposta la stringa che identifica questa parte XML personalizzata all'interno di un documento OOXML. |
| [Schemas](../../aspose.words.markup/customxmlpart/schemas/) { get; } | Specifica il set di schemi XML associati a questa parte XML personalizzata. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Clone](../../aspose.words.markup/customxmlpart/clone/)() | Crea una copia "abbastanza profonda" dell'oggetto. Non duplica i byte dell'oggetto.[`Data`](./data/) valore. |

## Osservazioni

Un documento DOCX o DOC può contenere una o più parti di archiviazione dati XML personalizzate. Aspose.Words conserva e consente di creare ed estrarre dati XML personalizzati tramite[`CustomXmlParts`](../../aspose.words/document/customxmlparts/) collezione.

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

* spazio dei nomi [Aspose.Words.Markup](../../aspose.words.markup/)
* assemblea [Aspose.Words](../../)
