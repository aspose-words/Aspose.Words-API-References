---
title: "Aspose::Words::Fields::FieldCompare::get_ComparisonOperator метод"
linktitle: "get_ComparisonOperator"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldCompare::get_ComparisonOperator метод. Получает или задает оператор сравнения в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/fieldcompare/get_comparisonoperator/
---
## FieldCompare::get_ComparisonOperator method


Получает или задаёт оператор сравнения.

```cpp
System::String Aspose::Words::Fields::FieldCompare::get_ComparisonOperator()
```


## Примеры



Показывает, как сравнивать выражения с помощью поля COMPARE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldCompare>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCompare, true));
field->set_LeftExpression(u"3");
field->set_ComparisonOperator(u"<");
field->set_RightExpression(u"2");
field->Update();

// Поле COMPARE отображает "0" или "1", в зависимости от истинности утверждения.
// Результат этого утверждения — ложь, поэтому поле отобразит "0".
ASSERT_EQ(u" COMPARE  3 < 2", field->GetFieldCode());
ASSERT_EQ(u"0", field->get_Result());

builder->Writeln();

field = System::ExplicitCast<Aspose::Words::Fields::FieldCompare>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCompare, true));
field->set_LeftExpression(u"5");
field->set_ComparisonOperator(u"=");
field->set_RightExpression(u"2 + 3");
field->Update();

// Это поле отображает "1", так как утверждение истинно.
ASSERT_EQ(u" COMPARE  5 = \"2 + 3\"", field->GetFieldCode());
ASSERT_EQ(u"1", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.COMPARE.docx");
```

## См. также

* Class [FieldCompare](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
