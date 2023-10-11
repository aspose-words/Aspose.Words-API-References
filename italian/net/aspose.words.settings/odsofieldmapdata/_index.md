---
title: Class OdsoFieldMapData
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Settings.OdsoFieldMapData classe. Specifica come una colonna nellorigine dati esterna deve essere mappata ai campi di unione predefiniti allinterno del documento.
type: docs
weight: 5900
url: /it/net/aspose.words.settings/odsofieldmapdata/
---
## OdsoFieldMapData class

Specifica come una colonna nell'origine dati esterna deve essere mappata ai campi di unione predefiniti all'interno del documento.

Per saperne di più, visita il[Stampa unione e reporting](https://docs.aspose.com/words/net/mail-merge-and-reporting/) articolo di documentazione.

```csharp
public class OdsoFieldMapData
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [OdsoFieldMapData](odsofieldmapdata/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Column](../../aspose.words.settings/odsofieldmapdata/column/) { get; set; } | Specifica l'indice in base zero della colonna all'interno di un'origine dati esterna che deve essere mappata al nome locale di un campo MERGEFIELD specifico. Il valore predefinito è 0. |
| [MappedName](../../aspose.words.settings/odsofieldmapdata/mappedname/) { get; set; } | Specifica il nome del campo di unione predefinito che verrà mappato al numero di colonna specificato dal[`Column`](./column/) proprietà all'interno di questo campo mapping. Il valore predefinito è una stringa vuota. |
| [Name](../../aspose.words.settings/odsofieldmapdata/name/) { get; set; } | Specifica il nome della colonna all'interno di un'origine dati esterna per la colonna il cui indice è specificato dal[`Column`](./column/)property. Il valore predefinito è una stringa vuota. |
| [Type](../../aspose.words.settings/odsofieldmapdata/type/) { get; set; } | Specifica se un determinato campo di stampa unione è stato mappato o meno a una colonna nell'origine dati esterna specificata. Il valore predefinito èDefault . |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Clone](../../aspose.words.settings/odsofieldmapdata/clone/)() | Restituisce un clone profondo di questo oggetto. |

### Osservazioni

Microsoft Word fornisce alcuni nomi di campi di unione predefiniti che consente di inserire in un documento come MERGEFIELD o utilizzare nei campi ADDRESSBLOCK o GREETINGLINE. Le informazioni specificate n`OdsoFieldMapData` consente di mappare una colonna nell'origine dati esterna a un singolo campo di unione predefinito.

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

* spazio dei nomi [Aspose.Words.Settings](../../aspose.words.settings/)
* assemblea [Aspose.Words](../../)


