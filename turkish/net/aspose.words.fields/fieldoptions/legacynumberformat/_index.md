---
title: FieldOptions.LegacyNumberFormat
linktitle: LegacyNumberFormat
articleTitle: LegacyNumberFormat
second_title: .NET için Aspose.Words
description: Alanlar için eski sayı biçimlerini etkinleştirmek veya devre dışı bırakmak, uyumluluğu ve performansı artırmak için FieldOptions LegacyNumberFormat özelliğini keşfedin.
type: docs
weight: 160
url: /tr/net/aspose.words.fields/fieldoptions/legacynumberformat/
---
## FieldOptions.LegacyNumberFormat property

Alanlar için eski (AW 13.10'dan önceki) sayı biçiminin etkin olup olmadığını gösteren değeri alır veya ayarlar.

```csharp
public bool LegacyNumberFormat { get; set; }
```

## Notlar

Bu özellik şu şekilde ayarlandığında:`doğru`, şablon sembolü "#" .net: 'deki gibi çalıştı. Eğer varsa diyez işaretini karşılık gelen rakamla değiştirir; aksi takdirde sonuç dizesinde hiçbir sembol görünmez.

Bu özellik şu şekilde ayarlandığında:`YANLIŞ`, şablon simgesi "#" MS Word: olarak çalışır. Bu biçim öğesi sonuçta görüntülenecek gerekli sayısal yerleri belirtir. Sonuç o yerde bir rakam içermiyorsa, MS Word bir boşluk görüntüler. Örneğin, { = 9 + 6 \# $### } $ 15 görüntüler.

Varsayılan değer:`YANLIŞ`.

## Örnekler

Alanlar için eski sayı biçimlendirmesinin nasıl etkinleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("= 2 + 3 \\# $##");

Assert.AreEqual("$ 5", field.Result);

doc.FieldOptions.LegacyNumberFormat = true;
field.Update();

Assert.AreEqual("$5", field.Result);
```

### Ayrıca bakınız

* class [FieldOptions](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
