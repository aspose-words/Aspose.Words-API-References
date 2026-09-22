---
title: "Aspose::Words::Fields::FieldIf::get_RightExpression yöntemi"
linktitle: "get_RightExpression"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldIf::get_RightExpression yöntemi. C++'da karşılaştırma ifadesinin sağ kısmını alır veya ayarlar."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.fields/fieldif/get_rightexpression/
---
## FieldIf::get_RightExpression method


Karşılaştırma ifadesinin sağ kısmını alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldIf::get_RightExpression()
```


## Örnekler



IF alanının nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Statement 1: ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIf, true));
field->set_LeftExpression(u"0");
field->set_ComparisonOperator(u"=");
field->set_RightExpression(u"1");

// IF alanı, \"TrueText\" özelliğinden bir dize gösterecektir,
// veya \"FalseText\" özelliğinden, oluşturduğumuz ifadenin doğruluğuna bağlı olarak.
field->set_TrueText(u"True");
field->set_FalseText(u"False");
field->Update();

// Bu durumda, \"0 = 1\" yanlıştır, bu yüzden gösterilen sonuç \"False\" olacaktır.
ASSERT_EQ(u" IF  0 = 1 True False", field->GetFieldCode());
ASSERT_EQ(Aspose::Words::Fields::FieldIfComparisonResult::False, field->EvaluateCondition());
ASSERT_EQ(u"False", field->get_Result());

builder->Write(u"\nStatement 2: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIf, true));
field->set_LeftExpression(u"5");
field->set_ComparisonOperator(u"=");
field->set_RightExpression(u"2 + 3");
field->set_TrueText(u"True");
field->set_FalseText(u"False");
field->Update();

// Bu sefer ifade doğrudur, bu yüzden gösterilen sonuç \"True\" olacaktır.
ASSERT_EQ(u" IF  5 = \"2 + 3\" True False", field->GetFieldCode());
ASSERT_EQ(Aspose::Words::Fields::FieldIfComparisonResult::True, field->EvaluateCondition());
ASSERT_EQ(u"True", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.IF.docx");
```

## Ayrıca Bakınız

* Class [FieldIf](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
