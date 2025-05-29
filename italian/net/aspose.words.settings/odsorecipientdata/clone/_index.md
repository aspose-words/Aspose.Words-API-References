---
title: OdsoRecipientData.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words per .NET
description: Crea senza sforzo un clone completo del tuo oggetto OdsoRecipientData con il nostro metodo Clone. Migliora la gestione dei tuoi dati con facilità ed efficienza!
type: docs
weight: 60
url: /it/net/aspose.words.settings/odsorecipientdata/clone/
---
## OdsoRecipientData.Clone method

Restituisce un clone profondo di questo oggetto.

```csharp
public OdsoRecipientData Clone()
```

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

* class [OdsoRecipientData](../)
* spazio dei nomi [Aspose.Words.Settings](../../../aspose.words.settings/)
* assemblea [Aspose.Words](../../../)
