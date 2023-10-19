---
title: FieldOptions.LegacyNumberFormat
linktitle: LegacyNumberFormat
articleTitle: LegacyNumberFormat
second_title: Aspose.Words for .NET
description: FieldOptions LegacyNumberFormat mülk. Alanlar için eski AW 13.10 öncesi sayı biçiminin etkin olup olmadığını belirten değeri alır veya ayarlar C#'da.
type: docs
weight: 160
url: /tr/net/aspose.words.fields/fieldoptions/legacynumberformat/
---
## FieldOptions.LegacyNumberFormat property

Alanlar için eski (AW 13.10 öncesi) sayı biçiminin etkin olup olmadığını belirten değeri alır veya ayarlar.

```csharp
public bool LegacyNumberFormat { get; set; }
```

## Notlar

Bu özellik olarak ayarlandığında`doğru`, şablon sembolü "#" .net: 'deki gibi çalıştı. Sayı işareti varsa karşılık gelen rakamla değiştirilir; aksi takdirde sonuç dizesinde hiçbir sembol görünmez.

Bu özellik olarak ayarlandığında`YANLIŞ`, şablon sembolü "#" MS Word gibi çalışır: Bu biçim öğesi sonuçta görüntülenecek gerekli sayısal yerleri belirtir. Sonuç bu yerde bir rakam içermiyorsa, MS Word bir boşluk görüntüler. Örneğin, { = 9 + 6 \# $### }, 15 $'ı görüntüler.

Varsayılan değer:`YANLIŞ`.

## Örnekler

Alanlar için eski sayı biçimlendirmesinin nasıl etkinleştirildiğini gösterir.

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
