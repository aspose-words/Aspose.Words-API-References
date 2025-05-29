---
title: OdsoFieldMapData Class
linktitle: OdsoFieldMapData
articleTitle: OdsoFieldMapData
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.OdsoFieldMapData per una mappatura fluida delle colonne di dati esterni sui campi di unione dei documenti predefiniti, migliorando l'automazione dei tuoi documenti.
type: docs
weight: 6730
url: /it/net/aspose.words.settings/odsofieldmapdata/
---
## OdsoFieldMapData class

Specifica come una colonna nell'origine dati esterna deve essere mappata ai campi di unione predefiniti all'interno del documento.

Per saperne di più, visita il[Unione di posta e creazione di report](https://docs.aspose.com/words/net/mail-merge-and-reporting/) articolo di documentazione.

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
| [Column](../../aspose.words.settings/odsofieldmapdata/column/) { get; set; } | Specifica l'indice basato su zero della colonna all'interno di un'origine dati esterna che deve essere mappato al nome locale di un campo MERGEFIELD specifico. Il valore predefinito è 0. |
| [MappedName](../../aspose.words.settings/odsofieldmapdata/mappedname/) { get; set; } | Specifica il nome del campo di unione predefinito che deve essere mappato al numero di colonna specificato da[`Column`](./column/) proprietà all'interno di questo campo mapping. Il valore predefinito è una stringa vuota. |
| [Name](../../aspose.words.settings/odsofieldmapdata/name/) { get; set; } | Specifica il nome della colonna all'interno di un'origine dati esterna per la colonna il cui indice è specificato da[`Column`](./column/)proprietà. Il valore predefinito è una stringa vuota. |
| [Type](../../aspose.words.settings/odsofieldmapdata/type/) { get; set; } | Specifica se un dato campo di unione di posta è stato mappato a una colonna nella data source esterna indicata o meno. Il valore predefinito èDefault . |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Clone](../../aspose.words.settings/odsofieldmapdata/clone/)() | Restituisce un clone profondo di questo oggetto. |

## Osservazioni

Microsoft Word fornisce alcuni nomi predefiniti per i campi unione che possono essere inseriti in un documento come MERGEFIELD o nei campi ADDRESSBLOCK o GREETINGLINE. Le informazioni specificate in`OdsoFieldMapData` consente di mappare una colonna nell'origine dati esterna a un singolo campo di unione predefinito.

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

* spazio dei nomi [Aspose.Words.Settings](../../aspose.words.settings/)
* assemblea [Aspose.Words](../../)
