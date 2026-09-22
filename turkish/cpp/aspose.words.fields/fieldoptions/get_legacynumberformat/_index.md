---
title: "Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat yöntemi."
linktitle: "get_LegacyNumberFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat yöntemi. Alanlar için eski (AW 13.10'dan önceki) sayı biçiminin etkin olup olmadığını gösteren değeri alır veya ayarlar (C++)."
type: docs
weight: 16000
url: /tr/cpp/aspose.words.fields/fieldoptions/get_legacynumberformat/
---
## FieldOptions::get_LegacyNumberFormat method


Alanlar için eski (AW 13.10'dan önceki) sayı formatının etkin olup olmadığını gösteren değeri alır veya ayarlar.

```cpp
bool Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat() const
```

## Açıklamalar


Bu özellik **true** olarak ayarlandığında, şablon simgesi "#" .net'te olduğu gibi çalışır: Eğer mevcutsa pound işaretini karşılık gelen rakamla değiştirir; aksi takdirde sonuç dizesinde hiçbir simge görünmez.

Bu özellik **false** olarak ayarlandığında, şablon simgesi "#" MS Word gibi çalışır: Bu biçim öğesi, sonuçta gösterilecek gerekli sayısal basamakları belirtir. Sonuç o basamakta bir rakam içermiyorsa, MS Word bir boşluk gösterir. Örneğin, { = 9 + 6 \# $### } ifadesi $ 15 gösterir.

Varsayılan değer **false**'tur.

## Örnekler



Alanlar için eski sayı biçimlendirmesinin nasıl etkinleştirileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"= 2 + 3 \\# $##");

ASSERT_EQ(u"$ 5", field->get_Result());

doc->get_FieldOptions()->set_LegacyNumberFormat(true);
field->Update();

ASSERT_EQ(u"$5", field->get_Result());
```

## Ayrıca Bakınız

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
