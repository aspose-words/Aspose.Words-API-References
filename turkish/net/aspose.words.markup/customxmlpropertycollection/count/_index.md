---
title: CustomXmlPropertyCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words for .NET
description: CustomXmlPropertyCollection Count mülk. Koleksiyonda yer alan öğelerin sayısını alır C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words.markup/customxmlpropertycollection/count/
---
## CustomXmlPropertyCollection.Count property

Koleksiyonda yer alan öğelerin sayısını alır.

```csharp
public int Count { get; }
```

## Örnekler

Akıllı etiketler hakkında ayrıntılı bilgi almak için akıllı etiket özellikleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Smart tags.doc");

// Microsoft Word'ün metnin bir bölümünü bir tür veri olarak tanıdığı bir belgede akıllı etiket görünür,
// ad, tarih veya adres gibi ve onu mor noktalı alt çizgi görüntüleyen bir köprüye dönüştürür.
// Word 2003'te akıllı etiketleri "Araçlar" --> aracılığıyla etkinleştirebiliriz. "Otomatik Düzeltme seçenekleri..." -> "Akıllı Etiketler".
// Giriş belgemizde Microsoft Word'ün akıllı etiket olarak kaydettiği üç nesne var.
// Akıllı etiketler iç içe olabilir, dolayısıyla bu koleksiyon daha fazlasını içerir.
SmartTag[] smartTags = doc.GetChildNodes(NodeType.SmartTag, true).OfType<SmartTag>().ToArray();

Assert.AreEqual(8, smartTags.Length);

// Bir akıllı etiketin "Özellikler" üyesi, her akıllı etiket türü için farklı olacak olan meta verilerini içerir.
// "Tarih" türündeki bir akıllı etiketin özellikleri, o etiketin yılını, ayını ve gününü içerir.
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

// Özelliklere anahtar-değer çifti gibi çeşitli yollardan da erişebiliriz.
Assert.True(properties.Contains("Day"));
Assert.AreEqual("22", properties["Day"].Value);
Assert.AreEqual("2003", properties[2].Value);
Assert.AreEqual(1, properties.IndexOfKey("Month"));

// Aşağıda, özellikler koleksiyonundan öğeleri kaldırmanın üç yolu verilmiştir.
// 1 - Dizine göre kaldır:
properties.RemoveAt(3);

Assert.AreEqual(3, properties.Count);

// 2 - İsme göre kaldır:
properties.Remove("Year");

Assert.AreEqual(2, properties.Count);

// 3 - Tüm koleksiyonu bir kerede temizle:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Ayrıca bakınız

* class [CustomXmlPropertyCollection](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
