---
title: "Aspose::Words::Fields::FieldIf класс"
linktitle: "FieldIf"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldIf класс. Реализует поле IF. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 54000
url: /ru/cpp/aspose.words.fields/fieldif/
---
## FieldIf class


Реализует поле IF. Чтобы узнать больше, посетите статью документации [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) .

```cpp
class FieldIf : public Aspose::Words::Fields::Field,
                public Aspose::Words::Fields::IMergeFieldSurrogate
```

## Методы

| Метод | Описание |
| --- | --- |
| [EvaluateCondition](./evaluatecondition/)() | Оценивает условие. |
| [get_ComparisonOperator](./get_comparisonoperator/)() | Получает или задаёт оператор сравнения. |
| [get_DisplayResult](../field/get_displayresult/)() | Получает текст, представляющий отображаемый результат поля. |
| [get_End](./get_end/)() override | Получает узел, представляющий конец поля. |
| [get_End](../field/get_end/)() const | Получает узел, представляющий конец поля. |
| [get_FalseText](./get_falsetext/)() | Получает или задает текст, отображаемый, если выражение сравнения **false**. |
| [get_FieldEnd](../field/get_fieldend/)() const | Получает узел, представляющий конец поля. |
| [get_FieldStart](../field/get_fieldstart/)() const | Получает узел, представляющий начало поля. |
| [get_Format](../field/get_format/)() | Получает объект [FieldFormat](../fieldformat/), который предоставляет типизированный доступ к форматированию поля. |
| [get_IsDirty](../field/get_isdirty/)() | Получает или задает, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |
| [get_IsLocked](../field/get_islocked/)() | Получает или задает, заблокировано ли поле (не должно пересчитывать свой результат). |
| [get_LeftExpression](./get_leftexpression/)() | Получает или задаёт левую часть выражения сравнения. |
| [get_LocaleId](../field/get_localeid/)() | Получает или задает LCID поля. |
| [get_Result](../field/get_result/)() | Получает или задает текст, находящийся между разделителем поля и его концом. |
| [get_RightExpression](./get_rightexpression/)() | Получает или задаёт правую часть выражения сравнения. |
| [get_Separator](./get_separator/)() override | Получает узел, представляющий разделитель поля. Может быть **null**. |
| [get_Start](./get_start/)() override | Получает узел, представляющий начало поля. |
| [get_Start](../field/get_start/)() const | Получает узел, представляющий начало поля. |
| [get_TrueText](./get_truetext/)() | Получает или задает текст, отображаемый, если выражение сравнения true. |
| virtual [get_Type](../field/get_type/)() const | Получает тип поля Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). Включены как код поля, так и результат дочерних полей. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним элементом его родительского узла, возвращает родительский абзац. Если поле уже удалено, возвращает **null**. |
| [set_ComparisonOperator](./set_comparisonoperator/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldIf::get_ComparisonOperator](./get_comparisonoperator/). |
| [set_FalseText](./set_falsetext/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldIf::get_FalseText](./get_falsetext/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LeftExpression](./set_leftexpression/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldIf::get_LeftExpression](./get_leftexpression/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Сеттер для [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_RightExpression](./set_rightexpression/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldIf::get_RightExpression](./get_rightexpression/). |
| [set_TrueText](./set_truetext/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldIf::get_TrueText](./get_truetext/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Выполняет отсоединение поля. |
| [Update](../field/update/)() | Выполняет обновление поля. Вызывает исключение, если поле уже обновляется. |
| [Update](../field/update/)(bool) | Выполняет обновление поля. Выбрасывает исключение, если поле уже обновляется. |
## Примечания


Сравнивает значения, указанные выражениями [LeftExpression](./get_leftexpression/) и [RightExpression](./get_rightexpression/), используя оператор, указанный в [ComparisonOperator](./get_comparisonoperator/).

Поле в следующем формате будет использоваться как источник слияния почты: { IF 0 = 0 "{PatientsNameFML}" "" \* MERGEFORMAT }

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

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
