---
title: "Aspose::Words::Fields::FieldInfo::get_InfoType yöntemi"
linktitle: "get_InfoType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldInfo::get_InfoType yöntemi. C++'da eklenecek belge özelliğinin tipini alır veya ayarlar."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fields/fieldinfo/get_infotype/
---
## FieldInfo::get_InfoType method


Eklenecek belge özelliğinin türünü alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldInfo::get_InfoType()
```


## Örnekler



INFO alanlarıyla nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Yerleşik "Comments" özelliği için bir değer ayarlayın ve ardından o özelliğin değerini göstermek için bir INFO alanı ekleyin.
doc->get_BuiltInDocumentProperties()->set_Comments(u"My comment");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldInfo>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldInfo, true));
field->set_InfoType(u"Comments");
field->Update();

ASSERT_EQ(u" INFO  Comments", field->GetFieldCode());
ASSERT_EQ(u"My comment", field->get_Result());

builder->Writeln();

// Alanının NewValue özelliği için bir değer ayarlamak ve güncellemek
// alan, aynı zamanda ilgili yerleşik özelliği yeni değerle üzerine yazar.
field = System::ExplicitCast<Aspose::Words::Fields::FieldInfo>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldInfo, true));
field->set_InfoType(u"Comments");
field->set_NewValue(u"New comment");
field->Update();

ASSERT_EQ(u" INFO  Comments \"New comment\"", field->GetFieldCode());
ASSERT_EQ(u"New comment", field->get_Result());
ASSERT_EQ(u"New comment", doc->get_BuiltInDocumentProperties()->get_Comments());

doc->Save(get_ArtifactsDir() + u"Field.INFO.docx");
```

## Ayrıca Bakınız

* Class [FieldInfo](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
