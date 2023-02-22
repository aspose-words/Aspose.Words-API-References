---
title: OdsoRecipientDataCollection.Item
second_title: Aspose.Words für .NET-API-Referenz
description: OdsoRecipientDataCollection eigendom. Ruft ein Element in dieser Sammlung ab oder legt es fest.
type: docs
weight: 30
url: /de/net/aspose.words.settings/odsorecipientdatacollection/item/
---
## OdsoRecipientDataCollection indexer

Ruft ein Element in dieser Sammlung ab oder legt es fest.

```csharp
public OdsoRecipientData this[int index] { get; set; }
```

### Beispiele

Zeigt, wie auf die Datensammlung zugegriffen wird, die angibt, welche Zusammenführungsdatenquellen-Datensätze bei einem Seriendruck ausgeschlossen werden.

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

// Wir können die Elemente in dieser Sammlung klonen.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// Wir können auch einzelne Elemente entfernen oder die gesamte Sammlung auf einmal löschen.
dataCollection.RemoveAt(0);

Assert.AreEqual(69, dataCollection.Count);

dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Siehe auch

* class [OdsoRecipientData](../../odsorecipientdata/)
* class [OdsoRecipientDataCollection](../)
* namensraum [Aspose.Words.Settings](../../odsorecipientdatacollection/)
* Montage [Aspose.Words](../../../)


