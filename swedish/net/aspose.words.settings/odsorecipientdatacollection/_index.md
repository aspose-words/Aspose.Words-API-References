---
title: Class OdsoRecipientDataCollection
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Settings.OdsoRecipientDataCollection klass. En maskinskriven samling avOdsoRecipientData
type: docs
weight: 5640
url: /sv/net/aspose.words.settings/odsorecipientdatacollection/
---
## OdsoRecipientDataCollection class

En maskinskriven samling av[`OdsoRecipientData`](../odsorecipientdata/)

```csharp
public class OdsoRecipientDataCollection : IEnumerable<OdsoRecipientData>
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [OdsoRecipientDataCollection](odsorecipientdatacollection/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words.settings/odsorecipientdatacollection/count/) { get; } | Hämtar antalet element som finns i samlingen. |
| [Item](../../aspose.words.settings/odsorecipientdatacollection/item/) { get; set; } | Hämtar eller ställer in ett objekt i den här samlingen. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Add](../../aspose.words.settings/odsorecipientdatacollection/add/)(OdsoRecipientData) | Lägger till ett objekt i slutet av den här samlingen. |
| [Clear](../../aspose.words.settings/odsorecipientdatacollection/clear/)() | Tar bort alla element från den här samlingen. |
| [GetEnumerator](../../aspose.words.settings/odsorecipientdatacollection/getenumerator/)() | Returnerar ett uppräkningsobjekt som kan användas för att iterera över alla objekt i samlingen. |
| [RemoveAt](../../aspose.words.settings/odsorecipientdatacollection/removeat/)(int) | Tar bort elementet vid det angivna indexet. |

### Exempel

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

* class [OdsoRecipientData](../odsorecipientdata/)
* namnutrymme [Aspose.Words.Settings](../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../)


