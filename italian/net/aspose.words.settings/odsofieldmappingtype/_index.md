---
title: OdsoFieldMappingType Enum
linktitle: OdsoFieldMappingType
articleTitle: OdsoFieldMappingType
second_title: Aspose.Words per .NET
description: Aspose.Words.Settings.OdsoFieldMappingType enum. Specifica i possibili tipi utilizzati per indicare se un determinato campo di stampa unione è stato mappato a una colonna nellorigine dati esterna specificata in C#.
type: docs
weight: 5920
url: /it/net/aspose.words.settings/odsofieldmappingtype/
---
## OdsoFieldMappingType enumeration

Specifica i possibili tipi utilizzati per indicare se un determinato campo di stampa unione è stato mappato a una colonna nell'origine dati esterna specificata.

```csharp
public enum OdsoFieldMappingType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Column | `0` | Specifica che il campo della stampa unione è stato mappato a una colonna nell'origine dati esterna specificata. |
| Null | `1` | Specifica che il campo della stampa unione non è stato mappato a una colonna nell'origine dati esterna specificata. |
| Default | `1` | Uguale aNull . |

## Esempi

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

* property [Type](../odsofieldmapdata/type/)
* spazio dei nomi [Aspose.Words.Settings](../../aspose.words.settings/)
* assemblea [Aspose.Words](../../)
