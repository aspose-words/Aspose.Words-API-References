---
title: Class OdsoFieldMapData
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Settings.OdsoFieldMapData sınıf. Harici veri kaynağındaki bir sütunun belge içindeki önceden tanımlanmış birleştirme alanlarıyla nasıl eşleneceğini belirtir.
type: docs
weight: 5900
url: /tr/net/aspose.words.settings/odsofieldmapdata/
---
## OdsoFieldMapData class

Harici veri kaynağındaki bir sütunun, belge içindeki önceden tanımlanmış birleştirme alanlarıyla nasıl eşleneceğini belirtir.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Adres Mektup Birleştirme ve Raporlama](https://docs.aspose.com/words/net/mail-merge-and-reporting/) dokümantasyon makalesi.

```csharp
public class OdsoFieldMapData
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [OdsoFieldMapData](odsofieldmapdata/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Column](../../aspose.words.settings/odsofieldmapdata/column/) { get; set; } | Belirli bir MERGEFIELD alanının yerel adıyla eşlenmesi gereken, harici bir veri kaynağı içindeki sütunun sıfır tabanlı dizinini belirtir. Varsayılan değer 0. 'dir |
| [MappedName](../../aspose.words.settings/odsofieldmapdata/mappedname/) { get; set; } | Tarafından belirtilen sütun numarasına eşlenecek önceden tanımlanmış birleştirme alanı adını belirtir.[`Column`](./column/) bu alan eşlemesindeki özellik. Varsayılan değer boş bir dizedir. |
| [Name](../../aspose.words.settings/odsofieldmapdata/name/) { get; set; } | dizini tarafından belirtilen sütun için harici veri kaynağı içindeki sütun adını belirtir.[`Column`](./column/)özellik. Varsayılan değer boş bir dizedir. |
| [Type](../../aspose.words.settings/odsofieldmapdata/type/) { get; set; } | Belirli bir adres-mektup birleştirme alanının, belirtilen dış veri kaynağındaki bir sütunla eşlenip eşlenmediğini belirtir. Varsayılan değer:Default . |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clone](../../aspose.words.settings/odsofieldmapdata/clone/)() | Bu nesnenin derin bir kopyasını döndürür. |

### Notlar

Microsoft Word, ADDRESSBLOCK veya GREETINGLINE alanlarında MERGEFIELD veya kullanımı olarak bir belgeye eklenmesine olanak tanıyan önceden tanımlanmış bazı birleştirme alanı adları sağlar. Belirtilen bilgiler`OdsoFieldMapData` , harici veri kaynağındaki bir sütunun önceden tanımlanmış tek bir birleştirme alanına eşlenmesine olanak tanır.

### Örnekler

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

* ad alanı [Aspose.Words.Settings](../../aspose.words.settings/)
* toplantı [Aspose.Words](../../)


