---
title: CustomXmlPropertyCollection Class
linktitle: CustomXmlPropertyCollection
articleTitle: CustomXmlPropertyCollection
second_title: .NET için Aspose.Words
description: Özel XML niteliklerini ve akıllı etiket özelliklerini etkili bir şekilde yönetmek için güçlü bir araç olan Aspose.Words.Markup.CustomXmlPropertyCollection'ı keşfedin.
type: docs
weight: 4640
url: /tr/net/aspose.words.markup/customxmlpropertycollection/
---
## CustomXmlPropertyCollection class

Özel XML niteliklerinin veya akıllı etiket özelliklerinin bir koleksiyonunu temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yapılandırılmış Belge Etiketleri veya İçerik Denetimi](https://docs.aspose.com/words/net/working-with-content-control-sdt/) belgeleme makalesi.

```csharp
public class CustomXmlPropertyCollection : IEnumerable<CustomXmlProperty>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.markup/customxmlpropertycollection/count/) { get; } | Koleksiyonda bulunan öğelerin sayısını alır. |
| [Item](../../aspose.words.markup/customxmlpropertycollection/item/) { get; } | Belirtilen ada sahip bir özelliği alır. (2 indexers) |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlpropertycollection/add/)(*[CustomXmlProperty](../customxmlproperty/)*) | Koleksiyona bir özellik ekler. |
| [Clear](../../aspose.words.markup/customxmlpropertycollection/clear/)() | Koleksiyondaki tüm öğeleri kaldırır. |
| [Contains](../../aspose.words.markup/customxmlpropertycollection/contains/)(*string*) | Koleksiyonun verilen ada sahip bir özelliği içerip içermediğini belirler. |
| [GetEnumerator](../../aspose.words.markup/customxmlpropertycollection/getenumerator/)() | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilen bir numaratör nesnesi döndürür. |
| [IndexOfKey](../../aspose.words.markup/customxmlpropertycollection/indexofkey/)(*string*) | Koleksiyondaki belirtilen özelliğin sıfır tabanlı dizinini döndürür. |
| [Remove](../../aspose.words.markup/customxmlpropertycollection/remove/)(*string*) | Belirtilen ada sahip bir özelliği koleksiyondan kaldırır. |
| [RemoveAt](../../aspose.words.markup/customxmlpropertycollection/removeat/)(*int*) | Belirtilen dizindeki bir özelliği kaldırır. |

## Notlar

Öğeler şunlardır[`CustomXmlProperty`](../customxmlproperty/) nesneler.

## Örnekler

Akıllı etiketler hakkında derinlemesine bilgi edinmek için akıllı etiket özellikleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Smart tags.doc");

// Microsoft Word'de bir belgede görünen akıllı etiket, metnin bir kısmını bir tür veri olarak tanır,
// isim, tarih veya adres gibi bir bilgiyi alıp mor noktalı alt çizgi gösteren bir köprü metnine dönüştürür.
// Word 2003'te akıllı etiketleri "Araçlar" -> "Otomatik Düzeltme seçenekleri..." -> "Akıllı Etiketler" yoluyla etkinleştirebiliriz.
// Giriş belgemizde Microsoft Word'ün akıllı etiket olarak kaydettiği üç nesne var.
// Akıllı etiketler iç içe olabilir, bu nedenle bu koleksiyon daha fazlasını içerir.
SmartTag[] smartTags = doc.GetChildNodes(NodeType.SmartTag, true).OfType<SmartTag>().ToArray();

Assert.AreEqual(8, smartTags.Length);

// Akıllı etiketin "Özellikler" üyesi, her akıllı etiket türü için farklı olacak olan meta verilerini içerir.
// "Tarih" tipi akıllı etiketin özellikleri yıl, ay ve günü içerir.
CustomXmlPropertyCollection properties = smartTags[7].Properties;

Assert.AreEqual(4, properties.Count);

using (IEnumerator<CustomXmlProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"Property name: {enumerator.Current.Name}, value: {enumerator.Current.Value}");
        Assert.AreEqual("", enumerator.Current.Uri);
    }
}

// Ayrıca özelliklere anahtar-değer çifti gibi çeşitli yollarla da erişebiliriz.
Assert.True(properties.Contains("Day"));
Assert.AreEqual("22", properties["Day"].Value);
Assert.AreEqual("2003", properties[2].Value);
Assert.AreEqual(1, properties.IndexOfKey("Month"));

// Aşağıda, özellik koleksiyonundan öğeleri kaldırmanın üç yolu bulunmaktadır.
// 1 - Dizinle kaldır:
properties.RemoveAt(3);

Assert.AreEqual(3, properties.Count);

// 2 - İsme göre kaldır:
properties.Remove("Year");

Assert.AreEqual(2, properties.Count);

// 3 - Tüm koleksiyonu bir defada temizle:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Ayrıca bakınız

* class [CustomXmlProperty](../customxmlproperty/)
* ad alanı [Aspose.Words.Markup](../../aspose.words.markup/)
* toplantı [Aspose.Words](../../)
