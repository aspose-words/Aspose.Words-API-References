---
title: OdsoRecipientDataCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words för .NET
description: OdsoRecipientDataCollection GetEnumerator metod. Returnerar ett uppräkningsobjekt som kan användas för att iterera över alla objekt i samlingen i C#.
type: docs
weight: 60
url: /sv/net/aspose.words.settings/odsorecipientdatacollection/getenumerator/
---
## OdsoRecipientDataCollection.GetEnumerator method

Returnerar ett uppräkningsobjekt som kan användas för att iterera över alla objekt i samlingen.

```csharp
public IEnumerator<OdsoRecipientData> GetEnumerator()
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

* class [OdsoRecipientData](../../odsorecipientdata/)
* class [OdsoRecipientDataCollection](../)
* namnutrymme [Aspose.Words.Settings](../../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../../)
