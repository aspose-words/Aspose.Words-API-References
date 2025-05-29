---
title: OdsoFieldMapDataCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words per .NET
description: Scopri la proprietà Item di OdsoFieldMapDataCollection per gestire e personalizzare facilmente la tua raccolta dati. Migliora la gestione dei tuoi dati oggi stesso!
type: docs
weight: 30
url: /it/net/aspose.words.settings/odsofieldmapdatacollection/item/
---
## OdsoFieldMapDataCollection indexer

Ottiene o imposta un elemento in questa raccolta.

```csharp
public OdsoFieldMapData this[int index] { get; set; }
```

## Esempi

Mostra come accedere alla raccolta di dati che mappa le colonne dell'origine dati ai campi di unione.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

// Questa raccolta definisce come una stampa unione mapperà le colonne da un'origine dati
// ai campi predefiniti MERGEFIELD, ADDRESSBLOCK e GREETINGLINE.
OdsoFieldMapDataCollection dataCollection = doc.MailMergeSettings.Odso.FieldMapDatas;
Assert.AreEqual(30, dataCollection.Count);

using (IEnumerator<OdsoFieldMapData> enumerator = dataCollection.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"Field map data index {index++}, type \"{enumerator.Current.Type}\":");

        Console.WriteLine(
            enumerator.Current.Type != OdsoFieldMappingType.Null
                ? $"\tColumn \"{enumerator.Current.Name}\", number {enumerator.Current.Column} mapped to merge field \"{enumerator.Current.MappedName}\"."
                : "\tNo valid column to field mapping data present.");
    }
}

// Clona gli elementi in questa raccolta.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// Utilizzare gli elementi del metodo "RemoveAt" singolarmente in base all'indice.
dataCollection.RemoveAt(0);

Assert.AreEqual(29, dataCollection.Count);

// Utilizzare il metodo "Clear" per cancellare l'intera raccolta in una sola volta.
dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Guarda anche

* class [OdsoFieldMapData](../../odsofieldmapdata/)
* class [OdsoFieldMapDataCollection](../)
* spazio dei nomi [Aspose.Words.Settings](../../../aspose.words.settings/)
* assemblea [Aspose.Words](../../../)
