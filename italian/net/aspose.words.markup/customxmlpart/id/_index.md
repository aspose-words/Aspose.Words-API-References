---
title: CustomXmlPart.Id
second_title: Aspose.Words per .NET API Reference
description: CustomXmlPart proprietà. Ottiene o imposta la stringa che identifica questa parte XML personalizzata allinterno di un documento OOXML.
type: docs
weight: 40
url: /it/net/aspose.words.markup/customxmlpart/id/
---
## CustomXmlPart.Id property

Ottiene o imposta la stringa che identifica questa parte XML personalizzata all'interno di un documento OOXML.

```csharp
public string Id { get; set; }
```

### Osservazioni

ISO/IEC 29500 specifica che questo valore è un GUID, ma le vecchie versioni di Microsoft Word consentivano qualsiasi stringa qui. Aspose.Words fa lo stesso per il formato ECMA-376. Tieni presente, tuttavia, che Microsoft Word Online non riesce ad aprire un documento creato con un valore non GUID. Pertanto, un GUID è il valore preferito per questa proprietà.

Un valore valido deve essere un identificatore univoco tra tutte le parti di dati XML personalizzate in questo documento.

Il valore predefinito è una stringa vuota. Il valore non può essere`nullo`.

### Esempi

Mostra come creare un tag di documento strutturato con dati XML personalizzati.

```csharp
Document doc = new Document();

// Costruisce una parte XML che contiene dati e la aggiunge alla raccolta del documento.
// Se abilitiamo la scheda "Sviluppatore" in Microsoft Word,
// possiamo trovare gli elementi di questa raccolta nel "riquadro di mappatura XML", insieme ad alcuni elementi predefiniti.
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

// Aggiunge un'associazione allo schema XML.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Clona una parte, quindi inseriscila nella raccolta.
CustomXmlPart xmlPartClone = xmlPart.Clone();
xmlPartClone.Id = Guid.NewGuid().ToString("B");
doc.CustomXmlParts.Add(xmlPartClone);

Assert.AreEqual(2, doc.CustomXmlParts.Count);

// Scorrere la raccolta e stampare il contenuto di ciascuna parte.
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

// Utilizza il metodo "RemoveAt" per rimuovere la parte clonata per indice.
doc.CustomXmlParts.RemoveAt(1);

Assert.AreEqual(1, doc.CustomXmlParts.Count);

// Clona la raccolta di parti XML, quindi utilizza il metodo "Clear" per rimuovere tutti i suoi elementi contemporaneamente.
CustomXmlPartCollection customXmlParts = doc.CustomXmlParts.Clone();
customXmlParts.Clear();

// Crea un tag di documento strutturato che visualizzerà il contenuto della nostra parte e lo inserirà nel corpo del documento.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[1]", string.Empty);

doc.FirstSection.Body.AppendChild(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CustomXml.docx");
```

### Guarda anche

* class [CustomXmlPart](../)
* spazio dei nomi [Aspose.Words.Markup](../../customxmlpart/)
* assemblea [Aspose.Words](../../../)


