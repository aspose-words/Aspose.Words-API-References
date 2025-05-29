---
title: OdsoFieldMapDataCollection Class
linktitle: OdsoFieldMapDataCollection
articleTitle: OdsoFieldMapDataCollection
second_title: .NET için Aspose.Words
description: OdsoFieldMapData nesnelerinin etkili yönetimi için güçlü bir türlendirilmiş koleksiyon olan Aspose.Words OdsoFieldMapDataCollection sınıfını keşfedin.
type: docs
weight: 6740
url: /tr/net/aspose.words.settings/odsofieldmapdatacollection/
---
## OdsoFieldMapDataCollection class

Bir tür koleksiyonu[`OdsoFieldMapData`](../odsofieldmapdata/) nesneler.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Posta Birleştirme ve Raporlama](https://docs.aspose.com/words/net/mail-merge-and-reporting/) belgeleme makalesi.

```csharp
public class OdsoFieldMapDataCollection : IEnumerable<OdsoFieldMapData>
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [OdsoFieldMapDataCollection](odsofieldmapdatacollection/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.settings/odsofieldmapdatacollection/count/) { get; } | Koleksiyonda bulunan öğelerin sayısını alır. |
| [Item](../../aspose.words.settings/odsofieldmapdatacollection/item/) { get; set; } | Bu koleksiyondaki bir öğeyi alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.settings/odsofieldmapdatacollection/add/)(*[OdsoFieldMapData](../odsofieldmapdata/)*) | Bu koleksiyonun sonuna bir nesne ekler. |
| [Clear](../../aspose.words.settings/odsofieldmapdatacollection/clear/)() | Bu koleksiyondaki tüm öğeleri kaldırır. |
| [GetEnumerator](../../aspose.words.settings/odsofieldmapdatacollection/getenumerator/)() | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilen bir numaratör nesnesi döndürür. |
| [RemoveAt](../../aspose.words.settings/odsofieldmapdatacollection/removeat/)(*int*) | Belirtilen dizindeki öğeyi kaldırır. |

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

* class [OdsoFieldMapData](../odsofieldmapdata/)
* property [FieldMapDatas](../odso/fieldmapdatas/)
* ad alanı [Aspose.Words.Settings](../../aspose.words.settings/)
* toplantı [Aspose.Words](../../)
