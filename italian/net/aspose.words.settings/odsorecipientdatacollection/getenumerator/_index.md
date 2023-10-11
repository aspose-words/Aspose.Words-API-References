---
title: OdsoRecipientDataCollection.GetEnumerator
second_title: Aspose.Words per .NET API Reference
description: OdsoRecipientDataCollection metodo. Restituisce un oggetto enumeratore che può essere utilizzato per scorrere tutti gli elementi della raccolta.
type: docs
weight: 60
url: /it/net/aspose.words.settings/odsorecipientdatacollection/getenumerator/
---
## OdsoRecipientDataCollection.GetEnumerator method

Restituisce un oggetto enumeratore che può essere utilizzato per scorrere tutti gli elementi della raccolta.

```csharp
public IEnumerator<OdsoRecipientData> GetEnumerator()
```

### Esempi

Mostra come accedere alla raccolta di dati che indica quali record dell'origine dati di unione verranno esclusi da una stampa unione.

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

// Possiamo anche rimuovere elementi individualmente o cancellare l'intera raccolta in una volta.
dataCollection.RemoveAt(0);

Assert.AreEqual(69, dataCollection.Count);

dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Guarda anche

* class [OdsoRecipientData](../../odsorecipientdata/)
* class [OdsoRecipientDataCollection](../)
* spazio dei nomi [Aspose.Words.Settings](../../odsorecipientdatacollection/)
* assemblea [Aspose.Words](../../../)


