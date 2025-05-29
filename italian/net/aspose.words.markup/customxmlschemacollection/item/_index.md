---
title: CustomXmlSchemaCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words per .NET
description: Scopri come gestire gli elementi di CustomXmlSchemaCollection senza sforzo. Impara a ottenere o impostare elementi tramite indice per una gestione semplificata dei dati XML.
type: docs
weight: 20
url: /it/net/aspose.words.markup/customxmlschemacollection/item/
---
## CustomXmlSchemaCollection indexer

Ottiene o imposta l'elemento all'indice specificato.

```csharp
public string this[int index] { get; set; }
```

## Esempi

Mostra come lavorare con una raccolta di schemi XML.

```csharp
Document doc = new Document();

string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello, World!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

// Aggiungere un'associazione di schema XML.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Clona la raccolta di associazioni di schemi XML della parte XML personalizzata,
// e quindi aggiungere un paio di nuovi schemi al clone.
CustomXmlSchemaCollection schemas = xmlPart.Schemas.Clone();
schemas.Add("http://www.w3.org/2001/XMLSchema-instance");
schemas.Add("http://schemas.microsoft.com/office/2006/metadata/contentType");

Assert.AreEqual(3, schemas.Count);
Assert.AreEqual(2, schemas.IndexOf("http://schemas.microsoft.com/office/2006/metadata/contentType"));

// Enumera gli schemi e stampa ciascun elemento.
using (IEnumerator<string> enumerator = schemas.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine(enumerator.Current);
}

// Di seguito sono riportati tre metodi per rimuovere gli schemi dalla raccolta.
// 1 - Rimuovi uno schema tramite indice:
schemas.RemoveAt(2);

// 2 - Rimuovi uno schema in base al valore:
schemas.Remove("http://www.w3.org/2001/XMLSchema");

// 3 - Utilizzare il metodo "Clear" per svuotare immediatamente la raccolta.
schemas.Clear();

Assert.AreEqual(0, schemas.Count);
```

### Guarda anche

* class [CustomXmlSchemaCollection](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
