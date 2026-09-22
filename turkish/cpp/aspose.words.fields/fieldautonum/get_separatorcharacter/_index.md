---
title: "Aspose::Words::Fields::FieldAutoNum::get_SeparatorCharacter method"
linktitle: "get_SeparatorCharacter"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldAutoNum::get_SeparatorCharacter yöntemi. C++'ta kullanılacak ayırıcı karakteri alır veya ayarlar."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fields/fieldautonum/get_separatorcharacter/
---
## FieldAutoNum::get_SeparatorCharacter method


Kullanılacak ayırıcı karakteri alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldAutoNum::get_SeparatorCharacter()
```


## Örnekler



Autonum alanlarını kullanarak paragrafların nasıl numaralandırılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Her AUTONUM alanı, AUTONUM alanlarının çalışan bir sayımının mevcut değerini gösterir,
// böylece numaralı bir liste gibi öğeleri otomatik olarak numaralandırabiliriz.
// Bu alan "1." sayısını gösterecek.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAutoNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoNum, true));
builder->Writeln(u"\tParagraph 1.");

ASSERT_EQ(u" AUTONUM ", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldAutoNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoNum, true));
builder->Writeln(u"\tParagraph 2.");

// Ayırıcı karakter, sayının hemen ardından alan sonucunda görünen, varsayılan olarak bir nokta işaretidir.
// Bu özelliği null bırakırsak, ikinci AUTONUM alanımız belgede "2." gösterecek.
ASSERT_TRUE(System::TestTools::IsNull(field->get_SeparatorCharacter()));

// Bu özelliği, dizesinin ilk karakterini yeni ayırıcı karakter olarak uygulamak için ayarlayabiliriz.
// Bu durumda, AUTONUM alanımız artık "2:" gösterecek.
field->set_SeparatorCharacter(u":");

ASSERT_EQ(u" AUTONUM  \\s :", field->GetFieldCode());

doc->Save(get_ArtifactsDir() + u"Field.AUTONUM.docx");
```

## Ayrıca Bakınız

* Class [FieldAutoNum](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
