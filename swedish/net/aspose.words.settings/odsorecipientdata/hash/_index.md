---
title: OdsoRecipientData.Hash
linktitle: Hash
articleTitle: Hash
second_title: Aspose.Words för .NET
description: Upptäck egenskapen OdsoRecipientData Hash, som tillhandahåller en unik hashkod för poster, vilket förbättrar dataintegriteten i Microsoft Word. Standardvärde, 0.
type: docs
weight: 40
url: /sv/net/aspose.words.settings/odsorecipientdata/hash/
---
## OdsoRecipientData.Hash property

Representerar hashkoden för den här posten. Ibland använder Microsoft Word`Hash` av en hel skiva istället för en[`UniqueTag`](../uniquetag/) värde. Standardvärdet är 0.

```csharp
public int Hash { get; set; }
```

## Exempel

Visar hur man får åtkomst till datasamlingen som anger vilka sammanslagna datakällposter som en dokumentkoppling kommer att exkludera.

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

// Vi kan klona elementen i den här samlingen.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// Vi kan också ta bort element individuellt, eller rensa hela samlingen på en gång.
dataCollection.RemoveAt(0);

Assert.AreEqual(69, dataCollection.Count);

dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Se även

* class [OdsoRecipientData](../)
* namnutrymme [Aspose.Words.Settings](../../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../../)
