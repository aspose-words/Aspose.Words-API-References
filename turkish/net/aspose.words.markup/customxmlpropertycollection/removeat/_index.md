---
title: CustomXmlPropertyCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: .NET için Aspose.Words
description: CustomXmlPropertyCollection'ınızı RemoveAt yöntemiyle zahmetsizce yönetin; akıcı veri işleme için özellikleri dizine göre hızla kaldırın.
type: docs
weight: 90
url: /tr/net/aspose.words.markup/customxmlpropertycollection/removeat/
---
## CustomXmlPropertyCollection.RemoveAt method

Belirtilen dizindeki bir özelliği kaldırır.

```csharp
public void RemoveAt(int index)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| index | Int32 | Sıfır bazlı endeks. |

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

* class [CustomXmlPropertyCollection](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
