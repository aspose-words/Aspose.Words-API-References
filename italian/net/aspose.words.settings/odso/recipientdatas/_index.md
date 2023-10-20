---
title: Odso.RecipientDatas
linktitle: RecipientDatas
articleTitle: RecipientDatas
second_title: Aspose.Words per .NET
description: Odso RecipientDatas proprietà. Ottiene o imposta una raccolta di oggetti che specificano linclusione/esclusione di singoli record nella stampa unione. Questo oggetto non viene mainullo  in C#.
type: docs
weight: 70
url: /it/net/aspose.words.settings/odso/recipientdatas/
---
## Odso.RecipientDatas property

Ottiene o imposta una raccolta di oggetti che specificano l'inclusione/esclusione di singoli record nella stampa unione. Questo oggetto non viene mai`nullo` .

```csharp
public OdsoRecipientDataCollection RecipientDatas { get; set; }
```

## Esempi

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

* class [OdsoRecipientDataCollection](../../odsorecipientdatacollection/)
* class [Odso](../)
* spazio dei nomi [Aspose.Words.Settings](../../../aspose.words.settings/)
* assemblea [Aspose.Words](../../../)
