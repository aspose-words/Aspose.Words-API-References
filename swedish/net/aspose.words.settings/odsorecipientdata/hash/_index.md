---
title: OdsoRecipientData.Hash
linktitle: Hash
articleTitle: Hash
second_title: Aspose.Words för .NET
description: OdsoRecipientData Hash fast egendom. Representerar hashkoden för denna post. Ibland använder Microsoft WordHash av en hel skiva istället för enUniqueTag value. Standardvärdet är 0 i C#.
type: docs
weight: 40
url: /sv/net/aspose.words.settings/odsorecipientdata/hash/
---
## OdsoRecipientData.Hash property

Representerar hashkoden för denna post. Ibland använder Microsoft Word`Hash` av en hel skiva istället för en[`UniqueTag`](../uniquetag/) value. Standardvärdet är 0.

```csharp
public int Hash { get; set; }
```

## Exempel

Visar hur man får åtkomst till insamlingen av data som anger vilka sammanslagningsdatakällaposter en sammanslagning kommer att utesluta.

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
