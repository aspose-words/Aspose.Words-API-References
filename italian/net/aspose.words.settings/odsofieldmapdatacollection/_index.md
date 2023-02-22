---
title: Class OdsoFieldMapDataCollection
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Settings.OdsoFieldMapDataCollection classe. Una raccolta tipizzata diOdsoFieldMapData oggetti.
type: docs
weight: 5610
url: /it/net/aspose.words.settings/odsofieldmapdatacollection/
---
## OdsoFieldMapDataCollection class

Una raccolta tipizzata di[`OdsoFieldMapData`](../odsofieldmapdata/) oggetti.

```csharp
public class OdsoFieldMapDataCollection : IEnumerable<OdsoFieldMapData>
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [OdsoFieldMapDataCollection](odsofieldmapdatacollection/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.settings/odsofieldmapdatacollection/count/) { get; } | Ottiene il numero di elementi contenuti nella raccolta. |
| [Item](../../aspose.words.settings/odsofieldmapdatacollection/item/) { get; set; } | Ottiene o imposta un elemento in questa raccolta. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words.settings/odsofieldmapdatacollection/add/)(OdsoFieldMapData) | Aggiunge un oggetto alla fine di questa raccolta. |
| [Clear](../../aspose.words.settings/odsofieldmapdatacollection/clear/)() | Rimuove tutti gli elementi da questa raccolta. |
| [GetEnumerator](../../aspose.words.settings/odsofieldmapdatacollection/getenumerator/)() | Restituisce un oggetto enumeratore che può essere utilizzato per scorrere tutti gli elementi della raccolta. |
| [RemoveAt](../../aspose.words.settings/odsofieldmapdatacollection/removeat/)(int) | Rimuove l'elemento in corrispondenza dell'indice specificato. |

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

* class [OdsoFieldMapData](../odsofieldmapdata/)
* property [FieldMapDatas](../odso/fieldmapdatas/)
* spazio dei nomi [Aspose.Words.Settings](../../aspose.words.settings/)
* assemblea [Aspose.Words](../../)


