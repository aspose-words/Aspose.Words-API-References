---
title: "Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel yöntemi"
linktitle: "get_CaptionlessTableOfFiguresLabel"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel yöntemi. C++ içinde başlıkların etiket ve numarasını içermeyen bir şekil tablosu oluşturulurken kullanılan dizi tanımlayıcısının adını alır veya ayarlar."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.fields/fieldtoc/get_captionlesstableoffigureslabel/
---
## FieldToc::get_CaptionlessTableOfFiguresLabel method


Şekil tablosu oluşturulurken başlığın etiketi ve numarası dahil edilmeyen sıralama tanımlayıcısının adını alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel()
```


## Örnekler



Dizi tanımlayıcısının adının nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));
fieldToc->set_CaptionlessTableOfFiguresLabel(u"Test");

ASSERT_EQ(u" TOC  \\a Test", fieldToc->GetFieldCode());
```

## Ayrıca Bakınız

* Class [FieldToc](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
