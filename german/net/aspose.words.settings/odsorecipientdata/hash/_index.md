---
title: OdsoRecipientData.Hash
linktitle: Hash
articleTitle: Hash
second_title: Aspose.Words für .NET
description: Entdecken Sie die Hash-Eigenschaft von OdsoRecipientData, die einen eindeutigen Hashcode für Datensätze bereitstellt und so die Datenintegrität in Microsoft Word verbessert. Standardwert: 0.
type: docs
weight: 40
url: /de/net/aspose.words.settings/odsorecipientdata/hash/
---
## OdsoRecipientData.Hash property

Stellt den Hash-Code für diesen Datensatz dar. Manchmal verwendet Microsoft Word`Hash` eines ganzen Datensatzes statt eines[`UniqueTag`](../uniquetag/) Wert. Der Standardwert ist 0.

```csharp
public int Hash { get; set; }
```

## Beispiele

Zeigt, wie auf die Datensammlung zugegriffen wird, die angibt, welche Datensätze aus Seriendruckdatenquellen bei einem Seriendruck ausgeschlossen werden.

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

// Wir können Elemente auch einzeln entfernen oder die gesamte Sammlung auf einmal löschen.
dataCollection.RemoveAt(0);

Assert.AreEqual(69, dataCollection.Count);

dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Siehe auch

* class [OdsoRecipientData](../)
* namensraum [Aspose.Words.Settings](../../../aspose.words.settings/)
* Montage [Aspose.Words](../../../)
