---
title: OdsoFieldMappingType Enum
linktitle: OdsoFieldMappingType
articleTitle: OdsoFieldMappingType
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.OdsoFieldMappingType per un'efficiente mappatura dei campi di stampa unione a fonti dati esterne. Migliora l'automazione dei tuoi documenti oggi stesso!
type: docs
weight: 6750
url: /it/net/aspose.words.settings/odsofieldmappingtype/
---
## OdsoFieldMappingType enumeration

Specifica i possibili tipi utilizzati per indicare se un dato campo di unione di posta è stato mappato a una colonna nella data source esterna specificata.

```csharp
public enum OdsoFieldMappingType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Column | `0` | Specifica che il campo di unione dati è stato mappato a una colonna nella specifica origine dati esterna. |
| Null | `1` | Specifica che il campo di unione di posta non è stato mappato a una colonna nella fonte dati esterna specificata. |
| Default | `1` | Uguale aNull . |

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

* property [Type](../odsofieldmapdata/type/)
* spazio dei nomi [Aspose.Words.Settings](../../aspose.words.settings/)
* assemblea [Aspose.Words](../../)
