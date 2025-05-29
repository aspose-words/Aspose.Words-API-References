---
title: OdsoRecipientDataCollection Class
linktitle: OdsoRecipientDataCollection
articleTitle: OdsoRecipientDataCollection
second_title: Aspose.Words per .NET
description: Scopri Aspose.Words.Settings.OdsoRecipientDataCollection, una potente raccolta tipizzata per gestire in modo efficiente OdsoRecipientData nelle tue applicazioni.
type: docs
weight: 6770
url: /it/net/aspose.words.settings/odsorecipientdatacollection/
---
## OdsoRecipientDataCollection class

Una raccolta tipizzata di[`OdsoRecipientData`](../odsorecipientdata/)

Per saperne di più, visita il[Unione di posta e creazione di report](https://docs.aspose.com/words/net/mail-merge-and-reporting/) articolo di documentazione.

```csharp
public class OdsoRecipientDataCollection : IEnumerable<OdsoRecipientData>
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [OdsoRecipientDataCollection](odsorecipientdatacollection/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.settings/odsorecipientdatacollection/count/) { get; } | Ottiene il numero di elementi contenuti nella raccolta. |
| [Item](../../aspose.words.settings/odsorecipientdatacollection/item/) { get; set; } | Ottiene o imposta un elemento in questa raccolta. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words.settings/odsorecipientdatacollection/add/)(*[OdsoRecipientData](../odsorecipientdata/)*) | Aggiunge un oggetto alla fine di questa raccolta. |
| [Clear](../../aspose.words.settings/odsorecipientdatacollection/clear/)() | Rimuove tutti gli elementi da questa raccolta. |
| [GetEnumerator](../../aspose.words.settings/odsorecipientdatacollection/getenumerator/)() | Restituisce un oggetto enumeratore che può essere utilizzato per scorrere tutti gli elementi nella raccolta. |
| [RemoveAt](../../aspose.words.settings/odsorecipientdatacollection/removeat/)(*int*) | Rimuove l'elemento all'indice specificato. |

## Esempi

Mostra come accedere alla raccolta di dati che designa quali record di origine dati di unione verranno esclusi dalla stampa unione.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

OdsoRecipientDataCollection dataCollection = doc.MailMergeSettings.Odso.RecipientDatas;

Assert.AreEqual(70, dataCollection.Count);

using (IEnumerator<OdsoRecipientData> enumerator = dataCollection.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine(
            $"Odso recipient data index {index++} will {(enumerator.Current.Active ? "" : "not ")}be imported upon mail merge.");
        Console.WriteLine($"\tColumn #{enumerator.Current.Column}");
        Console.WriteLine($"\tHash code: {enumerator.Current.Hash}");
        Console.WriteLine($"\tContents array length: {enumerator.Current.UniqueTag.Length}");
    }
}

// Possiamo clonare gli elementi in questa raccolta.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// Possiamo anche rimuovere gli elementi singolarmente o cancellare l'intera raccolta in una volta sola.
dataCollection.RemoveAt(0);

Assert.AreEqual(69, dataCollection.Count);

dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Guarda anche

* class [OdsoRecipientData](../odsorecipientdata/)
* spazio dei nomi [Aspose.Words.Settings](../../aspose.words.settings/)
* assemblea [Aspose.Words](../../)
