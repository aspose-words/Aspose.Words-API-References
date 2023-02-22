---
title: Class CustomXmlPart
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Markup.CustomXmlPart classe. Rappresenta una parte di archiviazione dati XML personalizzata dati XML personalizzati allinterno di un pacchetto.
type: docs
weight: 3680
url: /it/net/aspose.words.markup/customxmlpart/
---
## CustomXmlPart class

Rappresenta una parte di archiviazione dati XML personalizzata (dati XML personalizzati all'interno di un pacchetto).

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
| [DataChecksum](../../aspose.words.markup/customxmlpart/datachecksum/) { get; } | Specifica un checksum CRC (Cyclic Redundancy Check) del[`Data`](./data/) contenuto. |
| [Id](../../aspose.words.markup/customxmlpart/id/) { get; set; } | Ottiene o imposta la stringa che identifica questa parte XML personalizzata all'interno di un documento OOXML. |
| [Schemas](../../aspose.words.markup/customxmlpart/schemas/) { get; } | Specifica la serie di schemi XML associati a questa parte XML personalizzata. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Clone](../../aspose.words.markup/customxmlpart/clone/)() | Crea una copia "abbastanza profonda" dell'oggetto. Non duplica i byte del file[`Data`](./data/) valore. |

### Osservazioni

Un documento DOCX o DOC può contenere una o più parti di archiviazione dati XML personalizzata. Aspose.Words conserva e consente di creare ed estrarre dati XML personalizzati tramite il[`CustomXmlParts`](../../aspose.words/document/customxmlparts/) collezione.

### Esempi

Mostra come creare un tag di documento strutturato con dati XML personalizzati.

```csharp
Document doc = new Document();

// Costruisci una parte XML che contiene dati e aggiungila alla raccolta del documento.
// Se abilitiamo la scheda "Sviluppatore" in Microsoft Word,
// possiamo trovare elementi di questa raccolta nel "Riquadro mappatura XML", insieme ad alcuni elementi predefiniti.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello world!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual(Encoding.ASCII.GetBytes(xmlPartContent), xmlPart.Data);
Assert.AreEqual(xmlPartId, xmlPart.Id);

// Di seguito sono riportati due modi per fare riferimento alle parti XML.
// 1 - Da un indice nella raccolta di parti XML personalizzata:
Assert.AreEqual(xmlPart, doc.CustomXmlParts[0]);

// 2 - Per GUID:
Assert.AreEqual(xmlPart, doc.CustomXmlParts.GetById(xmlPartId));

// Aggiunge un'associazione dello schema XML.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Clona una parte, quindi inseriscila nella raccolta.
CustomXmlPart xmlPartClone = xmlPart.Clone();
xmlPartClone.Id = Guid.NewGuid().ToString("B");
doc.CustomXmlParts.Add(xmlPartClone);

Assert.AreEqual(2, doc.CustomXmlParts.Count);

// Scorri la raccolta e stampa il contenuto di ciascuna parte.
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

// Usa il metodo "RemoveAt" per rimuovere la parte clonata per indice.
doc.CustomXmlParts.RemoveAt(1);

Assert.AreEqual(1, doc.CustomXmlParts.Count);

// Clona la raccolta di parti XML, quindi usa il metodo "Clear" per rimuovere tutti i suoi elementi contemporaneamente.
CustomXmlPartCollection customXmlParts = doc.CustomXmlParts.Clone();
customXmlParts.Clear();

// Crea un tag di documento strutturato che visualizzerà il contenuto della nostra parte e lo inserirà nel corpo del documento.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[1]", string.Empty);

doc.FirstSection.Body.AppendChild(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CustomXml.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Markup](../../aspose.words.markup/)
* assemblea [Aspose.Words](../../)


