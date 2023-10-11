---
title: OdsoFieldMapData.Name
second_title: Aspose.Words per .NET API Reference
description: OdsoFieldMapData proprietà. Specifica il nome della colonna allinterno di unorigine dati esterna per la colonna il cui indice è specificato dalColumnproperty. Il valore predefinito è una stringa vuota.
type: docs
weight: 40
url: /it/net/aspose.words.settings/odsofieldmapdata/name/
---
## OdsoFieldMapData.Name property

Specifica il nome della colonna all'interno di un'origine dati esterna per la colonna il cui indice è specificato dal[`Column`](../column/)property. Il valore predefinito è una stringa vuota.

```csharp
public string Name { get; set; }
```

### Esempi

Mostra come accedere alla raccolta di dati che mappa le colonne dell'origine dati per unire i campi.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

// Questa raccolta definisce il modo in cui una stampa unione mapperà le colonne da un'origine dati
// ai campi MERGEFIELD, ADDRESSBLOCK e GREETINGLINE predefiniti.
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

// Utilizza gli elementi del metodo "RemoveAt" singolarmente per indice.
dataCollection.RemoveAt(0);

Assert.AreEqual(29, dataCollection.Count);

// Utilizza il metodo "Cancella" per cancellare l'intera raccolta in una volta.
dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Guarda anche

* class [OdsoFieldMapData](../)
* spazio dei nomi [Aspose.Words.Settings](../../odsofieldmapdata/)
* assemblea [Aspose.Words](../../../)


