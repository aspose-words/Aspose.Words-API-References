---
title: CustomXmlSchemaCollection Class
linktitle: CustomXmlSchemaCollection
articleTitle: CustomXmlSchemaCollection
second_title: Aspose.Words per .NET
description: Esplora la classe Aspose.Words.Markup.CustomXmlSchemaCollection per gestire gli schemi XML collegati alle parti XML personalizzate, migliorando la flessibilità e il controllo dei documenti.
type: docs
weight: 4650
url: /it/net/aspose.words.markup/customxmlschemacollection/
---
## CustomXmlSchemaCollection class

Una raccolta di stringhe che rappresentano schemi XML associati a una parte XML personalizzata.

Per saperne di più, visita il[Tag di documenti strutturati o controllo dei contenuti](https://docs.aspose.com/words/net/working-with-content-control-sdt/) articolo di documentazione.

```csharp
public class CustomXmlSchemaCollection : IEnumerable<string>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.markup/customxmlschemacollection/count/) { get; } | Ottiene il numero di elementi contenuti nella raccolta. |
| [Item](../../aspose.words.markup/customxmlschemacollection/item/) { get; set; } | Ottiene o imposta l'elemento all'indice specificato. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlschemacollection/add/)(*string*) | Aggiunge un elemento alla collezione. |
| [Clear](../../aspose.words.markup/customxmlschemacollection/clear/)() | Rimuove tutti gli elementi dalla raccolta. |
| [Clone](../../aspose.words.markup/customxmlschemacollection/clone/)() | Crea un clone profondo di questo oggetto. |
| [GetEnumerator](../../aspose.words.markup/customxmlschemacollection/getenumerator/)() | Restituisce un oggetto enumeratore che può essere utilizzato per scorrere tutti gli elementi nella raccolta. |
| [IndexOf](../../aspose.words.markup/customxmlschemacollection/indexof/)(*string*) | Restituisce l'indice basato su zero del valore specificato nella raccolta. |
| [Remove](../../aspose.words.markup/customxmlschemacollection/remove/)(*string*) | Rimuove il valore specificato dalla raccolta. |
| [RemoveAt](../../aspose.words.markup/customxmlschemacollection/removeat/)(*int*) | Rimuove un valore all'indice specificato. |

## Osservazioni

Non è necessario creare istanze di questa classe. Si accede alla raccolta di schemi XML di un XML personalizzato part tramite[`Schemas`](../customxmlpart/schemas/) proprietà.

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

* spazio dei nomi [Aspose.Words.Markup](../../aspose.words.markup/)
* assemblea [Aspose.Words](../../)
