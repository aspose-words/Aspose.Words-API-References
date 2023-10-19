---
title: OdsoFieldMapDataCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words for .NET
description: OdsoFieldMapDataCollection RemoveAt yöntem. Belirtilen dizindeki öğeyi kaldırır C#'da.
type: docs
weight: 70
url: /tr/net/aspose.words.settings/odsofieldmapdatacollection/removeat/
---
## OdsoFieldMapDataCollection.RemoveAt method

Belirtilen dizindeki öğeyi kaldırır.

```csharp
public void RemoveAt(int index)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| index | Int32 | Öğenin sıfır tabanlı dizini. |

## Örnekler

Veri kaynağı sütunlarını birleştirme alanlarıyla eşleştiren veri koleksiyonuna nasıl erişileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

// Bu koleksiyon, adres-mektup birleştirmenin bir veri kaynağındaki sütunları nasıl eşleyeceğini tanımlar
// önceden tanımlanmış MERGEFIELD, ADDRESSBLOCK ve GREETINGLINE alanlarına.
OdsoFieldMapDataCollection dataCollection = doc.MailMergeSettings.Odso.FieldMapDatas;
Assert.AreEqual(30, dataCollection.Count);

using (IEnumerator<OdsoFieldMapData> enumerator = dataCollection.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"Field map data index {index++}, type \"{enumerator.Current.Type}\":");

        Console.WriteLine(
            enumerator.Current.Type != OdsoFieldMappingType.Null
                ? $"\tColumn \"{enumerator.Current.Name}\", number {enumerator.Current.Column} mapped to merge field \"{enumerator.Current.MappedName}\"."
                : "\tNo valid column to field mapping data present.");
    }
}

// Bu koleksiyondaki öğeleri klonlayın.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// "RemoveAt" yönteminin öğelerini ayrı ayrı dizine göre kullanın.
dataCollection.RemoveAt(0);

Assert.AreEqual(29, dataCollection.Count);

// Koleksiyonun tamamını bir kerede temizlemek için "Temizle" yöntemini kullanın.
dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Ayrıca bakınız

* class [OdsoFieldMapDataCollection](../)
* ad alanı [Aspose.Words.Settings](../../../aspose.words.settings/)
* toplantı [Aspose.Words](../../../)
