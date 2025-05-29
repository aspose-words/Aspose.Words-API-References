---
title: Odso.RecipientDatas
linktitle: RecipientDatas
articleTitle: RecipientDatas
second_title: Aspose.Words för .NET
description: Hantera din koppling av dokument enkelt med Odso RecipientDatas. Kontrollera inkludering/exkludering av poster med en pålitlig och alltid tillgänglig samling.
type: docs
weight: 70
url: /sv/net/aspose.words.settings/odso/recipientdatas/
---
## Odso.RecipientDatas property

Hämtar eller anger en samling objekt som anger inkludering/exkludering av enskilda poster i dokumentkopplingen. Detta objekt är aldrig`null` .

```csharp
public OdsoRecipientDataCollection RecipientDatas { get; set; }
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

* class [OdsoRecipientDataCollection](../../odsorecipientdatacollection/)
* class [Odso](../)
* namnutrymme [Aspose.Words.Settings](../../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../../)
