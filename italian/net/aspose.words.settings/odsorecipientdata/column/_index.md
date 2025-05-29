---
title: OdsoRecipientData.Column
linktitle: Column
articleTitle: Column
second_title: Aspose.Words per .NET
description: Scopri la proprietà Colonna OdsoRecipientData, identifica facilmente colonne di dati univoche per i record, migliorando la gestione dei dati. Il valore predefinito è 0.
type: docs
weight: 30
url: /it/net/aspose.words.settings/odsorecipientdata/column/
---
## OdsoRecipientData.Column property

Specifica la colonna all'interno dell'origine dati che contiene dati univoci per il record corrente. Il valore predefinito è 0.

```csharp
public int Column { get; set; }
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
