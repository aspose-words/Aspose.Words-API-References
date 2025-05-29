---
title: OdsoFieldMapData Class
linktitle: OdsoFieldMapData
articleTitle: OdsoFieldMapData
second_title: .NET için Aspose.Words
description: Harici veri sütunlarının önceden tanımlanmış belge birleştirme alanlarına sorunsuz bir şekilde eşlenmesi ve belge otomasyonunuzun geliştirilmesi için Aspose.Words.OdsoFieldMapData sınıfını keşfedin.
type: docs
weight: 6730
url: /tr/net/aspose.words.settings/odsofieldmapdata/
---
## OdsoFieldMapData class

Harici veri kaynağındaki bir sütunun belge içindeki önceden tanımlanmış birleştirme alanlarına nasıl eşleneceğini belirtir.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Posta Birleştirme ve Raporlama](https://docs.aspose.com/words/net/mail-merge-and-reporting/) belgeleme makalesi.

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
| [Column](../../aspose.words.settings/odsofieldmapdata/column/) { get; set; } | Harici bir veri kaynağındaki sütunun sıfır tabanlı dizinini belirtir. Bu dizin, belirli bir MERGEFIELD alanının yerel adına eşlenir. Varsayılan değer 0'dır. |
| [MappedName](../../aspose.words.settings/odsofieldmapdata/mappedname/) { get; set; } | , tarafından belirtilen sütun numarasına eşlenecek olan önceden tanımlanmış birleştirme alanı adını belirtir.[`Column`](./column/) Bu alan eşlemesindeki özellik. Varsayılan değer boş bir dizedir. |
| [Name](../../aspose.words.settings/odsofieldmapdata/name/) { get; set; } | dizini belirtilen sütun için harici bir veri kaynağındaki sütun adını belirtir.[`Column`](./column/)property. Varsayılan değer boş bir dizedir. |
| [Type](../../aspose.words.settings/odsofieldmapdata/type/) { get; set; } | Belirli bir posta birleştirme alanının belirli harici veri kaynağındaki bir sütuna eşlenip eşlenmediğini belirtir. Varsayılan değer şudur:Default . |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clone](../../aspose.words.settings/odsofieldmapdata/clone/)() | Bu nesnenin derin bir klonunu döndürür. |

## Notlar

Microsoft Word, bir belgeye MERGEFIELD veya olarak eklenmesine izin verdiği bazı önceden tanımlanmış birleştirme alanı adları sağlar ve bunlar ADDRESSBLOCK veya GREETINGLINE alanlarında kullanılır.`OdsoFieldMapData` harici veri kaynağındaki bir sütunun önceden tanımlanmış tek bir birleştirme alanına eşlenmesine olanak tanır.

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

* ad alanı [Aspose.Words.Settings](../../aspose.words.settings/)
* toplantı [Aspose.Words](../../)
