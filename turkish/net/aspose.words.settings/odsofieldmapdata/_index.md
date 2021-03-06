---
title: OdsoFieldMapData
second_title: Aspose.Words for .NET API Referansı
description: Dış veri kaynağındaki bir sütunun belge içindeki önceden tanımlanmış birleştirme alanlarıyla nasıl eşleneceğini belirtir.
type: docs
weight: 5600
url: /tr/net/aspose.words.settings/odsofieldmapdata/
---
## OdsoFieldMapData class

Dış veri kaynağındaki bir sütunun belge içindeki önceden tanımlanmış birleştirme alanlarıyla nasıl eşleneceğini belirtir.

```csharp
public class OdsoFieldMapData
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [OdsoFieldMapData](odsofieldmapdata)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Column](../../aspose.words.settings/odsofieldmapdata/column) { get; set; } | Belirli bir MERGEFIELD alanının yerel adıyla eşlenecek olan bir harici veri kaynağındaki sütunun sıfır tabanlı dizinini belirtir. Varsayılan değer 0. 'dir. |
| [MappedName](../../aspose.words.settings/odsofieldmapdata/mappedname) { get; set; } | tarafından belirtilen sütun numarasıyla eşleştirilecek olan önceden tanımlanmış birleştirme alanı adını belirtir.[`Column`](./column) bu alan eşleme içindeki özellik. Varsayılan değer boş bir dizedir. |
| [Name](../../aspose.words.settings/odsofieldmapdata/name) { get; set; } | tarafından dizini belirtilen sütun için bir dış veri kaynağı içindeki sütun adını belirtir.[`Column`](./column) property. Varsayılan değer boş bir dizedir. |
| [Type](../../aspose.words.settings/odsofieldmapdata/type) { get; set; } | Belirli bir adres mektup birleştirme alanının, verilen harici veri kaynağındaki bir sütunla eşlenip eşlenmediğini belirtir. Varsayılan değerDefault . |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clone](../../aspose.words.settings/odsofieldmapdata/clone)() | Bu nesnenin derin bir klonunu döndürür. |

### Notlar

Microsoft Word, ADRESSBLOCK veya GREETINGLINE alanlarında MERGEFIELD veya kullanımı olarak bir belgeye eklenmesine izin verdiği bazı önceden tanımlanmış birleştirme alanı adları sağlar. Belirtilen bilgiler[`OdsoFieldMapData`](../odsofieldmapdata) , harici veri kaynağındaki bir sütunun önceden tanımlanmış tek bir birleştirme alanıyla eşlenmesine olanak tanır.

### Örnekler

Alanları birleştirmek için veri kaynağı sütunlarını eşleyen veri koleksiyonuna nasıl erişileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

// Bu koleksiyon, adres mektup birleştirmenin bir veri kaynağındaki sütunları nasıl eşleyeceğini tanımlar
// önceden tanımlanmış MERGEFIELD, ADRESSBLOCK ve GREETINGLINE alanlarına.
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

// "RemoveAt" yöntem öğelerini dizine göre ayrı ayrı kullanın.
dataCollection.RemoveAt(0);

Assert.AreEqual(29, dataCollection.Count);

// Tüm koleksiyonu bir kerede temizlemek için "Clear" yöntemini kullanın.
dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Settings](../../aspose.words.settings)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
