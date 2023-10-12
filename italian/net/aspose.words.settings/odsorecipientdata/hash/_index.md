---
title: OdsoRecipientData.Hash
second_title: Aspose.Words per .NET API Reference
description: OdsoRecipientData proprietà. Rappresenta il codice hash per questo record. A volte utilizza Microsoft WordHash di un intero record invece di aUniqueTag valore. Il valore predefinito è 0.
type: docs
weight: 40
url: /it/net/aspose.words.settings/odsorecipientdata/hash/
---
## OdsoRecipientData.Hash property

Rappresenta il codice hash per questo record. A volte utilizza Microsoft Word`Hash` di un intero record invece di a[`UniqueTag`](../uniquetag/) valore. Il valore predefinito è 0.

```csharp
public int Hash { get; set; }
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

* class [OdsoRecipientData](../)
* spazio dei nomi [Aspose.Words.Settings](../../odsorecipientdata/)
* assemblea [Aspose.Words](../../../)


