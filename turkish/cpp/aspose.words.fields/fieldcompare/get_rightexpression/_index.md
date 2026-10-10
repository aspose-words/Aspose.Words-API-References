---
title: "Aspose::Words::Fields::FieldCompare::get_RightExpression yöntemi"
linktitle: "get_RightExpression"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldCompare::get_RightExpression yöntemi. C++'da karşılaştırma ifadesinin sağ kısmını alır veya ayarlar."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.fields/fieldcompare/get_rightexpression/
---
## FieldCompare::get_RightExpression method


Karşılaştırma ifadesinin sağ kısmını alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldCompare::get_RightExpression()
```


## Örnekler



COMPARE alanı kullanarak ifadeleri nasıl karşılaştıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldCompare>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCompare, true));
field->set_LeftExpression(u"3");
field->set_ComparisonOperator(u"<");
field->set_RightExpression(u"2");
field->Update();

// COMPARE alanı, ifadesinin doğruluğuna bağlı olarak "0" veya "1" görüntüler.
// Bu ifadenin sonucu yanlıştır, bu yüzden alan "0" görüntüler.
ASSERT_EQ(u" COMPARE  3 < 2", field->GetFieldCode());
ASSERT_EQ(u"0", field->get_Result());

builder->Writeln();

field = System::ExplicitCast<Aspose::Words::Fields::FieldCompare>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCompare, true));
field->set_LeftExpression(u"5");
field->set_ComparisonOperator(u"=");
field->set_RightExpression(u"2 + 3");
field->Update();

// Bu alan, ifadenin doğru olması nedeniyle "1" görüntüler.
ASSERT_EQ(u" COMPARE  5 = \"2 + 3\"", field->GetFieldCode());
ASSERT_EQ(u"1", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.COMPARE.docx");
```

## Ayrıca Bakınız

* Class [FieldCompare](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
