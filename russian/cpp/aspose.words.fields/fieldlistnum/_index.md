---
title: "Aspose::Words::Fields::FieldListNum класс"
linktitle: "FieldListNum"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldListNum класс. Реализует поле LISTNUM. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 64000
url: /ru/cpp/aspose.words.fields/fieldlistnum/
---
## FieldListNum class


Реализует поле LISTNUM. Чтобы узнать больше, посетите статью документации [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldListNum : public Aspose::Words::Fields::Field,
                     public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Получает текст, представляющий отображаемый результат поля. |
| [get_End](../field/get_end/)() const | Получает узел, представляющий конец поля. |
| [get_FieldEnd](../field/get_fieldend/)() const | Получает узел, представляющий конец поля. |
| [get_FieldStart](../field/get_fieldstart/)() const | Получает узел, представляющий начало поля. |
| [get_Format](../field/get_format/)() | Получает объект [FieldFormat](../fieldformat/), который предоставляет типизированный доступ к форматированию поля. |
| [get_HasListName](./get_haslistname/)() | Возвращает значение, указывающее, предоставлено ли имя определения абстрактной нумерации в коде поля. |
| [get_IsDirty](../field/get_isdirty/)() | Получает или задает, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |
| [get_IsLocked](../field/get_islocked/)() | Получает или задает, заблокировано ли поле (не должно пересчитывать свой результат). |
| [get_ListLevel](./get_listlevel/)() | Получает или задает уровень в списке, переопределяя поведение поля по умолчанию. |
| [get_ListName](./get_listname/)() | Получает или задает имя определения абстрактной нумерации, используемого для нумерации. |
| [get_LocaleId](../field/get_localeid/)() | Получает или задает LCID поля. |
| [get_Result](../field/get_result/)() | Получает или задает текст, находящийся между разделителем поля и его концом. |
| [get_Separator](../field/get_separator/)() | Получает узел, представляющий разделитель поля. Может быть **null**. |
| [get_Start](../field/get_start/)() const | Получает узел, представляющий начало поля. |
| [get_StartingNumber](./get_startingnumber/)() | Получает или задает начальное значение для этого поля. |
| virtual [get_Type](../field/get_type/)() const | Получает тип поля Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). Включены как код поля, так и результат дочерних полей. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() override | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним элементом его родительского узла, возвращает родительский абзац. Если поле уже удалено, возвращает **null**. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_ListLevel](./set_listlevel/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldListNum::get_ListLevel](./get_listlevel/). |
| [set_ListName](./set_listname/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldListNum::get_ListName](./get_listname/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Сеттер для [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_StartingNumber](./set_startingnumber/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldListNum::get_StartingNumber](./get_startingnumber/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Выполняет отсоединение поля. |
| [Update](../field/update/)() | Выполняет обновление поля. Вызывает исключение, если поле уже обновляется. |
| [Update](../field/update/)(bool) | Выполняет обновление поля. Выбрасывает исключение, если поле уже обновляется. |

## Примеры



Показывает, как нумеровать абзацы с помощью полей LISTNUM.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Поля LISTNUM отображают число, которое увеличивается в каждом поле LISTNUM.
// Эти поля также имеют разнообразные параметры, позволяющие использовать их для имитации нумерованных списков.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));

// Списки по умолчанию начинают счёт с 1, но мы можем задать другое значение, например 0.
// Это поле отобразит "0)".
field->set_StartingNumber(u"0");
builder->Writeln(u"Paragraph 1");

ASSERT_EQ(u" LISTNUM  \\s 0", field->GetFieldCode());

// Поля LISTNUM поддерживают отдельные счётчики для каждого уровня списка.
// Вставка поля LISTNUM в тот же абзац, что и другое поле LISTNUM
// увеличивает уровень списка вместо счёта.
// Следующее поле продолжит счёт, который мы начали выше, и отобразит значение "1" на уровне списка 1.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);

// Это поле начнёт счёт на уровне списка 2. Оно отобразит значение "1".
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);

// Это поле начнёт счёт на уровне списка 3. Оно отобразит значение "1".
// Разные уровни списка имеют разное форматирование,
// поэтому эти поля вместе отобразят значение "1)a)i)".
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);
builder->Writeln(u"Paragraph 2");

// Следующее поле LISTNUM, которое мы вставим, продолжит счёт на уровне списка
// на котором находилось предыдущее поле LISTNUM.
// Мы можем использовать свойство "ListLevel", чтобы перейти к другому уровню списка.
// Если бы это поле LISTNUM осталось на уровне списка 3, оно отобразило бы "ii)",
// но, поскольку мы переместили его на уровень списка 2, оно продолжает счёт на этом уровне и отображает "b)".
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_ListLevel(u"2");
builder->Writeln(u"Paragraph 3");

ASSERT_EQ(u" LISTNUM  \\l 2", field->GetFieldCode());

// Мы можем задать свойство ListName, чтобы поле имитировало другой тип поля AUTONUM.
// "NumberDefault" имитирует AUTONUM, "OutlineDefault" имитирует AUTONUMOUT,
// а "LegalDefault" имитирует поля AUTONUMLGL.
// Имя списка "OutlineDefault" с 1 в качестве начального номера приведет к отображению "I.".
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_StartingNumber(u"1");
field->set_ListName(u"OutlineDefault");
builder->Writeln(u"Paragraph 4");

ASSERT_TRUE(field->get_HasListName());
ASSERT_EQ(u" LISTNUM  OutlineDefault \\s 1", field->GetFieldCode());

// Имя списка ListName не переносится из предыдущего поля, поэтому нам потребуется установить его для каждого нового поля.
// Это поле продолжает счет с другим именем списка и отображает "II.".
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_ListName(u"OutlineDefault");
builder->Writeln(u"Paragraph 5");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.LISTNUM.docx");
```

## См. также

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
