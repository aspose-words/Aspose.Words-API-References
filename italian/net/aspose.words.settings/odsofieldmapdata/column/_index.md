---
title: OdsoFieldMapData.Column
second_title: Aspose.Words per .NET API Reference
description: OdsoFieldMapData proprietà. Specifica lindice in base zero della colonna allinterno di unorigine dati esterna che deve essere mappato al nome locale di un campo MERGEFIELD specifico. Il valore predefinito è 0.
type: docs
weight: 20
url: /it/net/aspose.words.settings/odsofieldmapdata/column/
---
## OdsoFieldMapData.Column property

Specifica l'indice in base zero della colonna all'interno di un'origine dati esterna che deve essere mappato al nome locale di un campo MERGEFIELD specifico. Il valore predefinito è 0.

```csharp
public int Column { get; set; }
```

### Esempi

Mostra come accedere alla raccolta di dati che mappa le colonne dell'origine dati per unire i campi.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

// Questa raccolta definisce come una stampa unione mapperà le colonne da un'origine dati
// ai campi MERGEFIELD, ADDRESSBLOCK e GREETINGLINE.
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

// Usa gli elementi del metodo "RemoveAt" individualmente per indice.
dataCollection.RemoveAt(0);

Assert.AreEqual(29, dataCollection.Count);

// Usa il metodo "Cancella" per cancellare l'intera collezione in una volta.
dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Guarda anche

* class [OdsoFieldMapData](../)
* spazio dei nomi [Aspose.Words.Settings](../../odsofieldmapdata/)
* assemblea [Aspose.Words](../../../)


