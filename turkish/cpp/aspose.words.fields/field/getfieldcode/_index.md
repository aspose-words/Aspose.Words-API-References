---
title: "Aspose::Words::Fields::Field::GetFieldCode method"
linktitle: "GetFieldCode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::Field::GetFieldCode method. Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların sonuçları C++'ta dahil edilir."
type: docs
weight: 14000
url: /tr/cpp/aspose.words.fields/field/getfieldcode/
---
## Field::GetFieldCode() method


Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir.

```cpp
System::String Aspose::Words::Fields::Field::GetFieldCode()
```


## Örnekler



Bir alan kodu kullanarak bir belgeye alan eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// InsertField yönteminin bu aşırı yüklemesi, eklenen alanları otomatik olarak günceller.
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```


Bir alanın alan kodunun nasıl alınacağını gösterir.
```cpp
// IF alanı içinde bir MERGEFIELD içeren bir belge açın.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Nested fields.docx");
auto fieldIf = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(doc->get_Range()->get_Fields()->idx_get(0));

// Bir alanın alan kodunu almanın iki yolu vardır:
// 1 -  İç alanlarını atla:
ASSERT_EQ(u" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf->GetFieldCode(false));

// 2 -  İç alanlarını dahil et:
ASSERT_EQ(System::String::Format(u" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" "), fieldIf->GetFieldCode(true));

// Varsayılan olarak, GetFieldCode yöntemi iç alanları gösterir.
ASSERT_EQ(fieldIf->GetFieldCode(), fieldIf->GetFieldCode(true));
```

## Ayrıca Bakınız

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## Field::GetFieldCode(bool) method


Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür.

```cpp
System::String Aspose::Words::Fields::Field::GetFieldCode(bool includeChildFieldCodes)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| includeChildFieldCodes | bool | **true** eğer alt alan kodları dahil edilmeliyse. |

## Örnekler



Bir alanın alan kodunun nasıl alınacağını gösterir.
```cpp
// IF alanı içinde bir MERGEFIELD içeren bir belge açın.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Nested fields.docx");
auto fieldIf = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(doc->get_Range()->get_Fields()->idx_get(0));

// Bir alanın alan kodunu almanın iki yolu vardır:
// 1 -  İç alanlarını atla:
ASSERT_EQ(u" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf->GetFieldCode(false));

// 2 -  İç alanlarını dahil et:
ASSERT_EQ(System::String::Format(u" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" "), fieldIf->GetFieldCode(true));

// Varsayılan olarak, GetFieldCode yöntemi iç alanları gösterir.
ASSERT_EQ(fieldIf->GetFieldCode(), fieldIf->GetFieldCode(true));
```

## Ayrıca Bakınız

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
