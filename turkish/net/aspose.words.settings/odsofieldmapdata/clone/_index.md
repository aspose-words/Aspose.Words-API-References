---
title: OdsoFieldMapData.Clone
linktitle: Clone
articleTitle: Clone
second_title: .NET için Aspose.Words
description: Clone metodumuzla OdsoFieldMapData nesnenizin derin bir klonunu zahmetsizce oluşturun. Veri yönetiminizi hassasiyet ve kolaylıkla geliştirin.
type: docs
weight: 60
url: /tr/net/aspose.words.settings/odsofieldmapdata/clone/
---
## OdsoFieldMapData.Clone method

Bu nesnenin derin bir klonunu döndürür.

```csharp
public OdsoFieldMapData Clone()
```

## Örnekler

Veri kaynağı sütunlarını birleştirme alanlarına eşleyen veri koleksiyonuna nasıl erişileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

// Bu koleksiyon, bir posta birleştirmenin bir veri kaynağındaki sütunları nasıl eşleyeceğini tanımlar
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

// Bu koleksiyondaki öğeleri klonla.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// "RemoveAt" metodu elemanlarını indekse göre tek tek kullan.
dataCollection.RemoveAt(0);

Assert.AreEqual(29, dataCollection.Count);

// Tüm koleksiyonu bir kerede temizlemek için "Clear" metodunu kullanın.
dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Ayrıca bakınız

* class [OdsoFieldMapData](../)
* ad alanı [Aspose.Words.Settings](../../../aspose.words.settings/)
* toplantı [Aspose.Words](../../../)
