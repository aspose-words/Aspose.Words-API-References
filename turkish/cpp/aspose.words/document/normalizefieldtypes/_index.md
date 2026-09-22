---
title: "Aspose::Words::Document::NormalizeFieldTypes metodu"
linktitle: "NormalizeFieldTypes"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::NormalizeFieldTypes metodu. Tüm belgede FieldStart, FieldSeparator, FieldEnd'in FieldType değerlerini, C++'daki alan kodlarında bulunan alan türlerine karşılık gelecek şekilde değiştirir."
type: docs
weight: 66000
url: /tr/cpp/aspose.words/document/normalizefieldtypes/
---
## Document::NormalizeFieldTypes method


Belge genelindeki [FieldStart](../../../aspose.words.fields/fieldstart/), [FieldSeparator](../../../aspose.words.fields/fieldseparator/), [FieldEnd](../../../aspose.words.fields/fieldend/) öğelerinin [FieldType](../../../aspose.words.fields/fieldchar/get_fieldtype/) değerlerini, alan kodlarında bulunan alan türlerine karşılık gelecek şekilde değiştirir.

```cpp
void Aspose::Words::Document::NormalizeFieldTypes()
```

## Açıklamalar


Alan türlerini etkileyen belge değişikliklerinden sonra bu yöntemi kullanın.

Belgenin belirli bir bölümünde alan türü değerlerini değiştirmek için [NormalizeFieldTypes](../../range/normalizefieldtypes/) yöntemini kullanın.

## Örnekler



Bir alanın türünü alan koduyla güncel tutmanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE", nullptr);

// Aspose.Words, alan kodlarına göre alan türlerini otomatik olarak algılar.
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());

// Alan kodunu belirleyen alanın ham metnini manuel olarak değiştirin.
auto fieldText = System::ExplicitCast<Aspose::Words::Run>(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(Aspose::Words::NodeType::Run, true)->idx_get(0));
fieldText->set_Text(u"PAGE");

// Alan kodunu değiştirmek, bu alanı farklı bir türe dönüştürmüştür,
// ancak alanın tür özellikleri hâlâ eski türü gösteriyor.
ASSERT_EQ(u"PAGE", field->GetFieldCode());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Start()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Separator()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_End()->get_FieldType());

// Bu yöntemle bu özellikleri güncelleyerek mevcut değeri gösterin.
doc->NormalizeFieldTypes();

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_Type());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_Start()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_Separator()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_End()->get_FieldType());
```

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
