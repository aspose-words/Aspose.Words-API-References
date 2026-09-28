---
title: "Aspose::Words::Fields::FieldIfComparisonResult enum"
linktitle: "FieldIfComparisonResult"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldIfComparisonResult enum. Указывает результат оценки условия поля IF в C++."
type: docs
weight: 128000
url: /ru/cpp/aspose.words.fields/fieldifcomparisonresult/
---
## FieldIfComparisonResult enum


Указывает результат оценки условия поля IF.

```cpp
enum class FieldIfComparisonResult
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Ошибка | 0 | В условии есть ошибка. |
| True | 1 | Условие **true**. |
| False | 2 | Условие **false**. |


## Примеры



Показывает, как вставить поле IF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Statement 1: ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIf, true));
field->set_LeftExpression(u"0");
field->set_ComparisonOperator(u"=");
field->set_RightExpression(u"1");

// Поле IF отобразит строку из свойства \"TrueText\",
// или свойства \"FalseText\", в зависимости от истинности построенного нами утверждения.
field->set_TrueText(u"True");
field->set_FalseText(u"False");
field->Update();

// В этом случае \"0 = 1\" неверно, поэтому отображаемый результат будет \"False\".
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

// В этот раз утверждение верно, поэтому отображаемый результат будет \"True\".
ASSERT_EQ(u" IF  5 = \"2 + 3\" True False", field->GetFieldCode());
ASSERT_EQ(Aspose::Words::Fields::FieldIfComparisonResult::True, field->EvaluateCondition());
ASSERT_EQ(u"True", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.IF.docx");
```

## См. также

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
