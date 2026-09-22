---
title: "Aspose::Words::Fields::FieldAdvance::get_DownOffset yöntemi"
linktitle: "get_DownOffset"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldAdvance::get_DownOffset yöntemi. C++'ta alandan sonraki metnin aşağı kaydırılması için gereken nokta sayısını alır veya ayarlar."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fields/fieldadvance/get_downoffset/
---
## FieldAdvance::get_DownOffset method


Alanı izleyen metnin aşağı doğru hareket ettirilmesi gereken puan sayısını alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldAdvance::get_DownOffset()
```


## Örnekler



Bir ADVANCE alanı eklemeyi ve özelliklerini düzenlemeyi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"This text is in its normal place.");

// Aşağıda, ADVANCE alanını kullanarak ardından gelen metnin konumunu ayarlamanın iki yolu verilmiştir.
// Bir ADVANCE alanının etkileri paragraf sonuna kadar uygulanmaya devam eder,
// veya başka bir ADVANCE alanı ofset/koordinat değerlerini günceller.
// 1 -  Yönsel bir ofset belirtin:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_RightOffset(u"5");
field->set_UpOffset(u"5");

ASSERT_EQ(u" ADVANCE  \\r 5 \\u 5", field->GetFieldCode());

builder->Write(u"This text will be moved up and to the right.");

field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_DownOffset(u"5");
field->set_LeftOffset(u"100");

ASSERT_EQ(u" ADVANCE  \\d 5 \\l 100", field->GetFieldCode());

builder->Writeln(u"This text is moved down and to the left, overlapping the previous text.");

// 2 -  Metni koordinatlarla belirtilen bir konuma taşıyın:
field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_HorizontalPosition(u"-100");
field->set_VerticalPosition(u"200");

ASSERT_EQ(u" ADVANCE  \\x -100 \\y 200", field->GetFieldCode());

builder->Write(u"This text is in a custom position.");

doc->Save(get_ArtifactsDir() + u"Field.ADVANCE.docx");
```

## Ayrıca Bakınız

* Class [FieldAdvance](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
